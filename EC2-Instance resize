import boto3
import time 
 
cl = boto3.client('ec2')

my_instance = 'Instance ID'
region = 'us-east-1'

def lambda_handler(event, context):
   cl.stop_instances(InstanceIds=[my_instance])
   while True:
      rsp =  cl.describe_instance_status(InstanceIds=[str(my_instance)],IncludeAllInstances=True)
      state= rsp['InstanceStatuses'][0]['InstanceState']['Name']
      if state!="stopped":
         time.sleep(10)
      else :
         break
   cl.modify_instance_attribute(InstanceId=my_instance, Attribute='instanceType', Value='t2.micro')
   time.sleep(60)
   cl.start_instances(InstanceIds=[my_instance])
