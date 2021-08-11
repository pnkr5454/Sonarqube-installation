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
## Start Sonar
### Step6
```sh
/opt/sonarqube-7.2.1/bin/linux-x86-64/sonar.sh start
```
### Sonar default port is 9000
### Default username and password is admin/admin
