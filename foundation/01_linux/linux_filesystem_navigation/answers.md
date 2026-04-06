Why is the rm -r command considered dangerous? What simple precaution can you take before running it to avoid deleting the wrong directory?

this command is dangerous because it recursively deletes directories and its content permanently
to avoid deleting the wrong directory always ls before ans check for the right directory also use the -i option using which the system will first ask for confirmation before deleting


Think of a real-world scenario where you would need to view a very large log file on a server. Would you use cat or less? Why?

cat will dump down the entire file which will make it very difficult to read through it also if a file is very big it might freeze the terminal so
less is a better way to read a very large log file as it does not dumps down everything at one go instead loads a specific chunk also it allows scrolling and keyword searching and is more memory efficient.



How can using wildcards (* and ?) significantly speed up your workflow when you need to move, copy, or delete a specific subset of files in a directory with hundreds of items?

they speed up workflow as they allow to target multiple files at once without typing each one of them

 What is the difference between an absolute path (e.g., /home/user/project) and a relative path (e.g., ../project)? When is it better to use one over the other?

 Absolute Path is the exact location starting from the root of the computer. It works no matter where you currently are

 Relative Path is the location starting from your current folder it only works if you are in the correct starting position

 Using Relative Path is better when working with websites and code repositories as this makes your code portable, ensuring links don't break if you share the folder or move it to a different computer.

 Using Absoulte Path is good when working with cron jobs or global config files as you need absolute certainty of a file's location, regardless of where the script is run from.