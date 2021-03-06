# Team-International-Backend (Deadline FRIDAY 10:00 GMT)


Task given: **Dockerized micro-service for showing a dashboard for logged in users**

### Django, Swagger, Docker and Django RestAPI and PYTHON 3 were  used.


1--Fork the project to your github account
    
2--Clone the repository in your local environement

3--Run this command `git remote add upstream https://github.com/Team-International-Backend/edit/master/README.md`
 
 
 Before running this please keep in mind you will need **Swagger, Docker, Django, and REST API.**
 
 
---------------------------------------**Run the following commands to install these plugins**------------------------------------------
 ```
 pip install django
 
 pip install django-rest-swagger
 
 pip install djangorestframework
 ```
 Docker : https://docs.docker.com/docker-for-windows/install/
 
 -----------------------------------------------------**Running the server**-------------------------------------------------------------

In your command prompt navigate to the original file directory where the manage.py script exists and run the following:

`python manage.py runserver`

Now the server is up and running on your local host on http://127.0.0.1:8000/


For more testing purposes please refer to the following

`python manage.py makemigrations` -> **creates migration files based on your models**

`python manage.py migrate` -> **will create the tables in your db based on the migration files created**

`python manage.py createsuperuser` -> **will create a superuser for your application in the database**

-------------------------------------------------------**Accessing Swagger**-----------------------------------------------------------


If you would like to navigate to swagger please go to http://127.0.0.1:8000/docs

--------------------------------------------------**Configuring Swagger with Django 3.0**------------------------------------------------
!PLEASE NOTE: Swagger is currently facing problems with Django 3.0 or above, This problem is within the base swagger installation files on your local machine so there isn't really much we can do to fix it BUT we can always provide instructions :) 
When trying to navigate to http://127.0.0.1:8000/docs you will be greeted with a static file error to fix it simply do the following:

-navigate to `C:\Users\YOURNAME\AppData\Local\programs\python\python38\lib\site-packages\rest-framework-swagger\index.html`

-Open the HTML file in any text editor and navigate to line 2

Change `{% load staticfiles %} to {% load static %}`

-Back in the terminal press `Ctrl+C` to stop the server and run the server again.

And now Swagger will work, A ticket about this issue was open and answered by one of our team members here https://github.com/unioslo/mreg/issues/395


-------------------------------------------------------**Accessing the API**---------------------------------------------------------------

You can also visit the rest API by visiting http://127.0.0.1:8000/api 

http://127.0.0.1:8000/api/team-international/users/logged (it returns the already logged in users)




------------------------------------------------------------**Docker**------------------------------------------------------------------

1--Download and Install docker on your local machine,

2--Run the following commands on your terminal(Linux) or command prompt(Windows):

3--Test if docker is well installed by using this command : `docker --version` (it should display the docker's version installed).
        
 NOTE:In the root project folder you will notice **two files**, **Dockerfile** and **Docker-compose.yml** files.
        
4--Run this command: `docker-compose up` (It will build the image and run it using instructions in Dockerfile and Docker-              compose.yml files)
          
 This action **might take time** because; all dependencies like Django RestApi,Swagger...has to be downloaded as well.
        
 A the end of this process,The microservice will be running in the docker container and listenning to the port:8000
       (This port was configured in the  Docker-compose.yml file [line-5])


 
