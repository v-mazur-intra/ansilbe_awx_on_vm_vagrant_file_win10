# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "oraclelinux/8"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://oracle.github.io/vagrant-projects/boxes/oraclelinux/8.json"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080
###ADD:
  config.vm.network "forwarded_port", guest: 80, host: 80, host_ip: "127.0.0.1"
  config.vm.network "forwarded_port", guest: 443, host: 443, host_ip: "127.0.0.1"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
###UNCOMMENT:
  config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Disable the default share of the current code directory. Doing this
  # provides improved isolation between the vagrant box and your host
  # by making sure your Vagrantfile isn't accessable to the vagrant box.
  # If you use this you may want to enable additional shared subfolders as
  # shown above.
###COMMENT:
  # config.vm.synced_folder ".", "/vagrant", disabled: true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
##EDIT:
  config.vm.provider "virtualbox" do |vb|
  ## Display the VirtualBox GUI when booting the machine
  ## for control booting
    vb.gui = true
  ## Customize the amount of memory and cpu on the VM:
    #vb.memory = 6144 #minimum 
    ## optimum 8192
    vb.memory = 8192
    # vb.cpus = 2 #minimum
    vb.cpus = 3
    ## optimum 4
    vb.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
    ## REF: https://github.com/hashicorp/vagrant/issues/11726
  end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
  ## do not use expr: config.vm.provision "shell", inline: <<-SHELL
  ## due to privileged (boolean) - Specifies whether to execute the shell script as a privileged user or not (sudo). By default this is "true".
  ## REF: https://developer.hashicorp.com/vagrant/docs/provisioning/shell#privileged
  ## ref: https://stackoverflow.com/a/22556979
  ##
  ## SWAP
  # # REF: https://discuss.kubernetes.io/t/swap-off-why-is-it-necessary/6879/2
  # # disable swap in order for the kubelet to work properly.
  # ## disable swap on startup in /etc/fstab #does not work in vagrantfile 
  # #sudo sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab
  # free -h
  # swapon -s  
  config.vm.provision "shell", inline: "swapoff -a; free -h",
    run: "always"
  $script = <<-SCRIPT
    sudo dnf -y update
    sudo dnf -y install oracle-epel-release-el8
    sudo dnf -y update
    ## OPTIONAL:
    sudo dnf -y install PackageKit-command-not-found bash-completion mc htop tcpdump screen iptraf-ng iftop git curl
    sudo dnf install -y fuse-overlayfs # REF https://docs.docker.com/engine/security/rootless/ 
    sudo timedatectl set-timezone Europe/Kyiv
    ##disable ipv6 nmcli via err with docker image dowload with IPv6
    sudo nmcli con show
    sudo nmcli conn modify "System eth0" ipv6.method "disabled"
    sudo nmcli connection up "System eth0"
    ##disable DNS via DHCP (for docker image download)
    cat /etc/resolv.conf
    sudo nmcli conn modify "System eth0" ipv4.ignore-auto-dns yes
    sudo nmcli conn modify "System eth0" ipv4.dns  "8.8.8.8,1.1.1.1"
    sudo systemctl restart NetworkManager
    sleep 5
    cat /etc/resolv.conf
  ## Docker:
  ## ADDIT REFs:
  ## https://badtry.net/docker-tutorial-dlia-novichkov-rassmatrivaiem-docker-tak-iesli-by-on-byl-ighrovoi-pristavkoi/
  ## https://chrisjhart.com/TLDR-Docker-Ubuntu-2204/
  ## https://docs.docker.com/engine/install/centos/
    sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
    sudo dnf -y update
    sudo dnf -y install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    sudo usermod -aG docker $USER
    #usermod -aG docker vagrant
    #newgrp docker # to activate the changes to groups (without sudo !!!)
    #newgrp - docker # to activate the changes to groups (without sudo !!!)
    sudo groups $USER
    id
    sudo systemctl start docker.service
    sudo systemctl enable docker.service
    sudo systemctl enable containerd.service
  SCRIPT
  config.vm.provision "shell", inline: $script, privileged: false
  ## FOR REINITIALIZE SHELL SESSION 
  ## REBOOT - required;
  ## without "reboot" does not work docker rootless container)
  ## REF: https://docs.docker.com/engine/install/linux-postinstall/ 
  ## "newgrp docker" does not work
  config.vm.provision "shell", reboot: true, inline: <<-SHELL
  echo "rebooting!"
  SHELL
  $script2 = <<-SCRIPT
    ## OPTIONAL CHECK:
    echo "script2"
    sudo systemctl status docker.service
    docker --version
    docker run hello-world
    docker ps -a
    docker stop $(docker ps -a -q)   # stop all containers
    docker rm $(docker ps -a -q)     # remove all containers
    docker image list
    # docker image inspect hello-world:latest
    docker image rm hello-world:latest
    ## KIND:
    ## REF: https://kind.sigs.k8s.io/docs/user/quick-start#installing-from-release-binaries
    ## install:
    # echo "install KIND"
    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.20.0/kind-linux-amd64
    chmod +x ./kind
    ## sudo mv ./kind /usr/local/bin/kind
    sudo mv ./kind /usr/bin/kind
    ## install in default BIN (/usr/bin) location (not proposed by installer - /usr/local/bin/)
    ## due to ERR on RHEL 8.8 and other host systems using the none driver
    ## that do not include /usr/local/bin by default 
    ## alternatively you can can add /usr/local/bin to the secure_path used by sudo
    ## REF: https://github.com/kubernetes/minikube/issues/16783#issuecomment-1779227673
    ## REF2: https://codingshower.com/how-to-set-path-environment-variable-for-sudo-commands/
    ## alias sudo='sudo env PATH=$PATH' #does not help 
    kind --version
    echo "source <(kind completion bash)" >> ~/.bashrc
    source ~/.bashrc
    ## kubectl:
    ## REF: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    #sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
    sudo install -o root -g root -m 0755 kubectl /usr/bin/kubectl
    ## login -f $USER
    ## exec su -l $USER
    ## bash --login $USER
    kubectl version --client
    echo "source <(kubectl completion bash)" >> ~/.bashrc
    source ~/.bashrc
    # K9S
    # REF : https://github.com/derailed/k9s
    wget https://github.com/derailed/k9s/releases/download/v0.29.1/k9s_linux_amd64.rpm
    sudo rpm -Uvh k9s_linux_amd64.rpm
    k9s info
    # FOR WORKING INGRESS - change config 
    # (alternative for last common option - redirect via kubectl, i.e. "kubectl -n awx port-forward svc/awx-service --address 0.0.0.0 8080:80")
    # REFs:
    # https://kind.sigs.k8s.io/docs/user/ingress/
    # https://kubernetes.io/docs/concepts/services-networking/ingress/
    # https://kk-shichao.medium.com/expose-service-using-nginx-ingress-in-kind-cluster-from-wsl2-14492e153e99
    # https://dustinspecker.com/posts/test-ingress-in-kind/
    #  
    # !!! A YAML file cannot contain tabs as indentation # REF https://stackoverflow.com/a/19976827
    # REF: https://yaml.org/faq.html 
    cat <<-EOF > config.yaml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
