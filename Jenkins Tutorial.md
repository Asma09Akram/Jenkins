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




![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/8f71dea9-29f0-4411-987b-37a66fc62a56)

Configuring Jenkins
Jenkins is now installed and running on your EC2 instance. To configure Jenkins:

Connect to http://<your_server_public_DNS>:8080 from your browser. You will be able to access Jenkins through its management interface:

http://3.81.214.171:8080/

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/355953bf-6439-42af-b0e0-317d04a61772)

As prompted, enter the password found in /var/lib/jenkins/secrets/initialAdminPassword.

Use the following command to display this password:
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

You will get the password from the above command


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/de36eb94-e2ce-4917-8a35-3914ccc45af6)

The Jenkins installation script directs you to the Customize Jenkins page. Click Install suggested plugins.

Once the installation is complete, the Create First Admin User will open. Enter your information, and then select Save and Continue.

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/54b35244-89fb-4b3c-91c9-58be4132b009)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/7e71976e-66c0-418e-a972-957d85103959)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/98791e05-c7a1-4155-84b8-9e1fcc488e7a)


http://3.81.214.171:8080/

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/eb1e2962-8719-4c7f-be01-a9e822031409)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/9069d1ad-c658-48ab-a42e-157dfa122377)

On the left-hand side, select Manage Jenkins, and then select Manage Plugins.

Select the Available tab, and then enter Amazon EC2 plugin at the top right.

Select the checkbox next to Amazon EC2 plugin, and then select Install without restart.

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/5351b279-bc80-41a9-9d8e-06d125b315f4)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/ec5196ab-a696-40b3-8c6a-bb109ff9d958)


Once the installation is done, select Back to Dashboard.

Select Configure a cloud if there are no existing nodes or clouds.

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/e9367f1d-4958-463d-8083-97068e81a47f)


If you already have other nodes or clouds set up, select Manage Jenkins.

Thats how Jenkins is installed and ready to use on EC2
