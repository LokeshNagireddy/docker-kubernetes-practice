### Docker Install in Linux VM

OS: Amazon Linux2

### Connect to EC2 instance in AWS

1. Create a Security group to allow required/all ports. Create for inbound and outbound both.
2. Launch an Amazon EC2 VM with OS as Amazon Linux 2. To login to the VM, you can create a key-pair or login with user-id password based on the setup of the image.
3. Connect the instance by providing below info.
    * IP
    * Username
    * Password/private key
    * Port (SSH by default takes port number 22)

### Install Docker on the VM

1. Update OS Packages

```
sudo yum update -y
```

2. Install Docker

```
sudo yum amazon-linux-extras install docker

```

3. Start Docker

```
sudo service docker start

```

4. Enable Docker

```
sudo systemctl enable docker

```

5. Add User to docker group
```
sudo usermod -a -G docker ec2-user
```

Logout and Login again to run docker commands with normal user.