# Jenkins
##### Guidelines for beginner


### Notes

##### Started on the Jenkins tutorial by reading the documentation first on their official website to get preview with a better understanding on the tools. It took me 2 days  to read and understand it. I am installing my jenkins on my WSL2 Ubuntu. This installation guideline is the one that [I refer.](https://www.jenkins.io/doc/book/installing/linux/)


#### After finished installing, I checked the jenkins status if it is running using the command below on the terminal.

```bash
    sudo service jenkins status
```

#### To start the jenkins, run the command below on the terminal.

```bash
    sudo service jenkins start
```

#### Recheck the status and the output in terminal should be like this.

![Image1](/Jenkins/jenkins%20command.PNG)

#### Then, you can access the jenkins using the URL http://localhost:8080/

####  For first time installation, a password will be given. To get the password, we access the directory where the password is store.

1.  Make sure to access the root to go to the directory using command below.

```bash
    sudo -s
``` 

2. Access the directory using command below.

```bash
    cd /var/lib/jenkins/secrets
```

```bash
    ls
```
3. Access the password file use command below.

```bash
    vim initialAdminPassword
```

4. Copy the password and paste it during the first setup.

5. To exit the file and exit the root use command below.

```bash
    :q
```
```bash
    exit
```

#### When the first time setup finish, you will be able to see Jenkins dashboard.


_____


## Steps in creating first job on Jenkins

1. At the Jenkins dashboard, click the new item menu like shown in image below.

![image2](/Jenkins/jenkins%201st%20job.PNG)

2. Next, enter any suitable project name, in my case put HelloWorld as the name. Then click on the freestyle project and click on button Ok.

![image3](/Jenkins/jenkins%201st%20job%20next%20step.PNG)

3. Other section, I did not modify anything and just leave it empty. Only theSourceCode Management and Build section is configure. On the Source Code Management, select Git and paste any repository URL that I wish to used. Here I used my own repository. It is a simple Hellow World Java project.

![image4](/Jenkins/jenkins%201st%20job%20next%20step2.PNG)

4. On the Build section, select on Excecute shell and enter the command like in the picture below. 

![image5](/Jenkins/jenkin%20wsl1.PNG)

### Side Notes
##### If you install Jenkins on your Windows local machine, make sure to select Execute Windows batch command. If your Jenkins is install on Mac OS, Linux or WSL2 select the on the Execute shell or the command is not executing and job could not be build.

![image6](/Jenkins/jenkin%20wsl3.PNG)

5. Then click Apply and Save. You will see dashboard like shown in picture below. Click Build Now to start building the job.

![image7](/Jenkins/jenkins%20build.PNG)

6. Then, you can checkout on the Build History to see if it is success or not. As shown in the picture below, my #9 job is success. To check the status on each of the job, you can click  on it.

![image8](/Jenkins/jenkins.PNG)

8. The dashboard of the job  will look like picture shown below. Click on the Console Output to check on the status of the jobs.

![image9](/Jenkins/jenkins%20check.PNG)

9. Like shown in the picture below, my jobs is success and output is shown in the console.

![image10](/Jenkins/jenkins%20result.PNG)


_____

