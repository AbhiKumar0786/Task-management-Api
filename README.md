# Task-management-Api

OVERVIEW--
1) This is Task Management System project.
2) In this prject you can add Task into the database and update that task into the database if you are a authorised user.
3) In this project I have integrated a best authentication which help in providing the access control on API.

----------------------------------------------------------------------------------------------------------------------------------------------
Models**
1)User
  i) In this entity there will be a userId , username , Role , password.
  ii) role can be different type.(User , Admin).
  iii) by using signup process you can add the user into the database.

2)Task
  i) Task is very important entity in this project.
  ii) you can add the task with he help of user into the databse. you can update the task delete the task from the databse.
  iii)In the task there will be title , description , status , dueDate.
  
3)Role
 i)There will be id , name of role.
 ii) name of the role can be use , admin.
 
 ----------------------------------------------------------------------------------------------------------------------------------------------
Relationship**
1)User has relationship of @OneToMany with the Task. Because user can have many task but task can be given to one user only. 
2) User can update their task and can delete their task also.

-----------------------------------------------------------------------------------------------------------------------------------------------
User Registration, User Login and Authorization process.----
->User Resistration
  i)Post-api/auth/signup
  ii)(username , role , password , email)
  iii) after htting this api server wil check existing of user and save into the database.
->User Login
  i)Post-api/auth/signin
  ii)(username , password)
  iii) after hitting this api server will check about validation of user and send a Jwt token in form of response.
  
--------------------------------------------------------------------------------------------------------------------------------------------------
Project Endpoints...----
  1)Post-api/test/addTask
    i) You can add the task into the Db by using this api. 
    ii) you will be sending the rquest -AddTaskRquest(title , duedate , status , description username) in form of request  Body.
    iii) after getting this request it project will check that username is valid or not , if it is not valid then it will throw an error that User is not exist.
    iv) if username is true then it will send into the service and make the Task Object and set its all paramter and save it into the Database.

  2)Post-api/test/getAllTaskOfUser
    i) You can find the all task of a particular user.
    ii) int this api you will sending the request -GetAllTaskRequest(username) in form of  request body.

  3)Put-api/test/updateTaskDetails
    i) You can update the task by using this api.
    ii) you will be sending the request -TaskUpdateDetail(title , detail) int form of request body.

  4)Put-api/test/updateStatus
    i) You can update the status of task either it is completed ot not.
    ii) For updating the task you will be sending the request -UpdateStatus(title , status) in form of request of body.
    iii) after getting the Task with help of title and update the status.

  5)Delete-api/test/deleteTask
    i) You can delete the task from databse.
    ii) For deleting the task from database , you will be getting the task with the help of title of task.
  
  --------------------------------------------------------------------------------------------------------------------------------------------------------











  

