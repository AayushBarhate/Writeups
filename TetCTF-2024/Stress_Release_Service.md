# Remote Code Execution Attempt - CTF Challenge Writeup

## Understanding the Input Restrictions

During the CTF challenge, I encountered strict input restrictions that only allowed specific characters, namely `@` `!` , etc. Any attempt to input other characters(a-z) or numbers resulted in the webpage giving an error(Wrong way to release stress it seems).

## Remote Code Execution Attempt

Upon realizing the input restrictions, I hypothesized that the system might be vulnerable to remote code execution (RCE) attacks. I attempted various RCE payloads, such as `@!@!@!@!@!;ls` and `@!@!@!|ls`, to execute commands and obtain information. However, none of these attempts yielded the desired results.

## Continued Exploration

Despite multiple attempts and searches, I encountered challenges in further exploiting the system. The limitations imposed by the input restrictions and the lack of successful RCE payloads hindered my progress in uncovering additional vulnerabilities or obtaining the flag.