#######################################################################################
#
#CONTAINER DEMO RUNBOOK
#
#######################################################################################
#
##Environment
#
*compute: 10.226.224.238 uname:ubuntu/passwd:pureuser
*storage: 10.226.224.180/flashblade
*storage: 10.226.224.110/flasharray (iscsi)
*storage: 10.226.224.132/flasharray (iscsi)

#######################################################################################

Use this playbook to demo PSO
This will install PSO on a kubernetes cluster. 
The demo environment uses kubernetes 1.14 and includes helm and tiller.  
#
Tasks: 
*Install PSO from scratch using Helm
*Create a container with persistant storage 
*Upgrade the instance of PSO to add a second array. 
*Upgrade the instance of PSO to include the use of labels
*Create a container with persistant storage and assign volume to an array using labels.
*Create a container with persistant storage on flashblade
*Log into a container and view the attached storage volume. 
