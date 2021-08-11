# Sonarqube-installation
## Install java and sonarqube
* sudo yum install java-1.8.0-openjdk.x86_64  -y
* cd /opt
* sudo wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-7.2.1.zip
* sudo unzip sonarqube-7.2.1.zip
* sudo chown -R ec2-user.ec2-user sonarqube-7.2.1
## Start Sonar
/opt/sonarqube-7.2.1/bin/linux-x86-64/sonar.sh start
### Sonar default port is 9000
### Default username and password is admin/admin
