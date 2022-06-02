#
# Interview#Devops
## What is Devops ? 

By the name DevOps, it’s very clear that it’s a collaboration of Development as well as Operations. But one should know that DevOps is not a tool, or software or framework, DevOps is a Combination of Tools which helps for the automation of the whole infrastructure. ## Simple devops project Explain the CI/CD Pipeline using all the devops tools learnt ## What is Scrum? Scrum is basically used to divide your complex software and product development task into smaller chunks, using iterations and incremental practises. Each iteration is of two weeks. Scrum consists of three roles: Product owner, scrum master and Team 

## Mention the key aspects or principle behind DevOps? 

The key aspects or principle behind DevOps is: • Infrastructure as a Code • Continuous Integration • Continuous Deployment • Automation • Continuous Monitoring • Security 
## List out some of the popular tools for DevOps?
• Git 
• Jenkins 
• Ansible 
• Terraform 
• Kubernetes 
• Docker 
• Grafana 
## What is IaC? How you will achieve this? 

Infrastructure as Code (IaC) is the management of infrastructure (networks, virtual machines, load balancers, and connection topology) in a descriptive model, using the same versioning as DevOps team uses for source code. This will be achieved by using the tools such as Chef, Puppet and Ansible etc.

## Explain what is continuous integration? 
When multiple developers or teams are working on different segments of same web application, we need to perform integration test by integrating all the modules. To do that an automated process for each piece of code is performed on daily bases so that all your code gets tested. And this whole process is termed as continuous integration 

#GIT 

## what language is used in Git?
Git is written in C language, and since its written in C language its very fast and reduces the overhead of runtimes. 

## how can you clone a Git repository via Jenkins? 

First, we must enter the e-mail and user name for your Jenkins system, then switch into your job directory and execute the “git config” command. 

## Difference between git merge and rebase 

rebase reapplies commits on top of another base branch”, whereas “merge joins two or more development histories together 

## Explain the difference between git pull and git fetch? 

Git pull command basically pulls any new changes or commits from a branch from your central repository and updates your target branch in your local repository. Git fetch is also used for the same purpose, but its slightly different form Git pull. When you trigger a git fetch, it pulls all new commits from the desired branch and stores it in a new branch in your local repository. If we want to reflect these changes in your target branch, git fetch must be followed with a git merge. Our target branch will only be updated after merging the target branch and fetched branch. Just to make it easy for us, remember the equation below: Git pull = git fetch + git merge 

## What is the function of ‘git config’?
Git uses our username to associate commits with an identity. The git config command can be used to change our Git configuration, including your username. Suppose you want to give a username and email id to associate commit with an identity so that you can know who has made a commit. For that I will use: git config –global user.name “Your Name”: This command will add your username. git config –global user.email “Your E-mail Address”: This command will add your email id 

## Describe the branching strategies you have used? 

Generally, they ask this question to understand your branching knowledge Feature branching This model keeps all the changes for a feature inside of a branch. When the feature branch is fully tested and validated by automated tests, the branch is then merged into master. Task branching In this task branching model each task is implemented on its own branch with the task key included in the branch name. It is quite easy to see which code implements which task, just look for the task key in the branch name. Release branching Once the develop branch has acquired enough features for a release, then we can clone that branch to form a Release branch. Creating this release branch starts the next release cycle, so no new features can be added after this point, only bug fixes, documentation generation, and other release-oriented tasks should go in this branch. Once it’s ready to ship, the release gets merged into master and then tagged with a version number. In addition, it should be merged back into develop branch, which may have progressed since the release was initiated earlier 

# Ansible 

## What is ansible ? 

Ansible is mainly used in IT infrastructure to manage or deploy applications to remote nodes. Let’s say we want to deploy one application in 100’s of nodes by just executing one command, then Ansible is the one actually coming into the picture but should have some knowledge on Ansible script to understand or execute the same. 

## difference between ansible and chef ? 

