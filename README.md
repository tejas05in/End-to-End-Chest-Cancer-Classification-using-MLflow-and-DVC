# End-to-End-Chest-Cancer-Classification-using-MLflow-and-DVC


## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml
10. app.py



### dagshub
[dagshub](https://dagshub.com/)


MLFLOW_TRACKING_URI=https://dagshub.com/tejas05in/End-to-End-Chest-Cancer-Classification-using-MLflow-and-DVC.mlflow \
MLFLOW_TRACKING_USERNAME=tejas05in \
MLFLOW_TRACKING_PASSWORD=9efcb5c7b79d0e949378459b922b1462a80fa413 \
python script.py



```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/tejas05in/End-to-End-Chest-Cancer-Classification-using-MLflow-and-DVC.mlflow \
export MLFLOW_TRACKING_USERNAME=tejas05in \
export MLFLOW_TRACKING_PASSWORD=9efcb5c7b79d0e949378459b922b1462a80fa413 \

```

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.
## 2. Create IAM user for deployment

```

# with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


# Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

# Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

```
# 3. Create ECR repo to store/save docker image
```
- Save the URI: 186341999825.dkr.ecr.ap-northeast-1.amazonaws.com/carcinoma
```
# 4. Create EC2 machine (Ubuntu)
# 5. Open EC2 and Install docker in EC2 Machine:

```
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

# 6. Configure EC2 as self-hosted runner:

setting>actions>runner>new self hosted runner> choose os> then run command one by one

# 7. Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = ap-northeast-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app