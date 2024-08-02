## install brew

    brew install awscli

    brew install kubectl

    brew install weaveworks/tap/eksctl

## login console
    aws.amazon.com

## create iam user group/create user and assign to group

1. create user group: eks
2. attach policies: administratoracces
3. create user: eks-[name], add to user group
4. generate access key id, on user > security credentials > access keys
5. access keys > create access keys > select cli > i understand

## create eks cluster from command line

1. verify region provides eks service
2. find secret key and access key (csv)

    aws configure

view aws configure

    cat .aws/config 

    cat .aws/credentials

view recetly generated user

    aws iam get-user

    aws eks list-clusters


use yml manifest to create infraestructure (IaC)
    
    cluster.yaml

Once cluster.yaml file is completed, run command

    eksctl create cluster -f cluster.yaml

view aws worker nodes

    kubectl get nodes

cluster you can work with

    kubectl config get-contexts

    kubectl get pods -A

QUESTIONS
What is the name of the directory where the AWS CLI stores your credentials?
    .aws

To create a user with admin permissions, you start by creating what kind of IAM resource?
    IAM User group

Which AWS resource runs your Kubernetes worker nodes?
    EC2
