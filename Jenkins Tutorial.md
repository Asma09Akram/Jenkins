### Task 1. Launch an EC2 Ubuntu instance and connect to it.
* In the Security Group, Inbound rules allow SSH, HTTP, HTTPS
* Custome TCP and enter My IP


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/4761a2a0-4aad-4978-a2e4-77da6db51bfe)

### Task 2. Install Jenkins on EC2

https://www.jenkins.io/doc/book/installing/linux/#debianubuntu
* Install Java first and then install Jenkins otherwise it will give error when you start Jenkins
  
```
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
```

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/2b4036d1-1ff3-44c9-b2a3-40a427387a6d)


* Install Jenkins
* Long Term Support release
A LTS (Long-Term Support) release is chosen every 12 weeks from the stream of regular releases as the stable release for that time period. It can be installed from the debian-stable apt repository.

```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

```


Start Jenkins
You can enable the Jenkins service to start at boot with the command:

```
sudo systemctl enable jenkins
```

You can start the Jenkins service with the command:
```
sudo systemctl start jenkins
```
You can check the status of the Jenkins service using the command:
```
sudo systemctl status jenkins

```

Configuring Jenkins
Jenkins is now installed and running on your EC2 instance. To configure Jenkins:

Connect to http://<your_server_public_DNS>:8080 from your browser. You will be able to access Jenkins through its management interface:

http://3.81.214.171:8080/


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/8f71dea9-29f0-4411-987b-37a66fc62a56)



![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/355953bf-6439-42af-b0e0-317d04a61772)
