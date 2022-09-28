# importatnt files

## Vagrantfile 
| line                               | use                                                      |
|------------------------------------|----------------------------------------------------------|
|                                    | general config                                           |
| config.vm.box                      | = "ubuntu/xenial64"                                      |
| config.vm.hostname                 | = 'web-dev'                                              |
| config.vm.provision 'shell', path: | 'provision.sh'                                           |
| config.vm.network                  | 'forwarded_port', guest: 20, host: 2020, id: 'nginx-cnt' |


---

## provision.sh
| line | use                    |
|------|------------------------|
|      | install addon software |