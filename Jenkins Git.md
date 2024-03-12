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



![image](https://github.com/Asma09Akram/Jenkins/assets/124654068/9325150a-71bc-4177-a770-1b594e54b5a3)
