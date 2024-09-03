# Docker Study Guide

I've created this repository to showcase my studies on Docker. The Dockerfile folder includes a README with descriptions of important commands and some simple projects to test this commands. Below you'll find an overview of some basic concepts.

### Container
It’s an isolated process that runs in its own isolated environment. 
They are:

- **Self-contained**: It contains everything it needs to run with no reliance on any pre-installed dependency on the host machine.

- **Portable**: It works the same way on the development machine, data center or anywhere in the cloud.

- **Isolated**: One container has minimal influence on the host machine or another container, 
increasing the security of the application.

- **Independent**: Container are managed independently, delete one container won’t affect any 
others.

### Virtual Machines x Containers
A virtual machine is an entire operating system with its own kernel, hardware driver, programs, and applications. Despite being isolated, containers run on the same operating system as the host. Using a container instead of VM to run a single application can save costs.

### Image
It’s a standardized package that contains all the files, binaries, libraries and configuration 
to run a container. There are two important principles of images, they are immutable, once 
created it cannot be modified you can only create a new one or add changes on top of it, and 
they are composed of layers, each layer represents a set of file system changes that add, 
modify or remove files.

### Registry
It’s a centralized location for storing and sharing container images. It can be either public 
or private, with Docker Hub as the default public registry anyone can use. It contains 
repositories where the images are stored.

### Repository
It’s a collection of related container images within a registry.

### Docker Compose
It’s a declarative tool that defines multiple containers and their configuration in a single 
YAML file.

### Dockerfile 
It’s a text-based file with no extension that contains a script of instruction to build a 
container image.

### Volume
It provides the ability to connect specific filesystem paths of the container back to the host 
machine. Each time a container is started, it starts from the image definition and can create, 
update, and delete files, but Docker isolates these changes to the container, so when a 
container is removed, all of these changes are lost. Volumes can change all of this because 
changes in a mounted directory of the container are also seen on the host machine. Therefore, 
if you mount the same directory across container restarts, the same files would always be seen.
There are two types of volumes: volume mount that is completely managed by docker and bind 
mount that is dependent on the directory structure and os of the host machine.