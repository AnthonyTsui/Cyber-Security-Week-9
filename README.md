# Cyber-Security-Week-9

Time spent: 5 hours

Exploits:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

## #1 SQL Injection - Blue 
![SQL Injection](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/SQLinjection.gif)  
  1. Insert ' OR SLEEP(5)=0--' into the URL
  2. Server will execute the SQL command and sleep

## #2 Session Hijack - Blue 
![Session Hijack](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/sessionhijacking.gif)  

  1. Login at the link https://35.184.88.145/blue/public/staff/login.php
  2. Go to https://35.184.88.145/blue/public/hacktools/change_session_id.php to obtain the session ID
  3. Open another browser, and go to https://35.184.88.145/blue/public/hacktools/change_session_id.php again.
  4. Copy over the session ID from the second browser and paste it into the initial page to change it.

## #3 Insecure Direct Object Reference - Red
![IDOR](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/idor.gif)  

  1. On the Find a Salesperson section click on any of the users 
  2. In the URL change the id to 10
  3. Note that this profile is not reachable via the Find a Salesperson section of the website

## #4 Cross-Site Request Forgery - Red 
![Cross-site Forgery](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/csrf.gif)  

  1. Go to the Users section in the login tab of the Red section of the website
  2. Note the user with user id 1 and their information
  3. Run the cross_site_request.html file 
  4. Return to the login page and under users: note that the user with id 1 has modified information
  

## #5 User Enumeration - Green 
![User Enumeration](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/user-enumeration.gif)  

  1. Login and type pperson as the username with any password  
  2. Note that the error message is in bold and enter in a random string of letters with any password
  3. Note that the error message is not in bold, meaning the user does NOT exist.
  
## #6 Cross-Site Scripting - Green
![Cross Site Scripting](https://github.com/atsui4688/Cyber-Security-Week-9/blob/master/cs-scripting.gif)  

  1. In the contact section of the Green page, enter your name, email ,and <script>alert('Mallory found the XSS!');</script> in the feed back
  2. Submit and click login and feedback to display an alert message.
