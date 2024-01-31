# Remote Code Execution Attempt - TetCTF Challenge

## Analyzing the URL Endpoint

In the TetCTF challenge, a link was provided: [https://huk5xbypcc.execute-api.ap-southeast-2.amazonaws.com/dev/vulnerable?vulnerable="Welcome to TetCTF!"](https://huk5xbypcc.execute-api.ap-southeast-2.amazonaws.com/dev/vulnerable?vulnerable="Welcome%20to%20TetCTF!"). Visiting this link displayed the message "Welcome to TetCTF!".

## Attempting Remote Code Execution (RCE)

Upon discovering that anything within quotes after `?vulnerable=` would be printed, I suspected a potential vulnerability for remote code execution (RCE). I attempted to exploit this by appending a command within quotes, such as `"hi|ls"`. However, the attempt resulted in an error.

## Further Exploitation Attempts

I experimented with various derivatives of the RCE payload in Burp Suite. Despite numerous attempts, I was unable to successfully exploit the vulnerability.

## Utilizing Nmap for Reconnaissance

To gather more information about the host server and its services, I attempted to use Nmap. However, my attempts were met with throttling, limiting my ability to conduct further reconnaissance.

