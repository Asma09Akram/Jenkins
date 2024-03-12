

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/b31eb371-e3af-45f9-a01a-fc6c6c57a0c7)

Install Docker on EC2
```
sudo apt install docker.io
```
![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/443629ce-34d5-4204-ad63-a810fdb98327)


Installing docker on EC2 is done by Ansible which is a configuration management tool.

Now create a new Freestyle project 
Give the github repo name

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/ff8a6f0b-6dcf-41a1-9740-d3a2c8a1c98f)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/43050575-1644-432d-bfd6-f05bceddb903)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/9e62e91f-d7f5-43a7-b00f-e97b417d34c5)

```
echo "=============DEVOPS CICD STARTED ==================="
echo "CICD Started by User"
whoami
echo "Code Stage"
echo "Build Stage"
docker build -t django-app .

echo "Test Stage"

echo "Deploy Stage"
docker run -d -p 8000:8000 django-app:latest
```

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/aff89078-343b-4e60-ac56-fe37c99df461)

Apply and Save

Then Build Now

Build Failed

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/2e11c7a7-cecf-4730-9af2-51b028e9e5b5)

Got error 
permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock:

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/784f94e1-4ef0-4ff0-a526-523221b6686e)

We will now add Jenkins users to Docker group so that the Docker commands can be run correctly

```
sudo reboot
```
Connect to EC2 instance again and login to Jenkins and click on Build Now.
This time it has ran successfully


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/e0a8540a-70a4-4288-b82c-3e20009e02d6)

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/c474a77b-3add-40cb-995b-afedf1d00a70)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/6e837548-f00c-45c9-8135-85faa6eb987e)


Add a new inbound rule in Security Group of EC2 instance, allowing port 8000 to be accessed from Anywhere

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/eb36c662-2ee2-4101-9e90-4dc7b4a7b460)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/495e690a-e4d2-43bf-88db-e13894f53053)

