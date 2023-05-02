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
Pod :- container wrapped with few other things is pod 
<img width="329" alt="image" src="https://user-images.githubusercontent.com/106343663/235786599-23a7e0e1-4ef6-4b33-9644-8f822425a04f.png">


