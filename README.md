* The main purpose of my project is to, whenever my production server reaches its CPU limits, send an automatic notification to my email ID.
* For this project, I used two new services from the AWS. 
*cloudwatch
*sns (simple notification services).
*First create one EC2 instance. 
* Then go to the cloud watch services in AWS. 
*Next, go to the alarms section and create alarms, then click on select metrics.
*Click on EC2 instances and then select the per instance 
*Select your EC2 instances CPU utilization in the cloud watch.
*In the next page, you can set the limit by statistic and period. In the condition tab, you can set the limit.
*Click next
*In the next step, you can select the alrams and SNs (simple notification services) as services. 
*And then configure with your mail ID and click Create Alarms.
********Setting up my EC2 instances*********
sudo apt update
sudo apt install stress
stress --cpu 4 --timeout 60
Cammonds used to manually triger my instances to reach its CPU utilization limits.
*And I recevied the mail from my cloudwatch services that my EC2 instances reached their CPU utilization limits.
