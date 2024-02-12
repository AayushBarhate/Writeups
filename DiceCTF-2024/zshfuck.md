# Jail.zsh Script Analysis - CTF Writeup

## Understanding the Jail.zsh Script

Upon analyzing the jail.zsh script provided in the CTF challenge, I discovered that it imposed strict restrictions on user input. Only 6 characters were allowed for the charset, and certain characters such as '*', '?', and '`' were banned.

## Initial Exploration

I began by examining the jail.zsh script to understand its functionality and constraints. It became evident that the script was designed to limit user input and restrict certain characters.

## Directory Exploration

Using the limited character set allowed by the script, I attempted to explore the directory structure within the jail environment. The "ls" command provided some insight into the contents of the directories, helping me identify the location of the jail script.

I used the "find ." command to list all files and directories within the jail environment. This approach allowed me to locate the getflag executable, which was nested 4 directories deep.

![find](<images/image.png>)

## Exploitation Attempt

Given the constraints imposed by the jail.zsh script, executing the getflag executable directly within the jail environment was not feasible. Therefore, I shifted my focus to crashing the script to gain proper shell access.

### PS Command

I used the "ps" command to list all processes within the jail environment. This provided information about running processes, including the jail script. However, attempting to execute any processes, including the jail script, did not yield the desired outcome.

![processes listed](<images/ps.png>)


### Kill Command

As an alternative approach, I tried to terminate processes using the "kill" command, hoping to crash the script and gain proper shell access. Unfortunately, this attempt was also unsuccessful, and the script remained resilient to my efforts.

![kill](<images/kill.png>)


