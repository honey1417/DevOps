CREATE A VM IN GCP

gcloud compute instances create jenkins-slave \
    --zone=us-west4-b \
    --machine-type=e2-medium \
    --tags=http-server,https-server \
    --create-disk=auto-delete=yes,boot=yes,device-name=jenkins-slave,image=projects/centos-cloud/global/images/centos-stream-9-v20241210,mode=rw,size=20


# openjdk-17
--------------------
 INSTALL OPENJDK-17
--------------------
- cd /opt

- wget https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz

- tar xvf openjdk-17.0.2_linux-x64_bin.tar.gz

- sudo mv jdk-17.0.2/ /opt/jdk-17

----------------------------------
 CHANGE ENV VARIABLES FOR ALL USERS
-------------------------------------
- sudo vi /etc/profile

- export JAVA_HOME=/opt/jdk-17
- export PATH=$PATH:$JAVA_HOME/bin

- source /etc/profile
