# Build_Container
Learn to build a container w/ Docker and Singularity
### Studying Notes
1. Understanding Docker:  
Docker Basics: Familiarize yourself with Docker concepts such as images, containers, Dockerfiles, and Docker Hub.  
2. Docker Installation:
Install Docker on your system. The installation process varies depending on your operating system.
3. Setting Up a Dockerfile for CNVkit using the base image Python 3.7
4. Build the Docker image:
```
docker build -t <cnvkit-image> .
```
5. Example to run the Docker container
```docker run -it --name cnvkit-container cnvkit-image```
