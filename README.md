# **docker-dotnetcore-api**
Step-by-Step how-to build and package a .NET Core API as a Docker image, then deploy and spin that image up as Container on Windows, Linux hosts.

# **What is Docker?**
Docker is a **"containerization"** platform, enabling to package applications into images and run them as **“containers”** on any platform that can run Docker. So “It works on my local” argument is an empty word with Docker, as Docker images contain everything needed for the app to run. Cute!

# Containers vs. Virtual Machines
In short;
- Virtual Machines provide OS Level Virtualisation
- Containers provide App Level Virtualisation

![Virtual Machines vs. Containers](https://cloudblogs.microsoft.com/uploads/prod/sites/37/2019/07/Demystifying-containers_image1.png)

*ref* https://cloudblogs.microsoft.com/opensource/2019/07/15/how-to-get-started-containers-docker-kubernetes/

# Why Use Docker?
- Portability : Containers are self-contained so they can run on any platform that runs Docker.
- Scalability : Additional use of **“orchestration”** can spin up multiple container instances to support increased load.
- Performance : Containers generally perform better than their VM counterparts.

# **Ingredients**
 - VS Code or another IDE of your choice (free) [https://code.visualstudio.com/](https://code.visualstudio.com/)
 - .NET Core SDK (free)
 - Docker Desktop (free) [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
 - Docker Hub Account (free) [https://hub.docker.com/] (https://hub.docker.com/)
 - *(optional)* Some local machine to test your deployment

# **Docker Deployment**
## Deployment Flow

```mermaid
graph TD
A(DotNetCore API) -- Package as --> B((Docker Image))
B -- Run as --> C((Docker Container))