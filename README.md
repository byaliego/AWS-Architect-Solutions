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
    <blockquote> Create a route table entry for the endpoint + Create a gateway endpoint for DynamoDB.
  
    </blockquote>
    </br></br>
    </details>
    
    
    ___



   <details>
    <summary>
    ❓ A company's legacy application is currently relying on a single-instance Amazon RDS MySQL database without encryption. Due to new compliance requirements, all existing and new data in this database must be encrypted.
How should this be accomplished?  </summary>
    </br></br>
    <blockquote> Take a Snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot.
  
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
    ❓ A manufacturing company wants to implement predictive maintenance on its machinery equipment. The company will install thousands of IoT sensors that will send data to AWS in real time. A solutions architect is tasked with implementing a solution that will receive events in an ordered manner for each machinery asset and ensure that data is saved for further processing at a later time.  </summary>
    </br></br>
    <blockquote>  Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.
  
    </blockquote>
    </br></br>
    </details>

___
