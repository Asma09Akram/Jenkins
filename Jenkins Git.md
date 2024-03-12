1. Create a new Freestyle Project

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/a0a1ed08-2e4e-4f4e-89f7-1fde191b3504)

2. Go down to Build Steps and click on Execute shell

write the following code, here when the build will generate it will clone the Github repo DemoProject and it will go inside DemoProject folder and then read the
contents of README.md and index.md


```
echo "Hello from Demo 3 Project"
ls
git clone https://github.com/Asma09Akram/DemoProject.git
cd DemoProject
cat README.md
cat index.html
```


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/30ab0db8-41ed-41d0-8672-662b8727e99a)


Click on green triangle

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/7841b573-7932-4f19-8996-6b22cb1159a2)




### Task 2. Create another project named as Demo 1 as Freestyle project

Under Source Code Management
select Git, paste the repo url in the space

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/644a612b-1c2a-447b-a12d-c4a37a4400b4)



![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/9325150a-71bc-4177-a770-1b594e54b5a3)

give branch as main as given in the repo

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/4b826db6-20d1-4893-8d59-737655c8d109)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/12a31a07-5391-40a1-89e3-e3635a389c8b)

Save 

* Then click on Build Now under left hand navigation

  ![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/2c56bac3-ed21-4ee2-a579-db389bcc46be)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/46eef58b-9288-4f0e-a1b5-1004c8616a33)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/716097a2-ab80-4187-b10e-45b7a5390b4b)


Now go and add a new line in README.md file and commit the changes.

Now in Jenkins I triggered Build Now and now the new changes starting reflecting on console output

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/5288df15-6877-4af8-a8a1-ea2ad41098d4)


### Task 3. Build trigger Remotely

* Click on the previous build which was generated in last step and click on Configure from left hand navigation panel.

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/4e600790-b1b6-4e57-aeac-d32c28787442)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/42c4625f-33dd-4d11-a888-77ce3c0bdd24)

Click on Apply and Save

Now we have to use the URL to build the job remotely

Use the following URL to trigger build remotely: JENKINS_URL/job/Demo%201/build?token=TOKEN_NAME or /buildWithParameters?token=TOKEN_NAME
Optionally append &cause=Cause+Text to provide text that will be included in the recorded build cause.

```
JENKINS_URL/job/Demo%201/build?token=TOKEN_NAME

http://3.83.82.140:8080/job/Demo%201/build?token=mysecrettoken
```

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/da8538fd-341a-4013-9d5e-72ce3235388f)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/6a3bef33-7bab-459f-9bb0-92c9a4426fb5)

Now it will show a new build is triggered by Remote IP

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/180d2fad-ddf7-4d96-b531-472cec2caf33)



