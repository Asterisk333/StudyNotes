# Filesystem navigation 

---
>[⬅️**back**](./README.md)

| Command | FullName       | Purpose                       |
|:--------|:---------------|:------------------------------|
| touch   | touch          | Create File                   |
| mkdir   | make directory | Create a folder               |
| cp      | copy           | Copy a file or folder         |
| mv      | move           | Move a file or folder         |
| rm      | remove         | Remove a file or folder       |
| file    | file           | Determine the type of a file  |

## Creating Files and Folders (touch, mkdir)

---
```
tryhackme@linux2:~$ touch note 
tryhackme@linux2:~$ ls            
folder1 note
```

```
tryhackme@linux2:~$ mkdir mydirectory 
tryhackme@linux2:~$ ls            
folder1 mydirectory note
```


## Removing Files and Folders (rm)

---

```
tryhackme@linux2:~$ rm note 
tryhackme@linux2:~$ ls            
folder1 mydirectory
```

```
tryhackme@linux2:~$ rm -R mydirectory 
tryhackme@linux2:~$ ls            
folder1
```


## Copying and Moving Files and Folders (cp, mv)

---

```
tryhackme@linux2:~$ cp note note2 
tryhackme@linux2:~$ ls            
folder1 note note2
```

```
tryhackme@linux2:~$ mv note2 note3 
tryhackme@linux2:~$ ls            
folder1 note note3
```


## Determining File Type

---

```
tryhackme@linux2:~$ file note 
note: ASCII text
```

---
>[⬅️**back**](./README.md)