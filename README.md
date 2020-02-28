Tech Test
==============
# Tech Test Readme
The following is a recount of my efforts towards the deployment of an automated version of the tech test using minikube hosted on ubuntu 16.04.

# History

## Version 1
This version was done by hand in configuration of service was done with referencing the kubernetes documentation for correct tag usage. This was done with kubectl create on the command line af
ter I used docker-compose to test the containers and give them a once over.

## Version 2
This was created with ansible to automate the creation of the deployment files with kubectl being used for the deployment into the cluster.

## Version 3
This is like version two however I used ansible to install the deployment files to the cluster.

# Requirements

1. minikube running on the host
2. kubectl installed on the host
3. Update the user_name variable in group_var/all/all.yml
4. Update the inventory/host to the host in question
5. Minikube cluster has the ingress addon enabled

# Usage

ansible-playbook -i inventory/host site.yml