Chef operates with a master-client architecture. The server part runs on the master machine, while the client portion runs as an agent on every client machine. Chef also has an extra component named “workstation” that stores all of the configurations that are tested then pushed to the central server. Ansible only uses a master running on the server machine, but no agents running on the client machine. It uses an SSH connection to log in to the client systems or the nodes you want to configure, and the client machine VM has no need for special setup. ## What are the Pros and Cons of Ansible? Pros: 1. Open Source 2. Agent less 3. Improved efficiency , reduce cost 4. Less Maintenance 5. Easy to understand yaml files Cons: 6. Underdeveloped GUI with limited features 7. Increased focus on orchestration over configuration management 8. SSH communication slows down in scaled environments # Docker ##what is docker ? Docker is a containerization technology that packages your application and all its dependencies together in the form of Containers to ensure that your application works seamlessly in any environment.

# Docker 

## what is docker images ?
Docker image is the source of Docker container. Or in other words, Docker images are used to create containers.

## what is Docker Container? 

Docker Container is the running instance of Docker Image.

## How can you connect a container to a network when it starts? 
We need to use a following command 
docker run -itd –network=multi-host-network busybox 

## what is difference between grep -i and grep -v? 
I ignore alphabet difference V accept this value ex) ls | grep -i docker Dockerfile docker.tar.gz ls | grep -v docker Desktop Dockerfile Documents Downloads

## what is the dockefile? Explain docker commands? 

A Docker File is a simple text file with instructions on how to build your images. The following points need to be noted about the above file − The first line "#This is a sample Image" is a comment. You can add comments to the Docker File with the help of the # command The next line has to start with the FROM keyword. It tells docker, from which base image you want to base your image from. 
In our example, we are creating an image from the ubuntu image. 
The next command is the person who is going to maintain this image. 
Here you specify the MAINTAINER keyword and just mention the email ID. 
The RUN command is used to run instructions against the image.
In our case, we first update our Ubuntu system and then install the nginx server on our ubuntu image.
The last command is used to display a message to the user. 

## Jenkins

