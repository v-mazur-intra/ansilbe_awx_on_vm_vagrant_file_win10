## Vagrantfile for deploy Ansible AWX on KIND Cluster with Docker at Oracle Linux (via Vagrant&Virtualbox on Windows host)

###### [gist:](https://gist.github.com/v-mazur-intra/e3f2fbb7b473accfacd2e35bc2b0dc7c)

## Deploy AWX on KIND Cluster with Docker at Oracle Linux
### (via Vagrant&Virtualbox on Windows host)

PREFACE:

AWX https://github.com/ansible/awx 

AWX Operator: https://ansible.readthedocs.io/projects/awx-operator/en/latest/installation/basic-install.html

KIND https://kind.sigs.k8s.io/docs/user/quick-start/ 

KIND preferred via low resources consumptions and ingress options (direct access "via IP" from host)

- - -
Alternative cluster engines:

1) minikube:

REFs:

https://ansible.readthedocs.io/projects/awx-operator/en/latest/installation/creating-a-minikube-cluster-for-testing.html

https://chrisjhart.com/TLDR-AWX-Minikube-Ubuntu-2204/ 

higher resources consumption via default "double virtualization" = Docker in VM;

with config "driver=none (example "minikube start --addons=ingress,metrics-server --driver=none  --container-runtime="container.io") - very complex config especially "in rootless mode"

and also minikube has only embedded ingress (not fully cuntomizable)


2) k3s:

REF: https://github.com/kurokobo/awx-on-k3s/tree/main 

embedded ingress Traefik

(not full customizable; access only via hostname - req changes to C:\Windows\System32\drivers\etc\hosts )

- - -
ADDIT INFO:

installed K9s - perfect tool for control cluster
![292921477-bb2b7006-aed6-4b63-8172-3f80ff3712e2](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/a4514573-f2ce-4a66-b134-58b78be27157)


Vagrantfile language = Ruby; so convert TABs into spaces (i.e. Notepad++: Edit - Blank operations - TAB to Space)
!!! A YAML file cannot contain tabs as indentation 

REF https://stackoverflow.com/a/19976827

REF: https://yaml.org/faq.html 


ENV: win10, vagrant, virtualbox, oracle linux 8

VM: 2 LAN:

* NAT Internet;

* direct access static IP 192.168.33.10

- - - 

TODO:
remake to deploy via HELM

START
on base host win10:

```
mkdir awx
cd awx
```
VAGRANT UP:

REF: https://yum.oracle.com/boxes/

`vagrant init oraclelinux/8 https://oracle.github.io/vagrant-projects/boxes/oraclelinux/8.json`
```
# A `Vagrantfile` has been placed in this directory. You are now
# ready to `vagrant up` your first virtual environment! Please read
# the comments in the Vagrantfile as well as documentation on
# `vagrantup.com` for more information on using Vagrant.
```
EDIT Vagrantfile
and replace default content of **Vagrantfile** with text of latest ver of _Vagrantfile_ from [repo](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10))


