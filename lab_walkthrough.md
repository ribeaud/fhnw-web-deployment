**Introduction**

In this lab you will deploy a sample Java application based on Amazon ECS Fargate container solution. You will be guided through the all the steps needed.

**Login to the AWS Console**

You will need access to an AWS Account in order to conduct this lab. Either you're having an existing one, or you will be given access to an AWS environment.

**Prepare the environment**

We will be using a couple of AWS services for this lab. Please use the THIS CloudFormation template to automatically setup the infrastructure needed. The template will setup many of the infrastructure components so that you can concentrate on the container part. Please make sure you're running this template in the Frankfurt (eu-central-1) Region.

Services deployed automatically:
- Cloud9 IDE
- ECS Cluster (Fargate)
- ECR
- RDS MySQL
- Application LoadBalancer (ELB)

#Desribe how to run the template

**Access Cloud9 IDE**

Cloud9 is fully managed IDE and provides the AWS SDK, AWS Cli and has Docker pre-installed. 
- In the AWS Console select "Services" and type "Cloud9"
- Click "Open IDE" on your instance. This will open a new window in your Browser and show the Cloud9 GUI
 
**Clone Repository**
- Select the terminal window and make sure you're in the folling directory:
```bash
<some_name>:~/environment $ 
```
- Paste the following command to the terminal window:
```bash 
git clone https://github.com/cvolkmer/fhnw-web-deployment.git
```

**Check the ECR**
- Open a seaparate Browser tab (clone an existing one)
- In the AWS Console select "Services" and type "Elastic Container Registry"
- Click on the existing registry and open it
- Make sure there is no image in the registry
- Click on "View push commands" to get the instructions needed for the next steps.

**Build your image**
- Go back to your Cloud9
- Navigate into the following directory containing the Dockerfile + the .war-File of your application
```bash
cd fhnw-web-deployment/container/
```
- Follow the push commands from ECR and copy / paste them to the terminal window
- First, you will obtain temporary login credentials
- Then you will build your container image locally in Cloud9
- After that you will tag the image and
- Upload (push) it to the ECR registry


**Deploy your container**
- Go back to your Browser tab where you have ECR open
- Close the push instructions and click on "Task Definitions" in the left navigation pane
- Create a task definition
- Set DB parameters in container environment variables
- ...
- Create a service
- Start your service with ALB integration