## Install tools on Virtual machine

### Step 1:
- SSH into the EC2 instance created in [Step-1](./Steps/step-1.md).
```
ssh -i <path-to-pem-file> ubuntu@<ec2-instance-public-ip>
```

- Install Docker.
```
sudo apt-get update
sudo apt-get install docker.io -y
sudo usermod -aG docker $USER
sudo usermod -aG docker Jenkins
sudo chmod 777 /var/run/docker.sock
sudo chown jenkins:docker /var/run/docker.sock
sudo docker ps
```

### Step 2:
- After installing Docker, Spin-up a `sonar` container using the following command.
```
docker run -d --name sonar -p 9000:9000 sonarqube:lts-community
```

- Now, SonarQube is running on port 9000. To access SonarQube, open the port 9000 in the security group of the EC2 instance and open the following URL in a browser.
```
http://<ec2-instance-public-ip>:9000
```
![net-8]![running sonarq1](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/1b64e747-daa7-4e56-aca4-4bdf17412f17)

![net-9]!![imgsonarq2](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/66881cec-324c-4d3f-9853-fb1868096e12)



- Login to SonarQube using the default credentials.
```
Username: admin
Password: admin
```
![net-10]!![login sonarq2](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/6a30591c-4f4f-4e80-a4d8-ef27c34ebd67)


![net-11]!!![sonarq3](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/d4a21513-60f3-4890-93d9-18bcfa6a67ab)



![net-12]![sonarq4](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/76782a70-666b-4b46-bf25-504763907cac)

### Step 3:
- Install Trivy.
```
sudo apt-get install wget apt-transport-https gnupg lsb-release

wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null

echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list

sudo apt-get update

sudo apt-get install trivy -y
```

### Step 4:
- Install make.
```
sudo apt-get install make -y
```

