# vagrantkube 

This is designed to be an easy way to start running with Kubernetes in minutes 

Steps for install and running. Prerequisite is that Vagrant must be installed https://www.vagrantup.com/downloads.html 

1) Clone the repo, `cd` into folder

2) Open the Vagrantfile - validate that the names of the Nodes and IP Addresses are suitable for your environment 

3) In the folder where the Vagrantfile is, type `vagrant up` . This will begin the creation of the environment 
    You can also use `vagrant up <nodename>` to boot a particular node listed in your Vagrant environment 
    
4) SSH into the manager node - using the Vagrantfile included, type `vagrant ssh kube11` . Substitute the appropriate Kubernetes master used in your environment. This will be the node that uses `k8smgrinst.sh` located in the Vagrantfile, located underneath kube11 in this example. You will see `kube11.vm.provision :shell, path: "k8smgrinst.sh"` 

5) Type in `kubectl get nodes` into the kube11 node you ssh'd into - make sure all nodes have joined 

6) Enjoy! 
