
# AWS EC2 – Linux Server Setup and Apache Web Server Installation

## 1. Lab Name
AWS EC2 – Linux Server Setup and Apache Web Server Installation

## 2. Objective
To launch a Linux virtual machine on Amazon EC2, configure the instance, and install the Apache HTTP Server to prepare a web server environment.

## 3. Technologies & Tools Used
- AWS EC2
- AWS Management Console
- AWS Sandbox Environment
- Amazon Linux 2023
- Apache HTTP Server (HTTPD)
- Linux
- Cloud-init

## 4. Implementation Steps
1. Started the AWS Sandbox environment.
2. Accessed the AWS Management Console.
3. Launched a Linux EC2 instance using Amazon Linux 2023.
4. Configured the instance with the required startup settings.
5. Booted the EC2 instance successfully.
6. Verified the network interface initialization.
7. Observed the cloud-init startup configuration process.
8. Installed the Apache HTTP Server (`httpd`) through the startup configuration.
9. Verified the package installation from the system logs.
10. Confirmed that the cloud-init process completed successfully.

## 5. Linux Commands Practised

| Command | Description |
|---|---|
| `sudo systemctl status httpd` | Checks Apache service status |
| `sudo systemctl start httpd` | Starts the Apache service |
| `sudo systemctl enable httpd` | Enables Apache to start automatically at boot |
| `ip addr` | Displays network interface information |
| `uname -a` | Displays Linux kernel information |

## 6. Real-World Applications
- Hosting websites on AWS EC2 instances.
- Configuring Linux-based web servers.
- Deploying web applications in cloud environments.
- Managing Apache HTTP Server services.
- Understanding automated server provisioning using cloud-init.
- Supporting cloud infrastructure and DevOps operations.

## 7. Screenshots

### output
![Output](screenshots/linux-boot.png)

### Instance 
![Instance](screenshots/Apache Service Status.png)

## 8. Result
Successfully launched an Amazon Linux 2023 EC2 instance and installed the Apache HTTP Server using automated startup configuration.

Gained hands-on experience with:
- EC2 instance initialization.
- Amazon Linux 2023 environment.
- Cloud-init configuration.
- Apache HTTP Server installation.
- Linux server administration basics.

## 9. Key Learning
Understood how AWS EC2 instances initialize, how cloud-init automates server configuration during startup, and how Apache HTTP Server can be installed to prepare a Linux machine for web hosting.
