# hybrid-cloud-3-tier-public-cloud-aws

## Hybrid Cloud Solution for a 3-Tier Application using AWS for Web Tier and Database Tier

### I designed a blueprint to deploy and configure a 3-Tier Web Application with a Load Balancer hosted on private cloud, two Web Tiers each hosted on a private and public cloud AWS and a Database server hosted on the public cloud AWS

### Design & Configuration
1) Two application profiles for deployment
  * Small - 1 vCPU, 1 core, 1 GB RAM or t2.micro AWS instance
  * Medium - 2vCPU, 2 cores, 1 GB RAM or t2.micro AWS instance
2) Developers can scale in and scale out the Web Tier independent of each provider.
3) Developers can perform a backup and restoral at any time.
4) Public VMs use region us-west-2 and Red Hat Enterprise Linux 8
5) Load Balancer will use HAProxy Software.
6) Web Server will be Apache Web server
7) Web Tier VMs automatically follow a naming convention of wwwX - X = 0-4
8) Web Tier VMs start a 2 replicas and can scale to a maximum of 4, all other services do not scale.

### Security
1) All VM accounts requires SSH access and can be granted sudo privileges.
2) teccadmin account to configure the OS and install software
3) No VM resource parameters can be changed by the end user.
4) Allow SSH access form any IP address for all servicees
5) Allow HTTP and HTTPs access from any IP address for the Web Server and Load Balancer
6) Allow MySQL database access
7) Two SSH credentials, one for the Web Tier and another for the Database Tier

## Create a Blueprint for a 3 Tier App 
### HAProxy &  Apache Web Server deployed on Nutanix
### Apache Web Server & MySQL Server deployed on AWS
![3 Tier App on Nutanix & AWS](/project3/images/2021-02-03_072532-3_tier_hybrid_medium.jpg)

### Add AWS as a Provider
![New AWS Provider](/project3/images/2021-02-03_091453-aws_add_provider_1.jpg)

### Configure Apache Web Server on AWS
![Configure Apache on AWS](/project3/images/2021-02-03_072756-aws_web_server.jpg)

### Configure MySQL Server on AWS
![Configure MySQL on AWS](/project3/images/2021-02-03_072836-aws_mysql_server.jpg)

### Launch Deployment
![Launch Deployment on AWS & Nutanix](/project3/images/2021-02-03_073103-launch_application.jpg)

### Provision 3 Tier App
![Provisioning](/project3/images/2021-02-03_073610-app_provisioning_1.jpg)

### AWS Instances of Apache Web Server and MySQL Server running
![AWS Instances deployed](/project3/images/2021-02-03_074439-aws_instaces.jpg)


### 3 Tier App Provisioning Steps
![App Provisioning](/project3/images/2021-02-03_080640-app_running.jpg)

### 3 Tier App Services Deployed
![App Services](/project3/images/2021-02-03_080739-app_running_2.jpg)

### Activate Web Scale Out Function on Nutanix Apache Web Servers
![WebScaleOut Nutanix Apache Web Servers](/project3/images/2021-02-03_082445-nutanix_web_scale_out.jpg)

### Activate Web Scale Out Function on AWS Apache Web Servers
![WebScaleOut AWS Apache Web Servers](/project3/images/2021-02-03_083541-aws_scale_out.jpg)

### Nutanix & AWS Apache Web Servers Deployed
![Deployed Servers](/project3/images/2021-02-03_085116_-aws-nutanix_web_scaleout.jpg)

### AWS Apache Web Servers Instances
![AWS Apache Web Servers instances](/project3/images/2021-02-03_085302-aws_webscaleout_instances.jpg)

### Backup AWS MySQL Server
![AWS Backup MySQL Function Running](/project3/images/2021-02-03_085339-database_backup.jpg)

### Activate Web Scale In Function on Nutanix Apache Web Servers
![WebScaleIn Nutanix Apache Web Servers](/project3/images/2021-02-03_090528-nutanix_web_scale_in.jpg)

### Display Nutanix Apache Web Servers after WebScaleIn
![WebScaleIn Nutanix Apache Web Servers Instances](/project3/images/2021-02-03_090618-aws_webscalein.jpg)

### Activate Web Scale In Function on AWS Apache Web Servers
![WebScaleIn AWS Apache Web Servers](/project3/images/2021-02-03_091115-aws_scale_in.jpg)

### Display AWS Apache Web Servers after WebScaleIn
![WebScaleIn AWS Apache Web Servers Instances](/project3/images/2021-02-03_091317-aws_scalein.jpg)

### Unprovision AWS Apache Web Servers & MySQL Server - Part 1
![Unprovision AWS Instances - Part 1](/project3/images/2021-02-03_092243-aws_delete.jpg)

### Unprovision AWS Apache Web Servers & MySQL Server - Part 2
![Unprovision AWS Instances - Part 2](/project3/images/2021-02-03_092202-aws_delete.jpg)

### Hybrid Cloud using Nutanix and AWS
![Hybrid Cloud using AWS](/project3/images/0-start.jpg)

