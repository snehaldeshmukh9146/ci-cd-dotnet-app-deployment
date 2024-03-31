## Strore Credentials in Jenkins

### Storing Dockerhub Credentials

- Open Jenkins in a browser.
- Click on Credentials.
- Click on System.
- Click on Global credentials.
- Click on Add Credentials.
- Select Username with password.
- Enter the username and password of your Dockerhub account.
- Click on OK.

<img width="472" alt="step6a" src="https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/4260e858-3df9-47ee-bdf1-58a6a4a66288">



### Storing SonarQube Credentials

#### How to get SonarQube Credentials

- Open SonarQube in a browser.
- Click on Administration.
- Click on Security.
- Click on Users.

<img width="788" alt="step6b" src="https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/d230c79d-cbe4-47e8-8019-df92b9edab52">


<img width="570" alt="Step6c" src="https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/9e84400a-8d42-42ef-8f95-890ef6392d42">



#### How to store SonarQube Credentials in Jenkins

- Open Jenkins in a browser.
- Click on Credentials.
- Click on System.
- Click on Global credentials.
- Click on Add Credentials.
- Select Secret text.
- Enter the generated token in the Secret field.
- Enter the ID as `sonar-token`.
- Enter the description as `sonar-token`.
- Click on OK.

<img width="566" alt="step6d" src="https://github.com/snehaldeshmukh9146/ci-cd-dotnet-app-deployment/assets/126494356/c50ce6bb-6c7e-4673-8100-80f8aed46953">
