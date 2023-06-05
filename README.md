# AWS-Architect-Solutions



  <details>
    <summary>
      ❓ A Solutions Architect identified a series of DDoS attacks while monitoring the VPC. The Architect needs to fortify the current cloud infrastructure to protect the data of the clients. He needs a solution to mitigate these kinds of attacks.</summary>
  </br></br>
         <blockquote> Use AWS Shield Advanced to detect and mitigate DDoS attacks.</blockquote>
  </br></br>
  </details>
  
  ___
  
   <details>
    <summary>
    ❓ A telecommunications company is planning to give AWS Console access to developers. Company policy mandates the use of identity federation and role-based access control. Currently, the roles are already assigned using groups in the corporate Active Directory.
    In this scenario, what kind of the services can provide developers access to the AWS console? </summary>
    </br></br>
    <blockquote> Considering that the company is using a corporate Active Directory, it is best to use AWS Directory Service AD Connector for easier integration.    In addition, since the roles are already assigned using groups in the corporate Active Directory, it would be better to also use IAM Roles. Take note that you can assign an IAM Role to the users or groups from your Active Directory once it is integrated with your VPC via the AWS Directory Service AD Connector.
    </blockquote>
    </br></br>
    </details>

___

   <details>
    <summary>
    ❓ A company's web application uses an Amazon RDS PostgreSQL DB instance to store its application data. During the financial closing period at the start of every month, Accountants run large queries that impact the database's performance due to high usage. The company wants to minimize the impact that the reporting activity has on the web application.
What should a solutions architect do to reduce the impact on the database with the LEAST amount of effort? </summary>
    </br></br>
    <blockquote> Amazon RDS uses the MariaDB, MySQL, Oracle, PostgreSQL, and Microsoft SQL Server DB engines' built-in replication functionality to create a special type of
DB instance called a read replica from a source DB instance. Updates made to the source DB instance are asynchronously copied to the read replica. You can reduce the load on your source DB instance by routing read queries from your applications to the read replica.
When you create a read replica, you first specify an existing DB instance as the source. Then Amazon RDS takes a snapshot of the source instance and creates a read-only instance from the snapshot. Amazon RDS then uses the asynchronous replication method for the DB engine to update the read replica whenever there is a change to the source DB instance. The read replica operates as a DB instance that allows only read-only connections. Applications connect to a read replica the same way they do to any DB instance. Amazon RDS replicates all databases in the source DB instance.
    </blockquote>
    </br></br>
    </details>

___


   <details>
    <summary>
    ❓ A company's application is running on Amazon EC2 instances in a single Region. In the event of a disaster, a solutions architect needs to ensure that the resources can also be deployed to a second Region.
Which combination of actions should the solutions architect take to accomplish this? </summary>
    </br></br>
    <blockquote>  Launch a new EC2 instance from an Amazon Machine Image (AMI) in a new Region + Copy an Amazon Machine Image (AMI) of an EC2 instance and specify a different Region for the destination.
   Amazon Machine Image (AMI) Copy. AMI Copy enables you to easily copy your Amazon Machine Images between AWS
Regions. AMI Copy helps enable several key scenarios including:
Simple and Consistent Multi-Region Deployment ג€" You can copy an AMI from one region to another, enabling you to easily launch consistent instances based on the same AMI into different regions.
Scalability ג€" You can more easily design and build world-scale applications that meet the needs of your users, regardless of their location.
Performance ג€" You can increase performance by distributing your application and locating critical components of your application in closer proximity to your users.
You can also take advantage of region-specific features such as instance types or other AWS services.
Even Higher Availability ג€" You can design and deploy applications across AWS regions, to increase availability.
Once the new AMI is in an Available state the copy is complete.
    </blockquote>
    </br></br>
    </details>

___



   <details>
    <summary>
    ❓ A solutions architect needs to ensure that API calls to Amazon DynamoDB from Amazon EC2 instances in a VPC do not traverse the internet.
What should the solutions architect do to accomplish this?  </summary>
    </br></br>
    <blockquote>
  
  Create a route table entry for the endpoint + Create a gateway endpoint for DynamoDB.
  </blockquote>
    </br></br>
    </details>
    
    
___



   <details>
    <summary>
    ❓ A company's legacy application is currently relying on a single-instance Amazon RDS MySQL database without encryption. Due to new compliance requirements, all existing and new data in this database must be encrypted.
How should this be accomplished?  </summary>
    </br></br>
    <blockquote> 
  Take a Snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot.
  </blockquote>
    </br></br>
    </details>
    
    
  ___





   <details>
    <summary>
    ❓ A manufacturing company wants to implement predictive maintenance on its machinery equipment. The company will install thousands of IoT sensors that will send data to AWS in real time. A solutions architect is tasked with implementing a solution that will receive events in an ordered manner for each machinery asset and ensure that data is saved for further processing at a later time.  </summary>
    </br></br>
    <blockquote>  Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.
  </blockquote>
    </br></br>
    </details>

