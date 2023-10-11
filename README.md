# Chicken Disease Classification Project

This project utilizes convolutional neural networks to classify chicken diseases. The primary motivation behind this project was to sharpen deployment skills, though it serves as a practical foundation for tasks of similar nature.

> **Acknowledgment**: Major inspiration for this project was drawn from this [YouTube tutorial](https://www.youtube.com/watch?v=p1bfK8ZJgkE&t=7718s). The objective of recreating it was not only to refine deployment proficiency but also to add individual modifications and deepen comprehension of its core concepts.

## 🔧 Technologies Used
- **DVC** for version control of datasets and machine learning models.
- **Docker** for containerizing the application.
- **AWS** and **Azure** for cloud deployment.
- **Python** for backend logic and ML model training.


## 🚀 Quick Start

### **Step 1**: Clone the repository:

```bash
git clone https://github.com/olaaumari/Chicken-Disease-Classification.git
```

### Step 2: Set up a Python environment:

Using conda, create and activate an environment:


```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
```


### Step 3: Install dependencies:
```bash
pip install -r requirements.txt
```

### Step 4: Launch the application:
```bash
# Finally run the following command
python app.py
```

Then, navigate to your local host to view the app.
```bash
open up you local host and port
```


### DVC Commands:
Execute these commands if you're making changes or want to track data:

1. dvc init
2. dvc repro
3. dvc dag



# AWS-CICD-Deployment-with-Github-Actions

## 1.  Sign in to the AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1.    Construct a docker image from source code.
    2.    Push the docker image to ECR.
    3.    Initiate your EC2 instance.
    4.    Retrieve your image from ECR to EC2.
    5.    Launch the docker image inside EC2.

	#Required AWS Policies::

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    Make sure to save the repository URL for future reference.
    Example: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = exemple >>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = cnnClassifier




# AZURE-CICD-Deployment-with-Github-Actions

## Save password:

exemple : s3cEZKH5yytiVnJ3h+eI3qhhzf9q1vNwEi6+q+WGdd+ACRCZ7JD6


## Run from terminal:

docker build -t chickenapp.azurecr.io/chicken:latest .

docker login chickenapp.azurecr.io

docker push chickenapp.azurecr.io/chicken:latest


## Deployment Steps:

1. Build the Docker image of the Source Code
2. Push the Docker image to Container Registry
3. Launch the Web App Server in Azure 
4. Pull the Docker image from the container registry to Web App server and run 

## 📚 Further Reading

Dive deeper into the topics covered in this project:

- Convolutional Neural Networks ([Source](#))
- Data Version Control ([DVC Documentation](https://dvc.org/doc))
- AWS Deployment ([AWS Documentation](https://docs.aws.amazon.com/))
- Azure Deployment ([Azure Documentation](https://docs.microsoft.com/en-us/azure/))


## 🤝 Contribution & Feedback

Feedback, issues, and pull requests are always welcome. For major changes, please open an issue first to discuss what you would like to change. Your contributions will help enhance the project further.