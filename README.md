This repository is created as part of my Kubernetes learning journey.

As we know all know Kubernetes is a container Orchastration platform. What is the real requirement of container orchestration?
K8 has been introduced to eliminate major drawbacks we faced from container platfroms like docker.
The main issues in Container platforms are :
   1) Single Host and short life of containers-->Containers are empherical and may have short life
   2) No Auto Healing--> No auto recovery of containers when container become dead 
   3) No Autoscaling --> If customer traffic increases drastically there is no load balancing provision or scaling
   4) Docker has less enterprise features -->docker platform don't have load balancing,firewall, autoscaling etc(not referring to docker swarm)

Kubernetes Architecture:-
Kubernetes is based on Master(control plane) and Worker node(Data plane) cluster.As the name suggest master node controls all the cluster and it;s the worker nodes who actually do the work and host the Pods.
The smallest identity in K8 is Pod ( In docker the smallest identity is container)

Architecture:-

<img width="331" alt="image" src="https://user-images.githubusercontent.com/106343663/235789298-befad692-53b2-48d7-877f-e24e642ff7c2.png">

(image taken from internet)

Kubernetes worker node(data plane) has:-

   -pod :-Container wrapped in something else too                                
   -kubelet running:-responsible for pod running                           
   -Kubeproxy :-provides networking,IP and default load balancing                           
   -container runtime:-is responsible for container to run.                                                                  
       ( K8 we can use containerd etc)
   
Kubernetes master node(control pane) has :-                                           
   -API server:- Entry point for K8 cluster                                                      
   -Scheduler:- acts on scheduling                                                                            
   -Controller Manager:- manages controllers.(ex:-replica sets controllers)
        (cloud controller manager also there:-used when k8 is deployed in EKS/AKS etc )                       
   -etcd:-Key value storage.Storage current value of entire cluster.Backup etc stored
    




