# openshift
Script to beginer

Enviroment REHL7.9
install:

# Setup Enviroment
```sh
sudo yum install qemu-kvm*

sudo yum group install --with-optional \
virtualization-host-environment

sudo systemctl enable --now libvirtd

sudo usermod -a -G libvirt seth

newgrp - libvirt

groups

```

# Docker & KVM
```sh
curl --location \
https://github.com/docker/machine/releases/download/v0.16.1/docker-machine-Linux-`uname -i` > \
~/Downloads/docker-machine

chmod +x ~/Downloads/docker-machine

sudo mv ~/Downloads/docker-machine /usr/local/bin/

curl --location \
https://github.com/dhiltgen/docker-machine-kvm/releases/download/v0.10.0/docker-machine-driver-kvm-centos7 > \
~/Downloads/docker-machine-driver-kvm

chmod +x ~/Downloaders/docker-machine-driver-kvm

sudo mv ~/Downloaders/docker-machine-driver-kvm /usr/local/bin/
```


# Download minishift
```sh
export VER="1.34.3"
curl -L https://github.com/minishift/minishift/releases/download/v$VER/minishift-$VER-linux-amd64.tgz -o minishift-$VER-linux-amd64.tgz
tar xvf minishift-$VER-linux-amd64.tgz

sudo mv minishift-$VER-linux-amd64/minishift /usr/local/bin 

minishift start

```

