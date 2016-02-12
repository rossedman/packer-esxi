# Packer VMWare ESXi
This is a demo packer template for ESXi. A full tutorial is [here](http://keyboardonfire.com/devops/vsphere-packer-kickstart/).

## Build

To build this template make sure you have an ESXi iso downloaded and installed in the `/isos` directory. You also must have Vagrant/VMWare plugin installed as well as VMWare Fusion or VMWare Workstation. 

```
$ packer build packer.json
$ vagrant add yourname/esxi builds/nameofbuild.box
$ vagrant up
```