networking:
  # WARNING: It is _strongly_ recommended that you keep this the default
  # (127.0.0.1) for security reasons. However it is possible to change this.
  apiServerAddress: "192.168.33.10"
  ## CHANGED FOR DIRECT ACCESS to API of CLUSTER
  ## - i.e. manage cluster via LENS (https://k8slens.dev/) or Kubernetic Desktop (non free! https://www.kubernetic.com/) from Windows
  # By default the API server listens on a random open port.
  # You may choose a specific port but probably don't need to in most cases.
  # Using a random port makes it easier to spin up multiple clusters.
  apiServerPort: 6443
nodes:
- role: control-plane
  kubeadmConfigPatches:
  - |
    kind: InitConfiguration
    nodeRegistration:
      kubeletExtraArgs:
        node-labels: "ingress-ready=true"
  extraPortMappings:
  - containerPort: 80
    hostPort: 80
    protocol: TCP
  - containerPort: 443
    hostPort: 443
    protocol: TCP
EOF
    ## for working EOF - need to delete the tabs/spaces in front of the "EOF"
    ## REF: https://stackoverflow.com/a/74862153
    ##
    ## KIND create cluster with config
    kind create cluster --config=config.yaml --wait 5m
    ## wait for cluster creation finished
    ## check if kubeconfig in default locations; or export 
    ## DEV [[ -f ~/.kube/config ]] || kind get kubeconfig > ~/.kube/config
    ## mkdir ~/.kube
    ## echo "cat ~/.kube/config"
    ## cat ~/.kube/config
    ## OR
    ## kind get kubeconfig > ~/.kube/config
    ## echo "This config may be used to connect to cluster with LENS or Kubernetic"
    ##
    ## deploy metrics server for CPU amd RAM consumption monitoring (i.e. "kubectl top nodes" or k9s)
    ## neeed patch (metric-server container, you need to add argument  --kubelet-insecure-tls)
    ## REF:
    ## https://gist.github.com/sanketsudake/a089e691286bf2189bfedf295222bd43
    mkdir metrics-server
    cat <<-EOF >metrics-server/kustomization.yaml
