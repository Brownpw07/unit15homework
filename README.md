## Unit 15 Homework: Web Vulnerabilities and Hardening

### Part 1: Q&A

#### The URL Cruise Missile

The URL is the gateway to the web, providing the user with unrestricted access to all available online resources. In the wrong hands can be used as a weapon to launch attacks.

Use the graphic below to answer the following questions:

| Protocol         | Host Name                 | Path                   | Parameters               |
| ---------------- | :-----------------------: | ---------------------- | ------------------------ |
| **http://**      | **`www.buyitnow.tv`**     | **/add.asp**           | **?item=price#1999**     |


1. Which part of the URL can be manipulated by an attacker to exploit a vulnerable back-end database system? 
	- The Parameters.

2. Which part of the URL can be manipulated by an attacker to cause a vulnerable web server to dump the `/etc/passwd` file? Also, name the attack used to exploit this vulnerability.
	- The Path is used in a directory path traversal exploit.
   
3. Name three threat agents that pose a risk for injection attacks.
	- Politcal activists, advanced persistent threats, script kiddies.

4. What kinds of sources can act as an attack vector for injection attacks?
	- Web forms without input sanitization.

5. Injection attacks exploit which part of the CIA triad?
	- Integrity.

6. Which two mitigation methods can be used to thwart injection attacks?
	- Input sanitization and input validation.

____

#### Web Server Infrastructure


Use the graphic below to answer the following questions:

| Stage 1        | Stage 2             | Stage 3                 | Stage 4              | Stage 5          |
| :------------: | :-----------------: | :---------------------: | :------------------: | :--------------: |
| **Client**     | **Firewall**        | **Web Server**          | **Web Application**  | **Database**     |
   
   
1. What stage is the most inner part of the web architecture where data such as, customer names, addresses, account numbers, and credit card info, is stored?
	- Database.

2. Which stage includes online forms, word processors, shopping carts, video and photo editing, spreadsheets, file scanning, file conversion, and email programs such as Gmail, Yahoo and AOL.
	- Web application.

3. What stage is the component that stores files (e.g. HTML documents, images, CSS stylesheets, and JavaScript files) that's connected to the Internet and provides support for physical data interactions between other devices connected to the web?
	- Web server.

4. What stage is where the end user interacts with the World Wide Web through the use of a web browser?
	- Client.

5. Which stage is designed to prevent unauthorized access to and from protected web server resources?
	- Firewall.
----


#### Server Side Attacks

In today’s globally connected cyber community, network and OS level attacks are well defended through the proper deployment of technical security controls such as, firewalls, IDS, Data Loss Prevention, EndPoint and security. However, web servers are accessible from anywhere on the web, making them vulnerable to attack.

1. What is the process called that cleans and scrubs user input in order to prevent it from exploiting security holes by proactively modifying user input.
	- Input sanitization.

2. Name the process that tests user and application-supplied input. The process is designed to prevent malformed data from entering a data information system by verifying user input meets a specific set of criteria (i.e. a string that does not contain standalone single quotation marks).
	- Input validation.

3. **Secure SDLC** is the process of ensuring security is built into web applications throughout the entire software development life cycle. Name three reasons why organization might fail at producing secure web applications.
	- It can have a high implementation cost, insufficient standardization, and has a total reliance on web app firewalls.

4. How might an attacker exploit the `robots.txt` file on a web server?
	- They could use a malicious web crawler to index a target web server and gather info for later use.

5. What steps can an organization take to obscure or obfuscate their contact information on domain registry web sites?
	- They can pay a fee to have the information redacted from public eyes, but it is still listed for cases of abuse.
   
6. True or False: As a network defender, `Client-Side` validation is preferred over `Server-Side` validation because it's easier to defend against attacks.
	- False.
   - Explain why you chose the answer that you did.
	- Server-side validation gives fewer options for the user to exploit and less control over how information is processed.

____

#### Web Application Firewalls

WAFs are designed to defend against different types of HTTP attacks and various query types such as SQLi and XSS.

WAFs are typically present on web sites that use strict transport security mechanisms such as online banking or e-commerce websites.

1. Which layer of the OSI model do WAFs operate at?
	- The application layer.

2. A WAF helps protect web applications by filtering and monitoring what?
	- Web traffic based on source.

3. True or False: A WAF based on the negative security model (Blacklisting) protects against known attacks, and a WAF based on the positive security model (Whitelisting) allows pre-approved traffic to pass.
	- True.
____

#### Authentication and Access Controls

Security enhancements designed to require users to present two or more pieces of evidence or credentials when logging into an account is called multi-factor authentication.

- Legislation and regulations such as The Payment Card Industry (PCI) Data Security Standard requires the use of MFAs for all network access to a Card Data Environment (CDE).

- Security administrators should have a comprehensive understanding of the basic underlying principles of how MFA works.

1. Define all four factors of multifactor authentication and give examples of each:

   - What you know:
	- Password or security questions.
   
   - What you have:
	- Synced key generator or key card. 
   
   - Who you are:
	- Photo ID or fingerprint.

   - Where you are:
	- GPS verification or landline phone call in verification.

   
2. True or False: A password and pin is an example of 2-factor authentication.
	- False, these are both knowledge based authentication methods. Often, a different type of information is used as a 2nd factor.
   
3. True or False: A password and `google authenticator app` is an example of 2-factor authentication.
	- True, these are an example of a knowledge based and an ownership based authentication.
   
4. What is a constrained user interface? 
	- a user interface that limits access to various functions by preventing those specific requests.
----
____

### Part 2: The Challenge 


#### Challenge #1

Your first mission is to break the authentication scheme. There are a number of ways to accomplish this task.

- **Hint #1**: Sometimes, form fields are shy!

- **Hint #2**: Find the hidden JavaScript.

<ins>[Challenge 1 Complete](images/challenge1complete.png)</ins>

#### Challenge #2

Next, steal all of the credit card numbers from the database. 

- **Hint #1**: Sometimes cookies wear different clothes to change their appearances.

- **Hint #2**: Break your way into the conversation and inject your own ideas.

<ins>[Challenge 2 Complete](images/challenge2.png)</ins>

#### Challenge #3

Your third and final mission is no easy feat. Your final act is to deface the website. This requires multiple skill sets, all of which you’ve learned and will need for this final act.
Two clues:

- **Hint 1**: You will need to use command injection.

- **Hint 2**: You will need to locate the `webgoat_challenge_guest.jsp` file and inject it with code in order to deface the website.

<ins>[Challenge 3](images/challenge3_1.png)</ins> <ins>[Complete](images/challenge3_2.png)</ins>

---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

