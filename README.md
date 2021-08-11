# Sonarqube-installation
## Install java and sonarqube
```sh
sudo yum install java-1.8.0-openjdk.x86_64  -y
```
```sh
cd /opt
```
```sh
sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-7.2.1.zip
```
```sh
sudo unzip sonarqube-7.2.1.zip
```
```sh
sudo chown -R ec2-user.ec2-user sonarqube-7.2.1
```
## Start Sonar
/opt/sonarqube-7.2.1/bin/linux-x86-64/sonar.sh start
### Sonar default port is 9000
### Default username and password is admin/admin
