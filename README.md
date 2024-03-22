# Task-management-Api

OVERVIEW--
1) This is Task Management System project.
2) In this prject you can add Task into the database and update that task into the database if you are a authorised user.
3) In this project I have integrated a best authentication which help in providing the access control on API.
--------------------------------------------------------------------------------------------------------------------------------------------

Models**
1)User
  1) In this entity there will be a userId , username , Role , password.
  2) role can be different type.(User , Admin).
  3) by using signup process you can add the user into the database.

2)Task
  1) Task is very important entity in this project.
  2) you can add the task with he help of user into the databse. you can update the task delete the task from the databse.
  3)In the task there will be title , description , status , dueDate.
  
3)Role
 1. There will be id , name of role.
 2. name of the role can be use , admin.
 
-------------------------------------------------------------------------------------------------------------------------------------------------
Relationship**
1. User has relationship of @OneToMany with the Task. Because user can have many task but task can be given to one user only. 
2. User can update their task and can delete their task also.

-------------------------------------------------------------------------------------------------------------------------------------------------
User Registration, User Login and Authorization process****
->1)User Resistration
  1. Post-api/auth/signup
  2. (username , role , password , email)
  3 after htting this api server wil check existing of user and save into the database.
->2)User Login
  1. Post-api/auth/signin
  2. (username , password)
  3. after hitting this api server will check about validation of user and send a Jwt token in form of response.
  
----------------------------------------------------------------------------------------------------------------------------------------------------

Project Endpoints****
  1)Post-api/test/addTask
    1. You can add the task into the Db by using this api. 
    2. you will be sending the rquest -AddTaskRquest(title , duedate , status , description username) in form of request  Body.
    3. after getting this request it project will check that username is valid or not , if it is not valid then it will throw an error that User is not exist.
    4. if username is true then it will send into the service and make the Task Object and set its all paramter and save it into the Database.

  2)Post-api/test/getAllTaskOfUser
    1. You can find the all task of a particular user.
    2. int this api you will sending the request -GetAllTaskRequest(username) in form of  request body.

  3)Put-api/test/updateTaskDetails
    1. You can update the task by using this api.
    2. you will be sending the request -TaskUpdateDetail(title , detail) int form of request body.

  4)Put-api/test/updateStatus
    1. You can update the status of task either it is completed ot not.
    2. For updating the task you will be sending the request -UpdateStatus(title , status) in form of request of body.
    3. after getting the Task with help of title and update the status.

  5)Delete-api/test/deleteTask
    1. You can delete the task from databse.
    2. For deleting the task from database , you will be getting the task with the help of title of task.

------------------------------------------------------------------------------------------------------------------------------------------------------------------




  

