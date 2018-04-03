# AWS-Instance-type-change
#Changing the Instance type through AWS Lambda using Python boto3
The available python script can be run through AWS Lambda. 
This is the basic script which allow us to change the Instance type by specifying the Instance ID that want to be change the Type.

Script function:

Step 1: It will first stop the running Instance
Step 2: Once stopped it wait for 10 seconds and then it performs the modify Instance Type as specified
Step 3: Once the Instance type is changed it will again wait for 60 Seconds and then start the respective Instance


