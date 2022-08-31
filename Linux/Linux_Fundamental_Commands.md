# Linux fundamental commands

---

| Simple Commands | Description                                            |
|:----------------|:-------------------------------------------------------|
| echo            | Output any text that we provide                        |
| whoami          | Find out what user we're currently logged in as!       |
| ls              | listing <br><br> Use --all / -a <br> to show all files |
| cd              | change directory                                       |
| cat             | concatenate<br> view content of files                  |
| pwd             | print working directory                                |

## find

---
If we remember the filename, we can simply use  

```find -name passwords.txt```  

where the command will look through every folder in our current directory for that specific file like so:  
  
```
tryhackme@linux1:~$ find -name passwords.txt 
./folder1/passwords.txt
tryhackme@linux1:~$
```  

We will construct a command such as find -name *.txt . Where "Find" has been able to find every .txt file and has then given us the location of each one:

```
tryhackme@linux1:~$ find -name *.txt 
./folder1/passwords.txt  
./Documents/todo.txt  
tryhackme@linux1:~$
```

## grep

---
Another great utility that is a great one to learn about is the use of ```grep```  
The grep command allows us to search the contents of files for specific values that we are looking for.

```
tryhackme@linux1:~$ wc -l access.log
244 access.log
tryhackme@linux1:~$
```

We can use grep to search the entire contents of this file for any entries of the value that we are searching for.  
Going with the example of a web server's access log, we want to see everything that the IP address "81.143.211.90" has visited  
```
tryhackme@linux1:~$ grep "81.143.211.90" access.log
81.143.211.90 - - [25/Mar/2021:11:17 + 0000] "GET / HTTP/1.1" 200 417 "-" "Mozilla/5.0 (Linux; Android 7.0; Moto G(4))"  
tryhackme@linux1:~$
```

## symbols and Operators

---
| Symbol/Operator   | Description                                                                                                                                             |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| &                 | This operator allows you to run commands in the background of your  <br/> terminal.                                                                     |
| &&                | This operator allows you to combine multiple commands together in one  <br/> line of your terminal.                                                     |
| ">"               | This operator is a redirector - meaning that we can take the output from a  <br/> command (such as using cat to output a file) and direct it elsewhere. |
| ">>"              | This operator does the same function of the > operator but appends the  <br/> output rather than replacing (meaning nothing is overwritten).            |

### Operator "&"

This operator allows us to execute commands in the background.  
For example, let's say we want to copy a large file. This will obviously  
take quite a long time and will leave us unable to do anything else until the file  
successfully copies.

The "&" shell operator allows us to execute a command and have it run in the background (such as this file copy) allowing us to do other things!



### Operator "&&"

This shell operator is a bit misleading in the sense of how familiar is to its partner "&".  
Unlike the "&" operator, we can use "&&" to make a list of commands to run for example
```
command1 && command2
```
. However, it's worth noting that command2 will only run if command1 was successful.

### Operator ">"

This operator is what's known as an output redirector. What this essentially means is  
that we take the output from a command we run and send that output to somewhere else.


A great example of this is redirecting the output of the echo command that we learned  
in Task 4. Of course, running something such as echo howdy will return "howdy" back  
tour terminal — that isn't super useful. What we can do instead, is redirect "howdy" to  
something such as a new file!

Let's say we wanted to create a file named "welcome" with the message "hey". We can run
```
echo hey > welcome
```
where we want the file created with the contents "hey" like so:
```
tryhackme@linux1:~$ echo hey > welcome
```

```
tryhackme@linux1:~$ cat welcome 
hey
```

### Operator ">>"

This operator is also an output redirector like in the previous operator (>) we  
discussed. However, what makes this operator different is that rather than overwriting  
any contents within a file, for example, it instead just puts the output at the end.

Following on with our previous example where we have the file "welcome" that has the  
contents of "hey". If were to use echo to add "hello" to the file using the > operator,  
the file will now only have "hello" and not "hey".

The >> operator allows to append the output to the bottom of the file — rather than  
replacing the contents like so:

```
tryhackme@linux1:~$ echo hello >> welcome
```

```
tryhackme@linux1:~$ cat welcome 
hey 
hello
```

>[⬅️**back**](./README.md)