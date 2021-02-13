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

![Hybrid Cloud using AWS](/project3/images/0-start.jpg)

