Threads Is a intentionally designed Vulnerable Web Application by Enciphers Team.
  
# Prerequisite for setting up the Lab
 
## Install Node.js for your system

Check these commands

node -v

npm -v

## Install MongoDB

NOTE: Be careful while installing mongodb, as if the installation is not done properly the debugging of the error is very tedious. Installation guide [Setup guide](https://akarsh-enciphers.github.io/beta-Threads/setup/)

## Setting Up the project

1 Run the command "git clone https://github.com/enciphers/ThreadsApp.git"
2 cd ThreadsApp
3 Open the "config.env" file and fill in the required details from your aws account. The application won't run if all information is not filled in. 


```
     key=value

    JWT_KEY=thr3@ds@000
     multer s3 configuration
    ACCESSKEYID= add_your_ACCESSKEYID
    SECRETACCESSKEY= add_your_SECRETACCESSKEY
    REGION= SECRETACCESSKEY_aws_REGION
    BUCKET_NAME= add_your_BUCKET_NAME
```

For the AWS s3 bucket, you need to create the account on AWS and create the s3 bucket and fill the ACCESSKEYID, SECRETACCESSKEY, REGION, BUCKET_NAME values of your account :
nano config.env

Install dependencies

4) Run the command "npm install" in the "Threads" folder to install all dependencies required for API.
5) Run the command "npm run client_install" to install all dependencies of react app.

Note: If it does not ask you to add dummy users while following the above steps,run the command below command to add dummy users

To add dummy users : run “npm run add_users”

How to run Web Application:

6) Run the command "npm start" to start the application. The application will run on "http://localhost:3000/".

## Starting the Project

npm start

You should see a message Connected to Moongose in the terminal, if that's the case then the project setup is done and all the prerequisites were installed properly if that's not the case, create an issue with the error and screenshot.
Using the application

Visit --> http://localhost:3000/home

NOTE:

+ Filling all information in both environment files is necessary to run the app.

+ Admin email address is "admin@threadsapp.co.in". You can visit "http://localhost:3000/management" for the admin page.

+ For the AWS s3 bucket, you need to fill correct information in the "config.env" file.

+ User profile pictures are saved in the "uploads" folder.

+ Post pictures are uploaded on s3 bucket.

+ You will get the option to add dummy data while installing dependencies of API. It will create 25 users and 25 posts and this user will follow each other randomly.

Follow all the steps properly to run the application.

You can use the command "npm run add_users" to add dummy data again. New dummy data will replace old dummy data.
The app is designed to add some random dummy users and posts when the app us being installed. You will be asked whether you want to add the dummy data or not, while the app set up is being done.

Some points about the app:

+ All Users and New Users section will show all other users, but yourself.

+ Want to use a live version of the app {Hosted by Enciphers}, for training? Drop us an email at training@enciphers.com

Threads
![alt text](http://url/to/img.png)

# Prerequisite for setting up the Lab
 
##  Install Node.js for your system
 
Check these commands

```
node -v
npm -v
```
 
##  Install MongoDB
 
NOTE: Be carefull while installing mongodb, as if the installation is not done properly the debugging of the error is very tedious.
 
## Setting Up the project
 
```
1) Run the command "git clone https://github.com/enciphers/ThreadsApp.git"
2) cd Threads
3) Open the "config.env" file and fill in the required information given in the file. The application won't run if all information is not filled in. For the AWS s3 bucket, you need to create the account on AWS and create the s3 bucket and fill the ACCESSKEYID, SECRETACCESSKEY, REGION, BUCKET_NAME values of your account.
4) Run the command "npm install" in the "Threads" folder to install all dependencies required for API.
5) Run the command "npm run client_install" to install all dependencies of react app.
5) Go to the client folder and open the ".env" file. Fill in the required information in the file. The port in the value of the variable "REACT_APP_API_BASE_URL"  should be equal to the value of "PORT" in the "config.env" file of the Threads folder.
6) Run the command "npm start" to start the application. The application will run on "http://localhost:3000/".Here "3000" is the value of the "PORT" provides the ".env" file in the client folder. So you need to replace the value of "3000" with the value of "PORT" in the ".env" file of the client.
"3000" is the default value of "PORT".
```
 
## Starting the Project
 
```
npm start
```
 
You should see a message `Connected to Moongose` in the terminal, if that's the case then the project setup is done and all the prerequisite were installed properly
if that's not the case, create an issue with the error and screenshot.
 
#### Using the application
 
```
Visit --> http://localhost:3000/home
Here "3000" is the value of the "PORT" provides the ".env" file in the client folder. So you need to replace the value of "3000" with the value of "PORT" in the ".env" file of the client.
"3000" is the default value of "PORT".
Create some users, then signin, play with API's etc
```
 
### NOTE:
 
1. Filling all information in both environment files is necessary to run the app.
2. Admin email address is "[admin@threadsapp.co.in](mailto:admin@threadsapp.co.in)". You can visit "http://localhost:3000/management" for the admin page.
3. For the AWS s3 bucket, you need to fill correct information in the "config.env" file.
4. User profile pictures are saved in the "uploads" folder.
5. Post pictures are uploaded on s3 bucket.
6. You will get the option to add dummy data while installing dependencies of API. It will create 25 users and 25 posts and this user will follow each other randomly.
7. Follow all the steps properly to run the application.
8. You can use the command "npm run add_users" to add dummy data again. New dummy data will replace old dummy data.
9. The app is designed to add some random dummy users and posts when the app us being installed. You will be asked whether you want to add the dummy data or not, while the app set up is being done. 
 
### Some points about the app:

1. All Users and New Users section will show other users, but not yourself. 
2. Want to use a live version of the app {Hosted by Enciphers}, for training? Drop us an email at training@enciphers.com
 
 
 
--------------------
 
 
