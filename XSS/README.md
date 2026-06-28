\# XSS (cross-site Scripting)



XSS is a web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. XSS works by manipulating a vulnerable web site so that it returns malicious JavaScript to users. After that, the attacker can compromise the interactions between the user and the application.







\## The main types



* Reflected XSS



The malicious payload is immediately reflected in the server's response after being submitted by the user.



* Stored XSS



The payload is permanently stored by the application (for example in a database or comment section) and executed whenever another user visits the affected page.



* DOM-Based XSS



The vulnerability exists entirely on the client side. JavaScript modifies the DOM using untrusted data without proper sanitization.







\## Detection

* Test user input fields with payloads to detect potential XSS vulnerabilities
* Inspect the source code of the pages to detect any suspicious JavaScript or HTML tags







\## Payloads used



* Simple example : <script>alert('Test XSS');</script>
* Example in an HTML attribute : <img src="x" onerror="alert('XSS test')">







\## Impact



* Theft of users’ identification details
* Execution of unauthorised actions
* Website defacement