## what is a Jenkins Pipeline? Jenkins Pipeline (or simply “Pipeline”) is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins. ## Explain what is continuous integration? When multiple developers or teams are working on different segments of same web application, we need to perform integration test by integrating all the modules. To do that an automated process for each piece of code is performed on daily bases so that all your code gets tested. And this whole process is termed as continuous integration. ## How to add slaves nodes? A Slave is a Java executable that runs on a remote machine. Following are the characteristics of Jenkins Slaves: It hears requests from the Jenkins Master instance. Slaves can run on a variety of operating systems ## explain declarative pipeline? Declarative Pipeline replaces Groovy variable assignments, control structures, loops, and exception handling with a predefined structure and model to allow users of all experience levels to quickly create consistent, concise Pipelines without learning Groovy. ## explain scripted pipeline? Scripted Pipeline allows users to code their Pipelines using a Groovy DSL ## what is difference between continuous deployment and delivery? In continuous deployment, the deployment to production is automatically triggered for every change that passes the test suite. Continuous Delivery is the ability to get changes of all types; including new features, configuration changes, bug fixes and experiments into production, or into the hands of users, safely and quickly in a sustainable way. ## What are the Labels in Jenkins and where it tends to be used? Similarly as with CI/CD arrangement should be concentrated , where each application in the association can be worked by a solitary CI/CD server , so in association there might be various types of utilization like java, c#,.NET and so forth, likewise with microservices approach your programming stack is inexactly coupled for the task , so you can have Labeled in every hub and select the choice Only assembled employments while name coordinating this hub, so when a manufacture is planned with the mark of the hub present in it, it hangs tight for next agent in that hub to be accessible, despite the fact that there are different agents in hubs. ## how to create githook? Git hooks are scripts that run automatically every time a particular event occurs in a Git repository. example as githook to jenkins user to build is triggered for every pull. # terraform ## Terraform commands? * terraform init - initializes the current directory * terraform refresh - refreshes the state file * terraform output - views Terraform outputs * terraform apply - applies the Terraform code and builds stuff * terraform destroy - destroys what has been built by Terraform * terraform plan - a dry run to see what Terraform will do ## What is Terraform init? Terraform init is a control to initialize an operational index that contains Terraform pattern files. This control can be looped multiple times. It is the first command that should be run after writing the new Terraform design. Give the terraform configuration for creating a single EC2 instance on AWS. This is the Terraform configuration for creating a single EC2 instance on AWS: provider “aws” { region = “”} resource “aws_instance” “example” { ami = "" instance_type = "" tags { Name = "example"} # AWS ## What is multifactor authentication? What is the use of it? Multifactor authentication (MFA) is a security system that requires more than one method of authentication from independent categories of credentials to verify the user’s identity for a login or other transaction. ## what is application loader balancer ? A load balancer serves as the single point of contact for clients. The load balancer distributes incoming application traffic across multiple targets, such as EC2 instances, in multiple Availability Zones. This increases the availability of your application. [Application load balancer] https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html ## what is network load balancer? Elastic Load Balancing automatically distributes your incoming traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones. It monitors the health of its registered targets, and routes traffic only to the healthy targets. Elastic Load Balancing scales your load balancer as your incoming traffic changes over time. It can automatically scale to the vast majority of workloads. [Network load balancer] https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html ## what is S3 bucket? A bucket is a container for objects stored in Amazon S3. You can store any number of objects in a bucket and can have up to 100 buckets in your account. ## what is IAM policy? IAM policies define permissions for an action regardless of the method that you use to perform the operation. For example, if a policy allows the GetUser action, then a user with that policy can get user information from the AWS Management Console ## what is EBS Volume? Amazon Elastic Block Store (Amazon EBS) provides block level storage volumes for use with EC2 instances. EBS volumes behave like raw, unformatted block devices. You can mount these volumes as devices on your instances. ## userdata Run commands on your instance at launch # Kubernetes ## What is Kubernetes? Kubernetes is an open-source container orchestration tool or system that is used to automate tasks such as the management, monitoring, scaling, and deployment of containerized applications. ## What is orchestration when it comes to software and DevOps? Orchestration refers to the integration of multiple services that allows them to automate processes or synchronize information in a timely fashion. Say, for example, you have six or seven microservices for an application to run. If you place them in separate containers, this would inevitably create obstacles for communication. Orchestration would help in such a situation by enabling all services in individual containers to work seamlessly to accomplish a single goal. ## What is a pod in Kubernetes? In this Kubernetes interview question, try giving a thorough answer instead of a one-liner. Pods are high-level structures that wrap one or more containers. This is because containers are not run directly in Kubernetes. Containers in the same pod share a local network and the same resources, allowing them to easily communicate with other containers in the same pod as if they were on the same machine while at the same time maintaining a degree of isolation. ## What is a Namespace in Kubernetes? Namespaces are used for dividing cluster resources between multiple users. They are meant for environments where there are many users spread across projects or teams and provide a scope of resources. ## What is etcd? Kubernetes uses etcd as a distributed key-value store for all of its data, including metadata and configuration data, and allows nodes in Kubernetes clusters to read and write data. Although etcd was purposely built for CoreOS, it also works on a variety of operating systems (e.g., Linux, BSB, and OS X) because it is open-source. Etcd represents the state of a cluster at a specific moment in time and is a canonical hub for state management and cluster coordination of a Kubernetes cluster. ## What are the different services within Kubernetes? Different types of Kubernetes services include: 1. Cluster IP service 2. Node Port service 3. Load Balancer service ## What is ClusterIP? * The ClusterIP is the default Kubernetes service that provides a service inside a cluster (with no external access) that other apps inside your cluster can access ## what is nodeport The NodePort service is the most fundamental way to get external traffic directly to your service. It opens a specific port on all Nodes and forwards any traffic sent to this port to the service. ## What is the difference between a replica set and a replication controller? A replication controller is referred to as RC in short. It is a wrapper on a pod. This provides additional functionality to the pods, which offers replicas. It monitors the pods and automatically restarts them if they fail. If the node fails, this controller will respawn all the pods of that node on another node. If the pods die, they won't be spawned again unless wrapped around a replica set. Replica Set, on the other hand, is referred to as rs in short. It is told as the next-generation replication controller. This kind of support has some selector types and supports the equality-based and the set-based selectors. It allows filtering by label values and keys. To match the object, they have to satisfy all the specified label constraints.