___


   <details>
    <summary>
    ❓ A company's website runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The website has a mix of dynamic and static content. Users around the globe are reporting that the website is slow.
Which set of actions will improve website performance for users worldwide?  </summary>
    </br></br>
    <blockquote>   Create an Amazon CloudFront distribution and configure the ALB as an origin. Then update the Amazon Route 53 record to point to the CloudFront distribution.
  </blockquote>
    </br></br>
    </details>

___



   <details>
    <summary>
    ❓ A company has been storing analytics data in an Amazon RDS instance for the past few years. The company asked a solutions architect to find a solution that allows users to access this data using an API. The expectation is that the application will experience periods of inactivity but could receive bursts of traffic within seconds.
Which solution should the solutions architect suggest?

  </summary>
    </br></br>
    <blockquote>    Set up an Amazon API Gateway and use AWS Lambda functions.
  </blockquote>
    </br></br>
    </details>

___




  <details>
    <summary>
    ❓ A company must generate sales reports at the beginning of every month. The reporting process launches 20 Amazon EC2 instances on the first of the month. The process runs for 7 days and cannot be interrupted. The company wants to minimize costs.
Which pricing model should the company choose?



  </summary>
    </br></br>
    <blockquote>   Scheduled Reserved Instances (Scheduled Instances) enable you to purchase capacity reservations that recur on a daily, weekly, or monthly basis, with a specified start time and duration, for a one-year term. You reserve the capacity in advance, so that you know it is available when you need it. You pay for the time that the instances are scheduled, even if you do not use them.
Scheduled Instances are a good choice for workloads that do not run continuously, but do run on a regular schedule. For example, you can use Scheduled
Instances for an application that runs during business hours or for batch processing that runs at the end of the week.
If you require a capacity reservation on a continuous basis, Reserved Instances might meet your needs and decrease costs.

How Scheduled Instances Work -
Amazon EC2 sets aside pools of EC2 instances in each Availability Zone for use as Scheduled Instances. Each pool supports a specific combination of instance type, operating system, and network.
To get started, you must search for an available schedule. You can search across multiple pools or a single pool. After you locate a suitable schedule, purchase it.
You must launch your Scheduled Instances during their scheduled time periods, using a launch configuration that matches the following attributes of the schedule that you purchased: instance type, Availability Zone, network, and platform. When you do so, Amazon EC2 launches EC2 instances on your behalf, based on the specified launch specification. Amazon EC2 must ensure that the EC2 instances have terminated by the end of the current scheduled time period so that the capacity is available for any other Scheduled Instances it is reserved for. Therefore, Amazon EC2 terminates the EC2 instances three minutes before the end of the current scheduled time period.
You can't stop or reboot Scheduled Instances, but you can terminate them manually as needed. If you terminate a Scheduled Instance before its current scheduled time period ends, you can launch it again after a few minutes. Otherwise, you must wait until the next scheduled time period.
  </blockquote>
    </br></br>
    </details>

___

  <details>
    <summary>
      ❓ A gaming company has multiple Amazon EC2 instances in a single Availability Zone for its multiplayer game that communicates with users on Layer 4. The chief technology officer (CTO) wants to make the architecture highly available and cost-effective.
What should a solutions architect do to meet these requirements? </summary>
  </br></br>
         <blockquote>  Configure a Network Load Balancer in front of the EC2 instances + Configure an Auto Scaling group to add or remove instances in multiple Availability Zones automatically.</blockquote>
  </br></br>
  </details>
  
  ___
  
  
  
   <details>
    <summary>
      ❓A company that hosts its web application on AWS wants to ensure all Amazon EC2 instances. Amazon RDS DB instances. and Amazon Redshift clusters are configured with tags. The company wants to minimize the effort of configuring and operating this check.
What should a solutions architect do to accomplish this?</summary>
  </br></br>
         <blockquote>   Use AWS Config rules to define and detect resources that are not properly tagged. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
   <details>
    <summary>
      ❓A development team needs to host a website that will be accessed by other teams. The website contents consist of HTML, CSS, client-side JavaScript, and images.
Which method is the MOST cost-effective for hosting the website?</summary>
  </br></br>
         <blockquote>   Create an Amazon S3 bucket and host the website there. </blockquote>
  </br></br>
  </details>
  
  ___
  
    
   <details>
    <summary>
      ❓A company runs an online marketplace web application on AWS. The application serves hundreds of thousands of users during peak hours. The company needs a scalable, near-real-time solution to share the details of millions of financial transactions with several other internal applications. Transactions also need to be processed to remove sensitive data before being stored in a document database for low-latency retrieval.
