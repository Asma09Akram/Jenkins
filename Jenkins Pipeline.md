## What is a Jenkins Pipeline?
Jenkins Pipeline (or simply "Pipeline") is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins.
A continuous delivery pipeline is an automated expression of your process for getting software from version control right through to your users and customers.
Jenkins Pipeline provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code". The definition of a Jenkins Pipeline is typically written into a text file 
(called a Jenkinsfile) which in turn is checked into a project’s source control repository.

1. Click on New item
Give any name, click on Freestyle project, click on Ok

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/26567148-a699-4ad7-9f42-aad29feddc83)

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/a10819e3-31a6-494e-a727-1f7e41c7d822)


Go down to Build Steps and click on Execute shell
```
echo "Hello from My Demo freestyle project"
```

Click on Apply and Save

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/e88a5c4a-99f0-4a64-a904-cfc5abeb4436)

Go back to the Dashboard

* Click on Green Triangle and it will do the Build Now action
  
![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/c0cdf433-cf7f-4730-8c00-6d8032f427f5)

If we click on Build history it will show 

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/04551f44-830b-497c-b246-e95204be5050)


![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/0fb76384-9753-4537-b7df-a4012db82b41)

Click on Console Output

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/add5627c-2028-44f8-822d-b29ca27df30d)


Made some changes like whoami and pwd in manage configurations

![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/c93b6bdc-2772-44b4-a745-47566521c41b)

