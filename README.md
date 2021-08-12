# Sonarqube-installation
## Install java and sonarqube
### Step1
```sh
sudo yum install java-1.8.0-openjdk.x86_64  -y
```
### Step2
```sh
cd /opt
```
### Step3
```sh
sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-7.2.1.zip
```
### Step4
```sh
sudo unzip sonarqube-7.2.1.zip
```
### Step5
```sh
sudo chown -R ec2-user.ec2-user sonarqube-7.2.1
```
## Run Sonarqube as a service
### Step1
* Create the file /etc/init.d/sonar with this content:
```sh
#!/bin/sh
#
# rc file for SonarQube
#
# chkconfig: 345 96 10
# description: SonarQube system (www.sonarsource.org)
#
### BEGIN INIT INFO
# Provides: sonar
# Required-Start: $network
# Required-Stop: $network
# Default-Start: 3 4 5
# Default-Stop: 0 1 2 6
# Short-Description: SonarQube system (www.sonarsource.org)
# Description: SonarQube system (www.sonarsource.org)
### END INIT INFO
 
/usr/bin/sonar $*
```
### Step2
* Register SonarQube at boot time (RedHat, CentOS, 64 bit):
```sh
sudo ln -s $SONAR_HOME/bin/linux-x86-64/sonar.sh /usr/bin/sonar
```
* Here $SONAR_HOME = /opt/sonarqube/(path of sonarqube installed)
```sh
sudo chmod 755 /etc/init.d/sonar
```
```sh
sudo chkconfig --add sonar
```
* Start the Sonarqube
```sh
sudo service sonar start
```
* To start sonarqube automatically when your ec2 reboot or restarts
```sh
sudo chkconfig sonar on
```
* Check the sonarqube status
```sh
sudo service sonar status
```
### Sonar default port is 9000
### Default username and password is admin/admin
