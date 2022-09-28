# Basics

## Install vagrant  

---

```
$ sudo apt update 
$ sudo apt install virtualbox

$ curl -O https://releases.hashicorp.com/vagrant/2.2.9/vagrant_2.2.9_x86_64.deb
$ sudo apt install ./vagrant_2.2.9_x86_64.deb
```


## carete disto
| Command                    | Use                                        |
|----------------------------|--------------------------------------------|
| vagrant init XXX --minimal | initialise  distro XXX in a minimal format |
| vagrant ssh                | connect to Container                       |
| vagrant halt               | stop the container                         |
| vagrant up                 | start the container                        |
| vagrant destroy -f         | loescht vm ohne vagant file                |


Vagrant is used to create a vm on a vm --> containers  

## files
>[🔎 **more**](Vagrant_Importat_Files.md)

| name         | use                                                                   |
|--------------|-----------------------------------------------------------------------|
| Vagrantfile  | is used for basic configuration <br/>  config.vm.hostname = 'web-dev' |
| provision.sh | is used for start up commands                                         |

---

>[⬅️**back**](../README.md)