What should a solutions architect recommend to meet these requirements?</summary>
  </br></br>
         <blockquote>   Stream the transactions data into Amazon Kinesis Data Streams. Use AWS Lambda integration to remove sensitive data from every transaction and then store the transactions data in Amazon DynamoDB. Other applications can consume the transactions data off the Kinesis data stream. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
      
   <details>
    <summary>
      ❓A company hosts its multi-tier applications on AWS. For compliance, governance, auditing, and security, the company must track configuration changes on its AWS resources and record a history of API calls made to these resources.
What should a solutions architect do to meet these requirements?</summary>
  </br></br>
         <blockquote>    Use AWS Config to track configuration changes and AWS CloudTrail to record API calls.</blockquote>
  </br></br>
  </details>
  
  ___
  
  
     
   <details>
    <summary>
      ❓A company is preparing to launch a public-facing web application in the AWS Cloud. The architecture consists of Amazon EC2 instances within a VPC behind an Elastic Load Balancer (ELB). A third-party service is used for the DNS. The company's solutions architect must recommend a solution to detect and protect against large-scale DDoS attacks.
Which solution meets these requirements?</summary>
  </br></br>
         <blockquote>    Enable AWS Shield Advanced and assign the ELB to it. </blockquote>
  </br></br>
  </details>
  
  
   ___
  
  
     
   <details>
    <summary>
      ❓A company is hosting a static website on Amazon S3 and is using Amazon Route 53 for DNS. The website is experiencing increased demand from around the world. The company must decrease latency for users who access the website.
Which solution meets these requirements MOST cost-effectively?</summary>
  </br></br>
         <blockquote>    Add an Amazon CloudFront distribution in front of the S3 bucket. Edit the Route 53 entries to point to the CloudFront distribution. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
   <details>
   <summary>
      ❓A company maintains a searchable repository of items on its website. The data is stored in an Amazon RDS for MySQL database table that contains more than 10 million rows. The database has 2 TB of General Purpose SSD storage. There are millions of updates against this data every day through the company's website.
The company has noticed that some insert operations are taking 10 seconds or longer. The company has determined that the database storage performance is the problem.
Which solution addresses this performance issue?</summary>
  </br></br>
         <blockquote>     Change the storage type to Provisioned IOPS SSD. </blockquote>
  </br></br>
  </details>
  
  ___
  


   <details>
    <summary>
      ❓A company has thousands of edge devices that collectively generate 1 TB of status alerts each day. Each alert is approximately 2 KB in size. A solutions architect needs to implement a solution to ingest and store the alerts for future analysis.
The company wants a highly available solution. However, the company needs to minimize costs and does not want to manage additional infrastructure. Additionally, the company wants to keep 14 days of data available for immediate analysis and archive any data older than 14 days.
What is the MOST operationally efficient solution that meets these requirements?</summary>
  </br></br>
         <blockquote>    Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the Kinesis Data Firehose stream to deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to transition data to Amazon S3 Glacier after 14 days. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
   <details>
    <summary>
      ❓A company's application integrates with multiple software-as-a-service (SaaS) sources for data collection. The company runs Amazon EC2 instances to receive the data and to upload the data to an Amazon S3 bucket for analysis. The same EC2 instance that receives and uploads the data also sends a notification to the user when an upload is complete. The company has noticed slow application performance and wants to improve the performance as much as possible.
Which solution will meet these requirements with the LEAST operational overhead?</summary>
  </br></br>
         <blockquote>    Create an Amazon AppFlow flow to transfer data between each SaaS source and the S3 bucket. Configure an S3 event notification to send events to an Amazon Simple Notification Service (Amazon SNS) topic when the upload to the S3 bucket is complete. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
    
   <details>
    <summary>
      ❓ A company runs a highly available image-processing application on Amazon EC2 instances in a single VPC. The EC2 instances run inside several subnets across multiple Availability Zones. The EC2 instances do not communicate with each other. However, the EC2 instances download images from Amazon S3 and upload images to Amazon S3 through a single NAT gateway. The company is concerned about data transfer charges.
What is the MOST cost-effective way for the company to avoid Regional data transfer charges?</summary>
  </br></br>
         <blockquote>    Deploy a gateway VPC endpoint for Amazon S3. </blockquote>
  </br></br>
  </details>
  
  ___



  
    
   <details>
    <summary>
      ❓A company has an on-premises application that generates a large amount of time-sensitive data that is backed up to Amazon S3. The application has grown and there are user complaints about internet bandwidth limitations. A solutions architect needs to design a long-term solution that allows for both timely backups to Amazon S3 and with minimal impact on internet connectivity for internal users.
