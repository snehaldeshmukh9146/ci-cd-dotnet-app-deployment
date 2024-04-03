## Deploying Application

- Go to the Jenkins Dashboard and click on the pipeline job.
- Click on **Build Now**.
- First , Try to build the pipeline with test stages only.
-  ![net-30](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/9a54671b-03d6-4d1c-8a16-9470c25cf190")

- You can see the test results in SonarQube also by going to Project section.
 ![net-31]

- After that, try to build the pipeline with all the stages.

- The build will start and you can see the progress in the console output.
- ![net-32](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/838481d1-f814-4381-af75-1f3636e894de")
 


- Once the build is completed, you can see the application running on the public IP of the EC2 instance.
- You can also see the application running on the public IP of the EC2 instance.
- You can see the .NET in the browser. By default, the application runs on port 5000.
- So, you have to open the port 5000 in the security group of the EC2 instance.
![net-37](https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/402d304c-60cf-4cf7-b1f8-58a68a681c36")


- Now, you can access the application using the URL `http://<public-ip>:5000`.
![net-38](https://github.com/mathesh-me/ci-cd-dotnet-app-deployment/assets/144098846/f9d36c37-229b-44bd-83d6-5581eebca057)
- Now , You can use the .net application.
