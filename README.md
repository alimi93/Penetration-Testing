# Penetration-Testing


<h2>Description</h2>
Web application testing is a friendly hacking test carried out by a cybersecurity professional to check for weak spots in a website before malicious hackers can exploit them. For this project, I will be testing the DVWA (Damn Vulnerable Web Application) website.
<br />

<p align="center">

  SQL Injection

 <br/>
 Sql injection is a web security vulnerablity that allows attackes to manipulate SQL queries by injection malicious input, enabling unauthorized access to modify database

SQL injection Attempt: paylods like id=1' Union All Select show that user inputer can manipulate SQL querries
<img src="https://i.imgur.com/wGlsCsi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Ping the Server attempt:  <br/>
In a vulnerable application, if a user can input  127.0.0.1|whoami, the application might execute  this command through a shell.  Ping the Server: Attempt to ping 127.0.0.1
 (essentially checking if the server is reachable).  Execute whoami: Simultaneously execute the whoami command, revealing the user

<img src="https://i.imgur.com/VQzMihg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
command injection attempt: <br/>

The command 127.0.0.1 && uname-a represents another example of a potential command injection attempt, where an attacker could execute multiple commands in a vulnerable
 application. 127.0.0.1: This is the localhost IP address  &&(Logical AND Operator): In command-line environments, the && operator allows the execution of the second command  only if the first command succeeds uname-a: This command provides system information, displaying details like the kernel name, version, and system architecture. It's commonly used for troubleshooting and system diagnostics.
 
<img src="https://i.imgur.com/kVKlaqs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<br />
Command Injection to display password:  <br/>

127.0.0.1 && cat /etc/passwd is another example of a potential command injection attack. Here's a detailed breakdown: Breakdown of the Command 127.0.0.1:
 This is the loopback address or localhost IP address. It refers to the  local machine and is commonly used for network tests. &&(Logical AND Operator):
 The &&operator executes the following command only if the preceding command succeeds. In this case, if the command 127.0.0.1 executes without errors, the following command (cat /etc/passwd) will  execute. cat /etc/passwd:  The cat command is used to read and display the contents of files in Unix/Linux systems. The /etc/passwd file contains user account information, including usernames, user IDs, group IDs, home directories, and other details. Importantly, it usually has read  permissions for all users, making it accessible even without elevate  privileges
 
<img src="https://i.imgur.com/fDKiT1n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<br />
Stored XSS Vulnerability:  <br/>

stored XSS Vulnerablity: The injected scripts is stored in the websites database and will ran every time a user visit that page where the message is displayed. This can lead to malicious action, as an attacker can use XSS to steal user data or manipulate the web page

<img src="https://i.imgur.com/dQ7OBbW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reverse Shell:  <br/>
<img src="https://i.imgur.com/264HXGP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reverse Shell Connection established:  <br/>
<img src="https://i.imgur.com/EElI3Zu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p align="center">
Payload exploitation: <br/>
<img src="https://i.imgur.com/7VhIc7D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Database Dump:  <br/>
<img src="https://i.imgur.com/K73Z0mm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Stealing Cookies: <br/>
<img src="https://i.imgur.com/iPISVML.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Terminal Showing Cookies:  <br/>
<img src="https://i.imgur.com/gtmkdy3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

  Tools Used to carry out this Penetration Testing

Kali Linux

Dvwa website

sqlmap

Netcat

 Recommendations: 
1. SQL Injection
 Prepared Statements: Use prepared statements (or parameterized queries) instead of dynamic queries. This helps separate SQL logic from data.
 Input Validation: Validate and sanitize all user inputs. Ensure that inputs conform to expected formats.
 WebApplication Firewalls (WAF): Implement WAFs to monitor and block malicious traffic.

 2. Command Injection
 Recommendations:
 Input Sanitization: Strictly validate input data, ensuring it does not contain any potentially harmful characters or command sequences.

 3. Cross-Site Scripting (XSS)
 Recommendations:
 Output Encoding: Properly encode all data sent to the browser, especially user-generated content. Use libraries that help in encoding
 data.
 Input Validation: Validate inputs to ensure that they meet expected formats and do not contain executable scripts.

 4. Stored XSS Vulnerability
 Recommendations:
 Database Sanitization: Sanitize data before storing it in the database to block malicious scripts from being saved.

5. Use of Outdated Software
 Recommendations:
 Regular Updates: Keep all software and components up to date, including the database management systems and libraries you depend on.
 Version Monitoring: Monitor software versions and be aware of which versions are vulnerable to security exploits.

 6. Secure Configuration
 Recommendations:
 Least Privilege Principle: Ensure that the application operates under the principle of least privilege. Avoid using default administrative
 users where possible.
 Secure Default Settings: Change default credentials and settings to more secure options. Disable unnecessary features or services.

 7. Network Security
 Recommendations:
 Firewalls: Employ firewalls to restrict access to sensitive parts of your application and databases.
 Intrusion Detection Systems (IDS): Utilize IDS to monitor and analyze network traffic for suspicious activities.

 8. Logging and Monitoring
 Recommendations:
 Implement Logging: Maintain detailed logs of all user activities and potential security incidents to enable rapid analysis and response.
 Regular Audits: Conduct regular security audits and penetration tests to identify and fix vulnerabilities proactively.

