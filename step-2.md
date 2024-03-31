## Install and Configure Jenkins

- SSH into the EC2 instance created in [Step-1](./Steps/step-1.md).
```
ssh -i <path-to-pem-file> ubuntu@<ec2-instance-public-ip>
```
- Install Jenkins.
```
sudo apt-get update

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
    /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update
sudo apt-get install fontconfig openjdk-11-jre
sudo apt-get install jenkins

sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```
- Now Jenkins is installed and running on port 8080. To access Jenkins, open the following URL in a browser.
```
http://<ec2-instance-public-ip>:8080
```
- To get the initial admin password, run the following command.
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
unlock jenkins
![net-3]![jenkins-login](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/ece577c9-f1ba-4c63-8a7e-aa0b607bf952)

- Install the suggested plugins.
![net-4]![jenkins-custmi](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/4cb87e8e-78d4-48ea-b35f-71718dfe5e91)


- Create an admin user.
![net-5]![jenkins-login-info](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/6ff6ae5e-c355-4458-8a4a-f4021608319c)




- Jenkins is now ready to use.
![net-6]![jenkins-readytouse](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/12d79344-7389-401c-8bd2-736811004875)

