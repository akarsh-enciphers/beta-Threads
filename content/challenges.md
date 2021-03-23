+++
title = "Challenges"
date = "2020-12-16"
sidemenu = "true"
description = "A Vulnerable Web Application Lab"
+++

As we know there are many vulnerabilities present in the Threads web application so to find out and exploit each of  these vulnerabilities are the challenges on Threads application. We have categorized the vulnerabilities into 4 parts (low,medium,high,critical) on the basis of how it is going to affect your system.

**Note** : ( In order to solve the challenges hints are provided with them).
   
Here is the list of all the challenges according to the severity category to solve and practise:


## Low 

### XSS(Self-XSS)

**About**: [Self-xss](https://portswigger.net/web-security/cross-site-scripting/reflected) has the behaviour similar to Reflected XSS however it can not be executed with simple ways like Url Crafting, Cross domain request.In this victim themself submit the xss payload (javascript code) in their browser that means you/victim yourself can exploit only. So in order to exploit this vulnerability as an attacker you need to convince the victim to submit/paste the javascript code in the browser (which is not simply not possible). Hence it is considered as a low vulnerability until unless chaining with other vulnerabilities like CSRF. 

Reference to Learn more:[Self-Cross Site Scripting](https://portswigger.net/web-security/cross-site-scripting/reflected) 


### Hidden Directories

**About**: Sometimes Application has hidden directories which are not visible on a public website and these can reveal useful information for potential attacks. Hidden Directories can be found via brute force using a wordlist.


### Cross-site Request Forgery(CSRF)

**About**: In this victim executes unwanted actions on behalf of the attacker on an application in which they are authenticated. [CSRF](https://owasp.org/www-community/attacks/csrf) can be done at the places in an application where state change events happen like password change,delete,update and similar. Attackers can trick a victim to click on a link via social engineering and execute the unwanted actions on a web application.

 Reference to Learn more:[Cross-site Request Forgery](https://owasp.org/www-community/attacks/csrf).


### No Password Policy

**About**: Sometimes the  application does not require that users should have strong passwords,  which makes it easier for attackers to compromise user accounts. There are many password policy followed by many application like:
  - use of both upper-case and lower-case letters (case sensitivity).
  - inclusion of one or more numerical digits.
  - inclusion of special characters, such as @, #, $.
  - prohibition of words found in a password blacklist.
  - prohibition of words found in the user's personal information.
  - prohibition of use of company name or an abbreviation.
  - prohibition of passwords that match the format of calendar dates, license plate numbers, telephone numbers, or other common numbers.

When all these policies are followed by the application then it becomes tough for attackers to get password for a user account 

### Weak Reset Password Implementation


### Automatic User Enumeration

### No password required for account deletion

### Simultaneous sessions are being kept active on the same browser 


## Medium 

### No rate Limiting

**About**: [No Rate limiting](https://cheatsheetseries.owasp.org/cheatsheets/Denial_of_Service_Cheat_Sheet.html#rate-limiting) Application or Server does not keep any restriction on sending the request from one client to server or web-application in a particular time frame which can cause problems to web applications/server. And bad people can perform DDos attacks by creating unusual traffic to server/web applications.

 Reference to learn more:[No Rate limiting](https://cheatsheetseries.owasp.org/cheatsheets/Denial_of_Service_Cheat_Sheet.html#rate-limiting)


### Failure to invalidate the session after password change

### Clickjacking

### Bruteforce of password leading to account takeover


## High

### Insecure Direct Object Reference

**About**: An insecure direct object reference [(IDOR)](https://portswigger.net/web-security/access-control/idor) is an access control vulnerability. Which occurs when unvalidated input is used to reference or access an object by using an unique ID. If by changing ID the attacker can access the details/object which should not be accessible, it's an IDOR. 

 Reference to learn more:[Insecure Direct Object Reference](https://portswigger.net/web-security/access-control/idor)

**Note**: There are two IDOR present in the application.

### Server-side Request Forgery(SSRF)

**About**: In a Server-Side Request Forgery [(SSRF)](https://owasp.org/www-community/attacks/Server_Side_Request_Forgery) victim server makes the http request on the behalf of the attacker to some other mentioned server by the attacker.

 Reference to learn more:[Server-side Request Forgery](https://owasp.org/www-community/attacks/Server_Side_Request_Forgery)

**Note**: There are two SSRF present in the application. one of which is a blind SSRF


### XSS(Stored XSS)

**About**: [Stored xss](https://portswigger.net/web-security/cross-site-scripting/stored) occurs when the application processes and stores untrusted data (malicious javascript) at the server side and includes that data in later http response in a unsafe way which can triggers the malicious javascript as input to application.

 Reference to learn more:[Stored-Cross Site Scripting](https://portswigger.net/web-security/cross-site-scripting/stored) 

**Note**: There are two Stored XSS in the application.

### Chaining of CSRF/IDOR with XSS


## Critical   

### JWT Authentication

**About**: JWT(JSON Web Token) are used for authentication and A statement from “RFC 7518 (JSON Web Algorithms) states that "A key of the same size as the hash output (for instance, 256 bits for "HS256") or larger MUST be used with this algorithm. Because shorter can be brute forced this is the one of the weak points that can occur while implementing jwt.

 Reference to learn more:[JSON Web Token](https://jwt.io/introduction/)

**Note**:  For JWT challenge, hardcoded email is *‘admin@threadsapp.test’* *. So first make  an account  the given email id and then try to forge the token.


These are all the challenges present on Threads application which you can solve.
Happy learning,Happy hacking!
 

