# Docker
# Lab work. Day 1
Tasks
1.	Install Docker Service on CentOS 7
1.1	Install Docker.
1.2	Verify that Docker has been installed and running correctly.
1.3	Check that service runs on Host start.
2.	Build Custom Docker Images. Use different the same tags and different versions (Name all images like sbeliakou/nginx:2.1, where "s" stands for "Siarhei" and "beliakou" is surname. “2.1” – points to the task number 2.1. Use your Real names from UPSA)
2.1	Create Dockerfile and build custom image of nginx (on centos).
2.2	Create Dockerfile and build custom image of nginx (on ubuntu).
2.3	Create Dockerfile and build custom image of nginx (on alpine).
2.4	Create Dockerfile and build custom image of tomcat (on maven:3.3-jdk-8/java:8-jre). Use sample java project from https://github.com/MNT-Lab/p323line
3.	Run Containers in different modes. Prove settings to be applied correctly.
3.1	Run Nginx and Tomcat with port mapping to Host node (automatically assigned port).
3.2	Run Nginx and Tomcat with port mapping to Host node (statically defined mapping).
3.3	Run Nginx and Tomcat with port mapping to Host node (automatically assigned port).
3.4	Run Nginx and Tomcat with Specified names.
3.5	Run Nginx and Tomcat with Specified names, mount vhost config to Nginx so that it forwards requests to Tomcat backend.
3.6	Run Nginx and Tomcat with different restart policies: always/unless-stopped
4.	Operate with running containers and available images.
4.1	Get List of Running Containers.
4.2	Get List of Running Containers, apply custom filter (Name, Image, Ports, Status).
4.3	Stop several containers (docker stop/docker kill). Get details about them.
4.4	Remove all stopped containers.
4.5	Remove all unused images.
5.	Working with Custom Network
5.1	Create custom network (123.45.0.0/16). Choose unique subnet.
5.2	Run Nginx and Tomcat in Custom Network (specify label which points to custom bridge network). Check details (IP addresses)
5.3	Run Nginx and Tomcat in Custom Network (specify label which points to custom bridge network) with specified IP addresses from chosen subnet.
5.4	Run Nginx in both Host and Custom Bridge Networks. Check details.
5.5	Stop all Containers in Custom Network (use filter by label you specified in 5.1-5.4)
5.6	Delete Custom Network.
5.7	Delete all containers (use filter by label you specified in 5.1-5.4)
6.	Get logs from all containers.
6.1	Get logs from Containers with “docker log” command
6.2	Run Tomcat so that its logs (catalina.out) will be available on the host system by the path of /var/log/tomcat/catalina.out. Check logs.
6.3	Configure Containers to send logs to Journald. Get logs with journalctl.
6.4	Configure Docker daemon to send logs from all containers to journald.
# Lab work. Day 2
Tasks
1.	Create docker-compose file for the next services: Nginx (latest), Jenkins (latest stable), Nexus (latest stable).
1.1	Nginx should forward to Jenkins and Nexus (virtual hosts / servers).
1.2	Jenkins should store all jobs and configuration data in external volume.
1.3	Nexus should store all artifacts in external volume.
1.4	Restrict Jenkins to use no more than 500MB of RAM.
1.5	Restrict Nexus to use no more than 300MB of RAM.
1.6	Restrict Jenkins to utilize no more than 35% CPU (test it).
1.7	Restrict Nexus to utilize no more than 25% CPU (test it).
1.8	Configure all containers (Nginx, Jenkins, Nexus) to send logs to journald. Check logs.
1.9	Assign custom network and IP addresses to Nginx, Jenkins and Nexus containers.
1.10	Create Jenkins Job to verify connectivity between Jenkins and Nexus.

2.	Configure SWARM on the Host
2.1	Create docker-compose file to deploy Nginx+Jenkins into SWARM. Choose appropriate settings.
