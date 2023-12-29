## Deploy Ansible AWX on KIND Cluster with Docker at Oracle Linux 8
### (via Vagrant with Virtualbox on Windows 10 host)

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

(not full customizable; access only via hostname - required changes to C:\Windows\System32\drivers\etc\hosts )

- - -
ADDIT INFO:

* installed K9s - perfect light CLI tool for control cluster

![292921477-bb2b7006-aed6-4b63-8172-3f80ff3712e2](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/e076729a-f5ca-4b6a-b90c-9e044b8298f7)


alternatively - uncomment line in Vagrantfile `kind get kubeconfig > ~/.kube/config`

and paste kubeconfig into [LENs](https://k8slens.dev/) 

![292922824-dd0eec10-fec2-4d6d-8969-314140d34ed2](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/18a17a96-03c3-442d-b6b1-6020c8cab88a)


or [Kubernetic](https://www.kubernetic.com/):

![292922979-49ef48de-b8ab-4b6b-af55-4a029cd3e1a4](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/b9abd6ee-6ca8-4132-819a-d3f942b1c6ce)
![292922837-fa726ab8-bdd5-4be1-b060-63b68feb5a88](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/66e8d900-d461-4828-a6c0-71e6c82bdac8)
![292922839-8a1b8361-4d41-4630-8ab7-75a47a32341c](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/d305344d-0b37-4c07-8c42-b11150f2c69b)


* Vagrantfile language = Ruby; when edit Vagrantfile - convert TABs into spaces (i.e. Notepad++: Edit - Blank operations - TAB to Space)

> A YAML file cannot contain tabs as indentation 

REF https://stackoverflow.com/a/19976827

REF: https://yaml.org/faq.html 

---

ENVIRONMENT: win10, vagrant, virtualbox, oracle linux 8

VM: 2 LANs for
1. for NAT access to Internet;
2. direct access to AWX via static IP 192.168.33.10

- - - 

_TODO:_
_remake to deploy via HELM_

---

START

in CMD of base host win10:

```
mkdir awx
cd awx
```

vagrant init:

REF: https://yum.oracle.com/boxes/

`vagrant init oraclelinux/8 https://oracle.github.io/vagrant-projects/boxes/oraclelinux/8.json`
```
# A `Vagrantfile` has been placed in this directory. You are now
# ready to `vagrant up` your first virtual environment! Please read
# the comments in the Vagrantfile as well as documentation on
# `vagrantup.com` for more information on using Vagrant.
```
EDIT Vagrantfile

i.e. `notepad Vagrantfile`

replace default content of **Vagrantfile** with text of [Vagrantfile](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/blob/main/Vagrantfile):

(or instead of `init` and edit *Vagrantfile* - just download [Vagrantfile](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/blob/main/Vagrantfile) from [repo](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10))

and run: 
`vagrant up`

wait for finish provisioning (about 30-40 min on VM with 2 CPU cores and 8G RAM)

example result of ready AWX:

![292921773-790bd436-3b61-40ba-a752-632183d454ed](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/84bd4835-dfa2-44da-9d25-31a1789d2cc8)
![292921787-2b1937a1-aae9-43e8-a78f-014066a03c7e](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/a2cf1740-ac7c-4d31-96d9-07da59c4673d)
![292921801-6e2a5208-f115-43c5-a3e0-02a353b414cf](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/0265c573-f6e1-4caf-9983-abcdab8af571)
![292921803-a5d0fdac-9124-451b-8ef6-01dafc885dc0](https://github.com/v-mazur-intra/ansilbe_awx_on_vm_vagrant_file_win10/assets/154795149/b02e3134-c2cf-484f-a1ee-83f9bf7bd44b)


---


[example output of provisioning](/AWX_on_kind_OL8_VboxVagrant_win10_output_example.md)


