## Interview Readiness:
* What does it mean to create a Docker image and why do we use Docker images? <br>
 
Creating a Docker image involves creating a lightweight, standalone, and executable package that includes everything needed to run a piece of software or application, such as code, libraries, dependencies, and configurations. Docker images are based on a Dockerfile, which is a script that contains instructions for building the image.<br>

We use Docker images for a variety of reasons, including: <br>

* Portability: Docker images can run on any machine or operating system that supports Docker, regardless of the underlying hardware and software. <br>

* Consistency: Docker images provide a consistent environment for running applications, ensuring that the same software and configurations are used every time the image is deployed. <br>

* Scalability: Docker images can be easily replicated and deployed to multiple machines, making it easy to scale applications up or down as needed.<br>

* Isolation: Docker images provide a level of isolation between the application and the host system, reducing the risk of conflicts or interference with other applications running on the same machine.<br>

* Overall, Docker images simplify the deployment and management of applications by providing a standardized and portable way to package and distribute software.<br>


## Interview Readiness:
* Please explain what is the difference from a Container vs a Virtual Machine? <br>

Containers and virtual machines are both technologies used for deploying and running applications, but they differ in their approach and level of isolation.<br>

Virtual machines (VMs) emulate an entire computer system, including the hardware, operating system, and applications. Each VM runs on a hypervisor, which creates a layer of abstraction between the physical hardware and the virtualized system. This allows multiple VMs to run on the same physical server, each with its own operating system and applications.

Containers, on the other hand, are a type of operating system virtualization that allows multiple applications to run on the same operating system kernel. Containers share the host operating system and some resources, such as the file system and network interface, but they are isolated from each other through a process called containerization. This allows containers to run more efficiently and with less overhead than VMs.

The main differences between containers and VMs are:

Resource requirements: VMs require more resources, such as CPU, memory, and disk space, to run because they emulate an entire operating system, while containers only require the resources needed to run the application.

Isolation: VMs provide a higher level of isolation between applications because each VM has its own operating system and resources. Containers share the host operating system and some resources, but they are isolated from each other through containerization.

Performance: Containers generally provide better performance than VMs because they have less overhead and can be started and stopped more quickly.

In summary, while both containers and virtual machines provide a way to deploy and run applications, containers are generally more lightweight and efficient, while VMs provide a higher level of isolation and security. The choice between the two depends on the specific requirements of the application and the environment in which it will be deployed.


## Interview Readiness:
* What are 5 examples of container orchestration tools (please list tools)? <br>

Here are five popular container orchestration tools:

Kubernetes: Kubernetes is an open-source container orchestration platform developed by Google. It provides a scalable and highly available platform for deploying and managing containerized applications.

Docker Swarm: Docker Swarm is a native clustering and orchestration tool for Docker containers. It provides a simple and easy-to-use platform for deploying and managing Docker-based applications.

Apache Mesos: Apache Mesos is an open-source distributed systems kernel that provides efficient resource isolation and sharing across distributed applications or frameworks, including containerized applications.

Nomad: Nomad is a flexible and simple-to-use container orchestration platform developed by HashiCorp. It can run both containerized and non-containerized applications, and it provides a single platform for managing a variety of workloads.

Amazon ECS: Amazon ECS (Elastic Container Service) is a fully-managed container orchestration service offered by Amazon Web Services. It provides a scalable and highly available platform for deploying and managing containerized applications on the AWS cloud.

There are many other container orchestration tools available, each with their own strengths and weaknesses, but these five are among the most popular and widely used in the industry.


## Interview Readiness:
* How does a Docker image differ from a Docker container? <br>

A Docker image is a static, immutable snapshot of an application and its dependencies, while a Docker container is a running instance of that image.

Docker images are created using a Dockerfile, which defines the application and its dependencies, as well as any other configurations or settings required to run the application. The Dockerfile is used to build a Docker image, which is essentially a lightweight, standalone, and portable package that includes everything needed to run the application.

Docker containers, on the other hand, are created by running a Docker image. When a Docker image is run, a Docker container is created, which is a lightweight and isolated runtime environment that runs the application. Each container runs in its own isolated environment with its own file system, networking, and resources, and it can be started, stopped, and restarted as needed.

In summary, a Docker image is a static snapshot of an application and its dependencies, while a Docker container is a running instance of that image. Docker images are used to build and package applications, while Docker containers are used to run and manage those applications.
