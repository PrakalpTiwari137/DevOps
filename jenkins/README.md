# Setting up jenkins in Ubuntu 18.04
## Step 1 - Installing jenkins
```
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install jenkins
```
## Step 2 - Starting jenkins
```
sudo systemctl start jenkins
sudo systemctl status jenkins
```
## Step 3 - Opening the firewall
```
sudo ufw allow 8080
sudo ufw status
```
Note: If the firewall is inactive, the following commands will allow OpenSSH and enable the firewall:</br>
```
sudo ufw allow OpenSSH
sudo ufw enable
```
## Step 4 - Setting up jenkins
To set up your installation, visit Jenkins on its default port, `8080`, using your server domain name or IP address:</br>
`http://your_server_ip_or_domain:8080` or `http://localhost:8080`</br>
In the terminal window, use the `cat` command to display the password:</br>
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
For further commands visit</br>
(https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-18-04)
