When a graphical application freezes, which command would you use first to try and stop it (kill or pkill)? Why? What would be your last resort signal if the first attempt doesn’t work?

pkill will be the first choice as by using this we can target the application or process by its name without requiring the pid which the kill command needs
the last resort will be using SIGKILL as it forces the operating system to terminate a process instantly, which can cause data loss or corrupted files.


Why is it a bad idea to add a directory like /tmp to your $PATH? - What are the potential security implications of modifying your $PATH carelessly?

Adding public directories like /tmp to your $PATH is a major security risk because anyone can put files there. An attacker can plant a malicious script named after a common command (like ls), and your system will execute their malware instead of the real command, granting them your user permissions.

An alias can save you a lot of typing. Think of three repetitive commands you might use often and write the alias commands you would add to your .bashrc file.

alias ll = ls -l
to quikly see all the files with sizes and permissions

alias gs = git status
Check repo's version control status 

alias update='sudo apt update && sudo apt upgrade -y'
Update and upgrade your system in a single command


What is the fundamental difference between du -sh and df -h? When would you use one over the other to diagnose a “disk full” error?

df -h (disk free) shows the total used and available space on entire drive and partitions

du -sh (disk usage) Calculates how much space a specific folder and everything inside it is consuming.

to diagnose a disk full error

first df -h to see the big picture and identify which partition is at 100% capacity
second du -sh * inside that full partition to hunt down exactly which specific folders or files are hoarding space 