Which solution meets these requirements?</summary>
  </br></br>
         <blockquote>    Establish a new AWS Direct Connect connection and direct backup traffic through this new connection. </blockquote>
  </br></br>
  </details>
  
  ___
  
  
   <details>
    <summary>
      ❓A company has an Amazon S3 bucket that contains critical data. The company must protect the data from accidental deletion.
Which combination of steps should a solutions architect take to meet these requirements? </summary>
  </br></br>
         <blockquote>    Enable MFA Delete on the S3 bucket + Enable versioning on the S3 bucket.  </blockquote>
  </br></br>
  </details>
  
  ___
  
  
  
    
  
   <details>
    <summary>
      ❓A company has a data ingestion workflow that consists of the following:
• An Amazon Simple Notification Service (Amazon SNS) topic for notifications about new data deliveries
• An AWS Lambda function to process the data and record metadata
The company observes that the ingestion workflow fails occasionally because of network connectivity issues. When such a failure occurs, the Lambda function does not ingest the corresponding data unless the company manually reruns the job.
Which combination of actions should a solutions architect take to ensure that the Lambda function ingests all data in the future? </summary>
  </br></br>
         <blockquote>    Create an Amazon Simple Queue Service (Amazon SQS) queue, and subscribe it to the SNS topic + Modify the Lambda function to read from an Amazon Simple Queue Service (Amazon SQS) queue. </blockquote>
  </br></br>
  </details>
  
  ___


    
  
   <details>
    <summary>
      ❓A company has an application that provides marketing services to stores. The services are based on previous purchases by store customers. The stores upload transaction data to the company through SFTP, and the data is processed and analyzed to generate new marketing offers. Some of the files can exceed 200 GB in size.
Recently, the company discovered that some of the stores have uploaded files that contain personally identifiable information (PII) that should not have been included. The company wants administrators to be alerted if PII is shared again. The company also wants to automate remediation.
What should a solutions architect do to meet these requirements with the LEAST development effort?

</summary>
  </br></br>
         <blockquote>   Use an Amazon S3 bucket as a secure transfer point. Use Amazon Macie to scan the objects in the bucket. If objects contain PII, use Amazon Simple Notification Service (Amazon SNS) to trigger a notification to the administrators to remove the objects that contain PII.  </blockquote>
  </br></br>
  </details>
  
  ___


  
  
   <details>
    <summary>
      ❓A company needs guaranteed Amazon EC2 capacity in three specific Availability Zones in a specific AWS Region for an upcoming event that will last 1 week.
What should the company do to guarantee the EC2 capacity?

</summary>
  </br></br>
         <blockquote>   Create an On-Demand Capacity Reservation that specifies the Region and three Availability Zones needed.  </blockquote>
  </br></br>
  </details>
  
  ___



   <details>
    <summary>
      ❓A company's website uses an Amazon EC2 instance store for its catalog of items. The company wants to make sure that the catalog is highly available and that the catalog is stored in a durable location.
What should a solutions architect do to meet these requirements?

</summary>
  </br></br>
         <blockquote>   Move the catalog to an Amazon Elastic File System (Amazon EFS) file system.  </blockquote>
  </br></br>
  </details>
  
  ___
  
  
  
  
   <details>
    <summary>
      ❓A company stores call transcript files on a monthly basis. Users access the files randomly within 1 year of the call, but users access the files infrequently after 1 year. The company wants to optimize its solution by giving users the ability to query and retrieve files that are less than 1-year-old as quickly as possible. A delay in retrieving older files is acceptable.
Which solution will meet these requirements MOST cost-effectively?
</summary>
  </br></br>
         <blockquote>   Store individual files in Amazon S3 Intelligent-Tiering. Use S3 Lifecycle policies to move the files to S3 Glacier Flexible Retrieval after 1 year. Query and retrieve the files that are in Amazon S3 by using Amazon Athena. Query and retrieve the files that are in S3 Glacier by using S3 Glacier Select.   </blockquote>
  </br></br>
  </details>
  
  ___
  
  
  
  
   <details>
    <summary>
      ❓A company has a production workload that runs on 1,000 Amazon EC2 Linux instances. The workload is powered by third-party software. The company needs to patch the third-party software on all EC2 instances as quickly as possible to remediate a critical security vulnerability.
What should a solutions architect do to meet these requirements?
</summary>
  </br></br>
         <blockquote>   Use AWS Systems Manager Run Command to run a custom command that applies the patch to all EC2 instances.   </blockquote>
  </br></br>
  </details>
  
  ___
