1) Open The Directory Containing The Script 

2) Double Click The xss.html file 

3) Open your Dev Tools to view the inline javascript

4) Use the filter to search for inner.html 

5) Navigate back to the webpage

6) Enter an xss payload to exploit the vulnerability

(EXPLAINED)

The webpage is vulnerable to XSS because it uses innerHTML to insert user input directly into the DOM. This allows an attacker to inject malicious HTML or JavaScript code into the webpage. A safer method in javascript would be something like inner.Text instead. Here is a one of the vulnerable parts of the code:
	
	document.getElementById('output').innerHTML = message;

When innerHTML is used, any HTML tags or JavaScript code in the user input will be rendered by the browser, potentially allowing an attacker to execute arbitrary scripts like:
	
 <img src=x onerror=alert('XSS')>


The Walkthrough is available on Youtube:

https://www.youtube.com/watch?v=i-ZlhnlWsWA

Support My Work With A Cup Of Coffee

![CashTag$ copy](https://github.com/Invader00100100/Xss-Lab/assets/102438675/a356ac38-97bf-4a4f-8765-10a4eaa51f56)


