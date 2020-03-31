# Setting up jenkins in Ubuntu 18.04
Inspired by the youtube video by edureka
Link : (https://www.youtube.com/watch?v=GkyUSSajFEg)

## Step1: Install latest version of Java
```
sudo apt update
sudo apt install default-jdk
java -version
```
## Step2: Install latest version of Apache Tomcat
```
wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.8/bin/apache-tomcat-9.0.8.tar.gz
```
Extract the contents of apache-tomcat-9.0.8.tar.gz
```
sudo tar -xvzf apache-tomcat-9.0.8.tar.gz
```
Now we need to edit the tomcat-users.xml file. It is present in the 'conf' folder. Open it with an editor. In my case the file was present in /home/prakalp/apache9/apache-tomcat-9.0.8/conf
```
gedit /home/prakalp/apache9/apache-tomcat-9.0.8/conf/tomcat-users.xml
```
Remove the comment block containing entry like <role rolename = ""/>
Replace the block with

```xml
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="manager-jmx"/>
<role rolename="manager-status"/>
<role rolename="admin-gui"/>
<role rolename="admin-script"/>
<user username="username_of_your_choice" password="password_of_your_choice" roles="manager-gui,manager-script,manager-jmx,manager-status,admin-gui,admin-script"/>
```

To start the tomcat go to 'bin' folder and type
```
./startup.sh
```
To check if tomcat has started, open web browser and type `localhost:8080`. It should open up Apache tomcat webpage.

## Step3: Download Jenkins war file
To download latest Jenkins war file
```
wget https://updates.jenkins-ci.org/latest/jenkins.war
```

## Step4: Deploy Jenkins war file
Go to the Apache tomcat webpage and click on the 'Manage App' button. 
Type the username and password you specified in the tomcat-users.xml file above
Scroll down and you will see Deploy block
Specify the entries as follows:

Context Path (required) : jenkins
XML configuration file URL : (leave it empty)
WAR or directory URL : (path to the jenkins.war file)

You will see /jenkins in the window which opened after you clicked on the 'Manage App' button

## Step5 : Install relevant plugins
Click on /jenkins after entering window by clicking 'Manage App' button
You will be asked to Unlock Jenkins
Let the text in red. It is the path_to_the_password
Open terminal and type `cat path_to_the_password`
Copy and paste the password. 
You are good to go.

