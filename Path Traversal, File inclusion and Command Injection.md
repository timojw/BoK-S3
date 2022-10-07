## Body of Knowledge: ##
__Path Traversal, File Inclusion, Command Injection__

__RELEVANCE__


__STARTING POINT__
Before this assignment I have had zero to no experience with these subjects and I'm going into it with only the knowledge that a website is a bunch of files. I learned that during my previous semesters.

__APPROACH__
My approach for this assignment will be to search for what the different attacks are and how to prevent them, I will do this using links in canvas pages but also looking for some new sources online. After this I will try to apply all of these techniques in a DVWA website.

__EXECUTION__
**What is path traversal and how does it work?**
Path traversal also known as directorty traversal aims to access files and directories that are stored outside the root folder. You do this by changing variables that reference files (../). Using this method it could be possible to access the application source code or configuration files.

Using path traversal I was able to access the password file (/etc/passwd) in the root folder. As you can see below I needed to go back quite far from where I started. Later I found that just going to page=/etc/passwd also worked.
![](/media/file%20inclusion2.png)
![](/media/file%20inclusion3.png)
Using path traversal I was able to access the fourth hidden file. This was done by editing the webadress in a certain way to show another file as seen below.
![](/media/file%20inclusion.png)
I also was able to access the page=/proc/version file which grants access to the operating system details of the victem.
![](/media/file%20inclusion4.png)
Later I found this funny file which is located one directory down so I had to include 2 times ../ before finding it.
![](/media/file%20inclusion6.png)
To make your application less vulnerable to these sort of attacks it would be wise not to work with user input when the system is calling for certain stored files. You could also use ID's in the structure of the application. To make sure that the hacker can not supply all parts of the code, surround it with your path code. There are more options to defend against such attacks.

**What is remote file inclusion and how does it work?**
Remote file inclusion is an attack targeting vulnerabilities in web applications that dynamically reference external scripts. The attacker's goal is to exploit the referencing function in an application to upload malware from a remote URL located within a different domain.

**What is command injection and how does it work?**
Command injection is an attack in which the goal is execution of commands on the host operating system. Command injection attacks are possible when an application passes unsafe user supplied data to a system shell. Command injection attacks are possible largely due to insufficient input validation.

As you see below I was able to add more commands after the ip address like hostname which provides the operating system for the application. Alteratively you could use the && symbol instead of the ; between commands.
![](/media/commandinjection2.png)
Another way of using command injection is the ls command which shows you what files are located in the current directory. You could also show it for other directories as shown below. It could be very usefull to combine with path traversal cause this was you know what files are where.
![](/media/commandinjection.png)

**How are path traversal, remote file inclusion and command injection related?**
After getting to know these vulnerabilities I would say that all of them are in some way related to browsing and accessing the files for the website. A path traversal vulnerability allows an attacker to access files on your web server to which they should not have access. Remote file inclusion is basically the same only the big difference is the ability to execute the source codes that are not saved in interpretable files. And command injection can be used to navigate the files as well by using ls or other commands.  

__AFTERTHOUGHTS__
After only doing some very basic excersises for these subjects I'm left wondering what else is possible and excited to do some more in the future, but due to my thight schedule I have to keep going for now.

__SOURCES__
- [Path Traversal](https://owasp.org/www-community/attacks/Path_Traversal)
- [Remote file inclusion (RFI)](https://www.imperva.com/learn/application-security/rfi-remote-file-inclusion/)
- [Command Injection](https://owasp.org/www-community/attacks/Command_Injection)