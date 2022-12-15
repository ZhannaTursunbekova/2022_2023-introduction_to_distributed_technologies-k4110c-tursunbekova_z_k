## Что такое docker, rkt, containerd? Как работает контейнеризация в одной из выбранных систем на выбор? (Полное объяснение с работой сетей и т.д) <br />

**Docker** is an open platform for developing, shipping, and running applications. 
Docker enables separate applications from infrastructure and deliver software quickly. 

**Rocket** is a Docker alternative designed for the server environment with the most stringent security and performance requirements. 
rkt is focused on the App Container definition, a set of simple and initial instructions for capturing containers.

**containerd** is a daemon for managing the lifecycle of a container, 
from downloading and unpacking a container image to executing and monitoring a container.

### Docker architecture
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, 
which does building, running, and distributing Docker containers. 
The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. 
Another Docker client is Docker Compose, that works with applications consisting of a set of containers.
![My Image](architecture.svg)

Docker uses a technology called namespaces to provide the isolated workspace called the container. 
When running a container, Docker creates a set of namespaces for that container.

These namespaces provide a layer of isolation. Each aspect of a container runs in a 
separate namespace and its access is limited to that namespace.

**The Docker daemon**
The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. 

**The Docker client**
Client sends such commands as docker run to dockerd, the docker command uses the Docker API. 

**Docker registries**
A Docker registry stores Docker images. For example, Docker Hub. 

**Images**
An image is a read-only template with instructions for creating a Docker container. 
Often, an image is based on another image, with some additional customization. 
For example, you may build an image which is based on the ubuntu image, but installs the Apache web server and your application, 
as well as the configuration details needed to make the application run.

It is possible to create your own images with Dockerfile with a simple syntax for defining the steps needed to create the image and run it. 
Each instruction in a Dockerfile creates a layer in the image. 

**Containers**
A container is a runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI. 
You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.
A container is isolated from other containers and its host machine. 
A container is defined by its image as well as any configuration options provided to it during the create or start process. 
When a container is removed, any changes to its state that are not stored in persistent storage disappear.

### Types of Container Networking
There are five types of container networking:

None: The container receives a network stack; however, it lacks an external connection. This mode is useful for testing containers, 
staging a container for a later network connection, and assigning to containers not requiring external communications.

Bridge: Containers that are bridged on an internal host network and allowed to communicate with other containers on the same host. 
Containers cannot be accessed from outside the host. Bridge network is the default for Docker containers.

Host: This configuration allows a created container to share the host’s network namespace, granting the container access to all 
the host’s network interfaces. The least complex of the external networking configurations, this type is prone to port conflicts 
due to the shared use of the networking interfaces.

Underlay: Underlays open the host interfaces directly to containers running on the host and remove the need for port-mapping, 
making them more efficient than bridges.

Overlay: Overlays use networking tunnels to communicate across hosts, allowing containers to act like they are on the same 
machine when they are hosted on different hosts.

## Блокчейн. Его основные характеристики.
Blockchain technology is a decentralized, distributed ledger that stores the record of ownership of digital assets. 
Any data stored on blockchain is unable to be modified, making the technology a legitimate disruptor for industries like payments, 
cybersecurity and healthcare. 

### Features

**Trustless technology**
Blockchain technology helps to form new digital relationships without need to trust a third party to make a transaction.

**Security and data privacy**
Blockchain technology relies on a large number of computers connected together to keep records of the data stored on them. It's not a single host.
This makes the blockchain a secure network — a lot of computing power is required to hack the network.

**Data redundancy**
As mention above blockchain uses thousands of computers to keep data, this makes it more reliable and redundant.

**Reduced costs**
A blockchain network is maintained by decentralized nodes located across the globe and this removes the costs for hosting, maintenance and the need to
rely on third-party service providers. 

**Accountability and traceability**
Blockchain helps with supply chain management. So companies are able to provide consumers  with tracking the history of the products 
they want to buy.

**It's not easy to hack**
It's theoretically possible but the reward may not be worth the effort. Also usually the hacks of some of the exchanges is not a reflection 
of the security strength of the blockchain but the exploitation of vulnerabilities found in the exchanges.



