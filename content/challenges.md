+++
title = "Challenges"
date = "2020-12-16"
sidemenu = "true"
description = "A vulnerable web application developed by Enciphers"
+++

As we know there are many vulnerabilities present in the Threads web application so to find out and exploit each of  these vulnerabilities are the challenges on Threads application. We have categorized the vulnerabilities into 4 parts (low,medium,high,critical) on the basis of how it is going to affect your system.

**Note** : ( In order to solve the challenges hints are provided with them).
   
Here is the list of all the challenges according to the severity category to solve and practise:


## Low 

### XSS(Self-XSS)

**About**: [Self-xss](https://portswigger.net/web-security/cross-site-scripting/reflected) has the behaviour similar to Reflected XSS however it can not be executed with simple ways like Url Crafting, Cross domain request.In this victim themself submit the xss payload (javascript code) in their browser that means you/victim yourself can exploit only. So in order to exploit this vulnerability as an attacker you need to convince the victim to submit/paste the javascript code in the browser (which is not simply not possible). Hence it is considered as a low vulnerability until unless chaining with other vulnerabilities like CSRF. 

Reference to Learn more:[Self-Cross Site Scripting](https://portswigger.net/web-security/cross-site-scripting/reflected) 

**Hint**: Self-XSS is present in the profile section of the application. You need to insert a javascript payload to exploit this vulnerability. 


### Hidden Directories

**About**: Sometimes Application has hidden directories which are not visible on a public website and these can reveal useful information for potential attacks. Hidden Directories can be found via brute force using a wordlist.

**Hint**: There are many hidden directories present in Threads application one consist of an admin section where an admin user can login. You can find the hidden directories with the help of following tools like DIRSEARCH, FUZZ dir etc.

### Cross-site Request Forgery(CSRF)

**About**: In this victim executes unwanted actions on behalf of the attacker on an application in which they are authenticated. [CSRF](https://owasp.org/www-community/attacks/csrf) can be done at the places in an application where state change events happen like password change,delete,update and similar. Attackers can trick a victim to click on a link via social engineering and execute the unwanted actions on a web application.

 Reference to Learn more:[Cross-site Request Forgery](https://owasp.org/www-community/attacks/csrf).

**Hint**: Can you try to change user password,username on profile using CSRF.


## Medium 

### MongoDB Injection(NoSQL Injection)

**About**: [NoSQL](https://www.netsparker.com/blog/web-security/what-is-nosql-injection/) injection vulnerabilities allow attackers to inject code into commands for databases that don’t use SQL queries, such as MongoDB. NoSQL injection attacks can be especially dangerous because code is injected and executed on the server in the language of the web application, potentially allowing arbitrary code execution.

 Reference to learn more:[MongoDB Injection](https://www.netsparker.com/blog/web-security/what-is-nosql-injection/)

**Hint** : It is present in a section where the application retrieve values from the database according to the user input like in fields like search bar.


## High

### Insecure Direct Object Reference

**About**: An insecure direct object reference [(IDOR)](https://portswigger.net/web-security/access-control/idor) is an access control vulnerability. Which occurs when unvalidated input is used to reference or access an object by using an unique ID. If by changing ID the attacker can access the details/object which should not be accessible, it's an IDOR. 

 Reference to learn more:[Insecure Direct Object Reference](https://portswigger.net/web-security/access-control/idor)

**Hint**:  Deleting Comment/Post of any user using BurpSuite (having the UUID).

### Server-side Request Forgery(SSRF)

**About**: In a Server-Side Request Forgery [(SSRF)](https://owasp.org/www-community/attacks/Server_Side_Request_Forgery) victim server makes the http request on the behalf of the attacker to some other mentioned server by the attacker.

 Reference to learn more:[Server-side Request Forgery](https://owasp.org/www-community/attacks/Server_Side_Request_Forgery)

**Hint**: It is present in the profile section of the application where an user can upload picture via URL.

### XSS(Stored XSS)

**About**: [Stored xss](https://portswigger.net/web-security/cross-site-scripting/stored) occurs when the application processes and stores untrusted data (malicious javascript) at the server side and includes that data in later http response in a unsafe way which can triggers the malicious javascript as input to application.

 Reference to learn more:[Stored-Cross Site Scripting](https://portswigger.net/web-security/cross-site-scripting/stored) 

**Hint**:  Under the profile section, you can change your website link, it would execute only when visited in an unauthenticated state.


## Critical   

### JWT Authentication

**About**: JWT(JSON Web Token) are used for authentication and A statement from “RFC 7518 (JSON Web Algorithms) states that "A key of the same size as the hash output (for instance, 256 bits for "HS256") or larger MUST be used with this algorithm. Because shorter can be brute forced this is the one of the weak points that can occur while implementing jwt.

 Reference to learn more:[JSON Web Token](https://jwt.io/introduction/)

**Note**:  For JWT challenge, hardcoded email is *‘test@test.com’* and the password for it is *‘123’*. So first make sure that an account exists with the above email id and then try to forge the token.

**Hint**:  The application uses cookie-based authentication but has the support of JWT as well.There is a /management page which has an authentication system which works via JWT API. When logging in to the /management page by providing your credentials, you would see that you are not authorized to log in. Now to become authorized user one has to forge the token of the admin account since its using HMAC so the current secret key is thr3@ds@000t so forge a token with *‘test@test.com’*.You can replace the token via burp request and response or just change the token under local storage and refresh the page you should have admin access where you can delete other users.

These are all the challenges present on Threads application which you can solve.
Happy learning,Happy hacking!
 

