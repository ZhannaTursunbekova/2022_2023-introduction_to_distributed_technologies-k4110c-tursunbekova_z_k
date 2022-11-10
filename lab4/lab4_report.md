University: [ITMO University](https://itmo.ru/ru/) <br />
Faculty: [FICT](https://fict.itmo.ru) <br />
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br />
Year: 2022/2023 <br />
Group: K4110c <br />
Author: Tursunbekova Zhanna Khasanovna <br />
Lab: Lab4 <br />
Date of create:   10.11.2022 <br />
Date of finished: 19.11.2022 <br />

# Name of lab: Networking in Minikube, CNI and CoreDNS

### 1. Starting minikube, install the CNI=calico plugin and the Multi-Node Clusters mode at the same time, for this lab you need to deploy 2 nodes.
![My Image](images/image1.png)

### 2. Check the operation of the Calico CNI plugin and the number of nodes, attach the results of the check to the report.
![My Image](images/image2.png)

### 3. To test Calico's work, we will try one of the functions called IPAM Plugin. 
###    To check the IPAM mode, you need to specify a label for previously launched nodes based on a rack or geographic location (your choice).
![My Image](images/image3.png)

### 4. Develop a manifest for Calico that assign IP addresses to "pods" based on labels.
![My Image](images/image4.png)

![My Image](images/image5.png)

### 5. Create a deployment with 2 replicas and pass variables to these replicas: REACT_APP_USERNAME, REACT_APP_COMPANY_NAME.
![My Image](images/image6.png)

![My Image](images/image7.png)

![My Image](images/image8.png)

### 6. Create a service through which you will have access to these pods. The choice of service type is up to you.
![My Image](images/image9.png)

### 7. Run minikube in port forwarding mode and connect to your containers through a web browser.
![My Image](images/image10.png)

![My Image](images/image11.png)

### 8. Using kubectl exec, go to any pod and try to ping the other pod, the results of the pings should be attached to the report.
![My Image](images/image12.png)
