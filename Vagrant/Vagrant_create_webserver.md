# Create Vagrant git Repo
## installation of NGINX

---

### initial installation

---
/home/ubuntu ->  
```
$ mkdir nginx  
$ cd nginx  
$ vagrant init ubuntu/xenial64 --minimal  
$ cat vagrantfile  
```
![cat-vagrantfile](images/Vgrtant_GitRepo_01.png)

### install packages

---
/home/ubuntu ->
```
$ nano provision.sh
```
![cat-provision.sh](images/Vgrtant_GitRepo_02.png)  
these commands are ran eveytime the vm starts up.

```
$ nano vagrantfile
```
Line 3 to enable the provision.sh file

```
$ vagrant provision
```

### Port forwarding

---

/home/ubuntu ->
```
$ nano vagrantfile
```  
add line 4

```
$ vagrant reload
```  
to reload the content of vagrantfile

### create shared directory

---

```
$ vagrant ssh
$ sudo mkdir /vagrant/www
$ nano /vagrant/www/index.html
```  
![cat-provision.sh](images/Vgrtant_GitRepo_03.png)  
```
$ sudo rm -rf /var/www/html
$ sudo ln -s /vagrant/www /var/www/html
exit
$ nano provision.sh
```  
![nano-provision.sh](images/Vgrtant_GitRepo_04.png)  
```
$ vagrant reload
```  
>[⬅️**back**](../README.md)








