# Install-Jenkins-on-AWS
## How can you easily setup Jenkins on AWS EC2 instance (Ubuntu)

# Step - 1 Install Java
Update your system
```sh
sudo apt update
```
Install java
```sh
sudo apt install openjdk-11-jre
```
Validate Installation
```sh
java -version
```
It should look something like this
```sh
openjdk version "11.0.12" 2021-07-20 OpenJDK Runtime Environment (build 11.0.12+7-post-Debian-2) OpenJDK 64-Bit Server VM (build 11.0.12+7-post-Debian-2, mixed mode, sharing)
```

# Step - 2 Install Jenkins

Just copy these commands and paste them onto your terminal.
```sh
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee \   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```
```sh
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \   https://pkg.jenkins.io/debian binary/ | sudo tee \   /etc/apt/sources.list.d/jenkins.list > /dev/null
```
```sh
sudo apt-get update
```
```sh
sudo apt-get install jenkins
```
# Step -3 Start jenkins
```sh
sudo systemctl enable jenkins
```
```sh
sudo systemctl start jenkins
```
```sh
sudo systemctl status jenkins
```
# Step - 4 Open port 8080 from AWS Console:



