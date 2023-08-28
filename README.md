<h1>CloudWatch 101</h1>



<h2>Description</h2>
Welcome to the CloudWatch Learning Repository! In this repository, you'll find a comprehensive collection of resources and tutorials designed to help you master Amazon CloudWatch, a powerful monitoring and management service provided by Amazon Web Services (AWS). Whether you're new to CloudWatch or looking to deepen your understanding, this repository is your one-stop destination for all things CloudWatch.


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 


<h2>Environments Used </h2>

- <b>AWS</b> 

<h2>Project walk-through:</h2>

<p align="center"> 
 <h3> Cloudwatch Infrastructure Design  <h3/>
<img src="https://i.imgur.com/0zlV2Ik.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>
- CloudWatch sit in AWS Public zone and it store metrics (CPU, Disk, Request, Latency, Errors)
- Various on-premises services publish data into CloudWatch (On Premises VMS and Applications; Internet Connected Application)
-  VPC also publish data into CloudWatch too, connecting CloudWatch via Internet Gateway 
- Private instances can also connect via interface endpoint 
- Alarm ( SNS Notification, ASC Scaling, Eventbridge Event)

<h3> Cloudwatch Data  <h3/>
- Namespace = Container of metric e.g AWS/EC2, AWS/Lambda
- Data point = Timestamp, value, unit of measure 
- Metric = time ordered set of data point (CPUUtilazation, Networkln, DiskWriteByte (EC2)
- EveryMetric has a Metricname and a namespace
- Dimesion = name/value pair
- Resolution =  Standard (60s), high (1)
- Retention = its aggrated and stored for longer less resolution 
- Statistic = aggregation over a period (Min, MAX, SUM, Average)
- Alarm = watches a metric over time of period (value of metric vs threshold overtime, one or more actions)
<img src="https://i.imgur.com/DGHJjRK.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>

<h3> Cloudwatch Logs - Ingestion <h3/>
- Public Service, Store, Monitor, Access Logging Data
- AWS, On-Premises, IOT or any application 
- CWAgent - system or custom application logging 
- VPC Flow Logs 
- CloudTrail .. Account Event and AWS API Calls
- Elastric BeanTalk, ECS Container Logs, API GW, Lamda Execution Logs
- Route 53 - Log DNS Requests
<img src="https://i.imgur.com/peXjjbd.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>


<h3> Cloudwatch Logs - Subscription  <h3/>

<img src="https://i.imgur.com/2uTPAM7.png" height="80%" width="80%" alt="Building and Securing an AWS VPC Steps"/>

