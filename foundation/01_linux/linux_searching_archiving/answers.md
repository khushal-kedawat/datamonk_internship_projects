1. Getting Help: There are three main ways to get help: man, --help, and help. Why do you think Linux has these different options instead of just one? In what specific scenario would help be the only correct choice?

man : it is short for manual man pages are comprehensive, system-wide documentation for executable programs, system calls, and configuration files
it is used for a deep dive allows user to scroll , search , read detailed descriptions of every single flag,

--help: it is not a standalone command but a flag passed to a specific program it prints a quick, concise summary directly to your terminal without opening a new reading window


help: it is specifically for shell built-ins shell  has several commands directly into its source code rather than existing as separate executable files on hard drive so they do not have their own man pages thus in such cases help command is usefull

The only time help is the strictly correct  choice is when you need information on a shell built-in command


2. Searching Files: What is the key difference between using ls | grep ".txt" and find . -name "*.txt"? When would one be more powerful than the other?

The core difference between these two commands comes down to scope and purpose: ls | grep is a quick text-filtering hack that only looks at your immediate surroundings, while find is a purpose-built search engine that actively traverses your file system.

find is more powerful when need to search subdirectories , need advance filters 
ls is a better option when there is a massive flat directory and want to quick filter to find text and bring it on screen


3. The document shows how ps aux | grep chrome can filter running processes. How could you use this same piping concept with the history command to find a specific command you ran last week?

this can be done by taking the output of the history command and giving it to the grep 
like history | grep "command"
as history prints a list of number of commands which were previously executed
instead of printing them on screen pipe will intercept them and funnels it forward
grep will recieve the list and acts as a filter only allowing specific search term in this case the command to pass and print its output on screen

4. A developer asks you to send them your project files. Why might you choose to send a .tar.gz archive instead of a .zip file if you know the other developer is also using Linux? What security risk should you be aware of before extracting an archive you received from an unknown source?

.tar.gz is a better option over .zip as it preserveres system metadata like file permission , links , properties which might get corrupted via .zip also 
.tar.gz uses compression which reduces the size large code files anyways before extracing an archive from unknown sources because of directory traversal attacks which can silently overwrite sensitive system or files outside the intended extraction folder