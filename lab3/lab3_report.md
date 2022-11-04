University: [ITMO University](https://itmo.ru/ru/) <br />
Faculty: [FICT](https://fict.itmo.ru) <br />
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <br />
Year: 2022/2023 <br />
Group: K4110c <br />
Author: Tursunbekova Zhanna Khasanovna <br />
Lab: Lab3 <br />
Date of create:   04.11.2022 <br />
Date of finished: 05.11.2022 <br />

# Name of lab: Certificates and Secrets in Minikube, secure data storage

### 1. Create configMap with variables: REACT_APP_ USERNAME, REACT_APP_ COMPANY NAME.
![My Image](images/image1.png)

### 2. Result.
![My Image](images/image2.png)

### 3. Create a replicaSet with 2 replicas and use configMap to pass the variables REACT_APP_USERNAME, REACT_APP_COMPANY_NAME.
![My Image](images/image3.png)

### 4. Result.
![My Image](images/image4.png)

### 5. Enable "minikube add-ons enable ingress" and generate TLS certificate, import certificate into minikube.
![My Image](images/image5.png)

![My Image](images/image6.png)

![My Image](images/image7.png)

### 6. Create an ingress in minikube with certificate, FQDN and name of the service.
#### Service
![My Image](images/image8.png)
#### Ingress
![My Image](images/image9.png)

![My Image](images/image10.png)

### 7. In hosts file, write the FQDN and IP address of your ingress and try to go to the FQDN name in the browser.
![My Image](images/image11.png)

### 8. Log in to the web application with your FQDN using HTTPS and check the certificate.
![My Image](images/image12.png)
