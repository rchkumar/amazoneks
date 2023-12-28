This Document gives information about how to create Load balancer controller 

1. Navigate to the path where create.sh is present

2. Run the create.sh, it does the following.
     1. Adding Repo for Helm
     2. Installing helm chart for Load balancer Controller
     3. Deploy Cloud Formation template , which is IAM Policy Yaml.
     
3. Attach IAM Policy ARN to the node instance role 

At this stage, we have created ingress controller, assigned IAM policy to the worker nodes, we need to test this whole procedure.

In order to test , navigate to the test folder 

And run ./run.sh script, which creates application load balancer (ingress object )and respective dep and service files


after above step, navigate to the test folder and deploy load balancer by running the script run.sh , which is present in test folder
