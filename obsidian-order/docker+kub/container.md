# container
****Container:**** ****Container**** refers to a lightweight, stand-alone, executable package of a piece of software that allows a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, thanks to the container, the developer can rest assured that the application will run on any other Linux machine regardless of any customized settings that the machine might have that could differ from the machine used for writing and testing the code.

In a way, Docker is a bit like a virtual machine. But unlike a virtual machine, rather than creating a whole virtual operating system, Docker allows applications to use the same Linux kernel as the system that they’re running on and only requires applications to be shipped with things not already running on the host computer. Also, containers are created and booted in seconds, use fewer resources while a VM takes time to boot and use more resources.
***
**Containers** have been used by developers for a long time to build, ship, and run applications.
***

Containers are isolated file-system capable of executing programs in a sandbox way. It contains all the things that the software needs to run.
***
A container is a unit of software that packages code with its required dependencies in order to run in an isolated, controlled environment. This allows you to run an application in a way that is predictable, repeatable, and without the uncertainty of inconsistent code execution across diverse development and production environments. A container will always start up and run code the same way, regardless of what machine it exists on.

Containers provide benefits on multiple levels. In terms of physical allocation of resources, containers provide efficient distribution of compute power and memory. However, containers also enable new design paradigms by strengthening the separation of application code and infrastructure code. This design separation also enables specialization within teams of developers, allowing developers to focus on their strengths.
***
A container allows us to virtualize applications and data and host this on top of a host virtual machine.

Containers are similar to Virtual Machines in that they virtualize some of your application. the difference is that a Virtual Machine abstracts away the hardware because it sits on top of a Virtual Machine so it abstracts away the operating system. Just as one physical machine can host multiple Virtual Machines, one Virtual Machine can host multiple containers.

Containers provide the following advantages:

-   They allow one VM to host multiple containers, potentially providing more efficient use of resources.
-   They allow us to isolate the applications in different containers, so they will not interfere with one another.
-   Containers allow us to split up an application physically, so that we can deploy, update, and scale each part of the application independently.

A container is based on an image. An image contains all the information to create a container in the same way that a class contains the information to instantiate an object and a blueprint contains the information to construct a building.
***
![[container.jpg]]
***
![[containerization.jpg]]
***



#container
#docker #kubenetes
