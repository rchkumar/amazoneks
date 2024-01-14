# amazoneks

Instructions :

1. Create cluster using the following command 

     eksctl apply cluster  -f createcluster.yaml --profile eksadmin

2. Register Cluster with IAM Provider using the following command

    eksctl utils associate-iam-oidc-provider \
    --region ap-southeast-1 \
    --cluster eks-acg \
    --approve --profile eksadmin

3. Delete the cluster using the following command

     eksctl delete cluster  -f createcluster.yaml --profile eksadmin

     It will delete all the following resources

            1. Delete the Node Group
            2. Delete the NAT Gateway
            3. Delete the load balancer and ASG
            4. Delete the ENIs
            5. Delete VPC
            6. Delete the cloud formation stacks
            7. Delete the EIP
            8. Delete the faregate profiles


Update is completed.