resources:
  - https://github.com/kubernetes-sigs/metrics-server/releases/download/v0.6.4/components.yaml
    ## CHECK latest here https://github.com/kubernetes-sigs/metrics-server/releases
patches:
  - patch: |-
      - op: add
        path: /spec/template/spec/containers/0/args/-
        value: --kubelet-insecure-tls
    target:
      version: v1
      kind: Deployment
      name: metrics-server
      namespace: kube-system
EOF
    kubectl apply -k metrics-server/
    ## WAIT for metrics-server become ready
    kubectl wait --namespace kube-system --for=condition=ready pod --selector=k8s-app=metrics-server --timeout=180s
    # wait for metrics-server ready
    sleep 60
    # check metrics-server working
    kubectl top nodes
    kubectl top pod -A
    ##TODO 
    # helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
    # helm repo update
    # helm upgrade --install --set args={--kubelet-insecure-tls} metrics-server metrics-server/metrics-server --namespace kube-system
    ## DEPLOY AWX via AWX Operator
    ## REFs:
    ## https://ansible.readthedocs.io/projects/awx-operator/en/latest/installation/basic-install.html
    ## https://chrisjhart.com/TLDR-AWX-Minikube-Ubuntu-2204/
    mkdir awx
    # Create kustomization file
    cat <<EOF > awx/kustomization.yaml
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
resources:
  # Find the latest tag here: https://github.com/ansible/awx-operator/releases
  - github.com/ansible/awx-operator/config/default?ref=2.9.0
  #- awx.yaml
# Set the image tags to match the git version from above
images:
  - name: quay.io/ansible/awx-operator
    newTag: 2.9.0
# Specify a custom namespace in which to install AWX
namespace: awx
EOF
    ## DEPLOY AWX Operator
    kubectl apply -k awx/
    ## WAIT for awx-operator become ready
    kubectl wait --namespace awx --for=condition=ready pod --selector=control-plane=controller-manager --timeout=5m
    sleep 60
    # EDIT: kustomization file (add - awx.yaml)
    cat <<EOF > awx/kustomization.yaml
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
resources:
  # Find the latest tag here: https://github.com/ansible/awx-operator/releases
  - github.com/ansible/awx-operator/config/default?ref=2.9.0
  - awx.yaml
# Set the image tags to match the git version from above
images:
  - name: quay.io/ansible/awx-operator
    newTag: 2.9.0
# Specify a custom namespace in which to install AWX
namespace: awx
EOF
    # Create AWX resource file
    cat <<EOF > awx/awx.yaml
---
apiVersion: awx.ansible.com/v1beta1
kind: AWX
metadata:
  name: awx
spec:
  service_type: nodeport
EOF
    ## DEPLOY AWX
    kubectl apply -k awx/
    ## WAIT for awx-operator become ready
    ## WAIT FOR DATABASE MIRGATION FINISHED
    sleep 1200 # about 20m on 3 cpu 8 ram
    kubectl wait --namespace awx --for=condition=ready pod --selector=app.kubernetes.io/name=awx-web --timeout=1200s
    ## DEPLOY INGRESS
    ## (alternative to kubectl -n awx port-forward svc/awx-service --address 0.0.0.0 8080:80)
    kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
    kubectl wait --namespace ingress-nginx --for=condition=ready pod --selector=app.kubernetes.io/component=controller --timeout=180s
    sleep 60
    cat <<-EOF > nginx-ingress.yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: ingress-for-awx
  namespace: awx
  annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /
spec:
  rules:
  - http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: awx-service
            port:
              number: 80
EOF
    kubectl apply --filename nginx-ingress.yaml
    kubectl describe ingress -n awx
    sleep 60
    ##check WEB locally
    curl http://192.168.33.10/
    #
    curl https://192.168.33.10/ -k
    echo "WEB interface of AWX is available from the host machine"
    echo "http://192.168.33.10/"
    echo "OR"
    echo "https://192.168.33.10/"
    # Get the password for the AWX admin user (default username is "admin") to log into the AWX web
    # interface.
    echo "The password for the AWX admin user (default username is admin)"  
    kubectl get secret -n awx awx-admin-password -o jsonpath="{.data.password}" | base64 --decode; echo
    echo "FINISH"
    SCRIPT
    config.vm.provision "shell", inline: $script2, privileged: false
    ###
    ## ADDITIONAL NOTES:
    ## kubectl config set-context --current --namespace=awx
    ## after reboot - cluster auto starts (vs if use driver podmadn - then cluster does not auto start!)
    ## after "kind delete cluster" - better delete all files at home (rm -rf ~/*) and reboot before starting new cluster
  ##SHELL 
end
