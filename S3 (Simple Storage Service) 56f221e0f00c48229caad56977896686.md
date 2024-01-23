# S3 (Simple Storage Service)

S3 is an **object storage** service that offer scalability, data availability, durable storage and performance. 

Create a simple web app that will need a relational and non relational databases, cache, an api, your own domain for the app and the api, send emails and have a process that needs to run in batches and queues, and have file storage. This simple project will teach you everything most companies use from AWS. The services you will use are RDS, dynamo, route 53, lambda functions, api gateway, ses, sqs, elastic cache, ec2 or elastic beanstalk, many IAM configs, and at the end, when you have domain over each service you can start learn about cloud formation.

## What is Object Storage?

Unlike traditional file systems, Object Storage organize data as object itself. Each object is stored in a single container, without complex file structure. Each object stored can have tag and metadata. This makes it accessible from anywhere in the world.

- [ ]  S3 provides high durability, ensuring that your data is maintained with 99.999999999% (11 9’s) durability over a given year.This means that the data is reliably stored and protected against loss.
- [ ]  S3 stores data in containers called buckets. You can think of a bucket like a top-level folder on a traditional hard drive, but with virtually unlimited capacity.

## **Bucket Metrics**

Bucket Metrics in Amazon S3 is an essential concept for understanding how to monitor and manage data stored in Amazon S3, a widely used cloud storage service provided by Amazon Web Services (AWS). The concept revolves around the collection and analysis of data related to S3 buckets, which are basic containers for storing data in S3. Let's break down this concept into simpler, more understandable terms and use real-life examples for clarity.

1. Understanding Amazon S3 and Buckets
Before diving into Bucket Metrics, it's important to understand what Amazon S3 and S3 buckets are. Imagine Amazon S3 as a huge, virtual storage space, like a gigantic online hard drive. Within this space, you can create "buckets." A bucket in Amazon S3 is similar to a folder on your computer, but it exists in the cloud. Each bucket can hold files (in S3, these are called objects), and you can have as many buckets as you need, each for different purposes.
2. What are Bucket Metrics?
Bucket Metrics in Amazon S3 are akin to a dashboard in a car. Just like how a dashboard tells you the speed, fuel level, and engine health, Bucket Metrics provide information about your S3 buckets. They offer insights into how the buckets are being used, how much data they contain, and other vital statistics. This information is crucial for managing your storage efficiently and keeping costs under control.
3. Key Metrics Tracked
Several key metrics are tracked in Amazon S3, including:

**Storage Usage:** Measures how much data is stored in each bucket. Imagine this like checking how much space is left in your closet.
**Number of Objects:** Counts the number of files (objects) in a bucket. It's like counting the number of books on a bookshelf.
**Data Transfer and Requests:** Tracks how often data is accessed or moved in and out of the bucket. Think of it as noting how many times you open a box to take something out or put something in.
Latency: Measures the time taken to complete a request, like how long it takes to retrieve a file. Similar to the time it takes to find a specific book in a library.

4. Real-Life Example
Let's use a real-life example to understand this better. Imagine you run a photography business and store all your photos in S3 buckets. Each project or event you cover has its own bucket. Bucket Metrics will help you understand:

How much space each event's photos are taking up.
How many photos are stored in each bucket.
How frequently you access photos from a particular event.
How quickly you can download or upload photos to and from each bucket.

5. Why are Bucket Metrics Important?
Understanding and monitoring these metrics is vital for several reasons:

**Cost Management:** By keeping an eye on storage usage and data transfer, you can manage costs more effectively, ensuring you're not paying for unused space or excessive data transfer.
**Performance Optimization:** Understanding access patterns and latency helps in optimizing the performance, ensuring faster access to frequently used data.
**Security and Compliance:** Tracking access patterns can also help in identifying unusual activities, potentially flagging security concerns.

6. How to Access and Use Bucket Metrics
Bucket Metrics are available through the AWS Management Console, a web interface provided by AWS. You can view these metrics in graphical forms and set up alerts if certain thresholds are reached, like receiving a notification when a bucket is almost full.

Conclusion

In summary, Bucket Metrics in Amazon S3 are like a sophisticated monitoring system for your cloud storage. They provide valuable insights into storage usage, access patterns, and overall performance, helping you manage your data more effectively and efficiently. By keeping a close eye on these metrics, you can ensure that your S3 usage aligns with your needs and budget, much like how you'd manage physical storage or resources in the real world.

Security Groups & Key pair (SSH)

## EC2 (Elastic Cloud Compute)

1. **EC2 Instances**: These are virtual servers in Amazon's Elastic Compute Cloud (EC2) for running applications. They're like having your own personal computer or server online. You can choose different sizes and capacities, depending on your needs (like choosing between a small laptop or a powerful desktop).
    - **Use Case**: Hosting web applications, running backend servers for mobile applications, or performing computational tasks.
    - **Example**: A startup can use an EC2 instance to host its website.
2. **Elastic Block Store (EBS)**: EBS provides block-level storage volumes for use with EC2 instances. Think of it as a hard drive that you can attach to your virtual server in the cloud.
    - **Use Case**: Storing database files, running software that requires quick access to data.
    - **Example**: An e-commerce website stores its product database on an EBS volume.
3. **Elastic Load Balancers (ELB)**: ELBs automatically distribute incoming application traffic across multiple targets, like EC2 instances. It's like having a traffic police officer who directs incoming cars (internet traffic) to various lanes (servers) to avoid congestion.
    - **Use Case**: Distributing web traffic across multiple servers to ensure high availability and fault tolerance.
    - **Example**: An online news portal uses ELB to manage high traffic during breaking news events.
4. **Auto Scaling Groups**: These help automatically adjust the number of EC2 instances you are using, based on the demand. Imagine a bus service that can automatically add more buses during rush hours and reduce them when it's quiet.
    - **Use Case**: Handling variable workloads, maintaining performance during peak times.
    - **Example**: An online store automatically scales up its servers during a sale event.
5. **Amazon Machine Images (AMI)**: AMIs are pre-configured templates for your instances, like a pre-built computer setup that includes the operating system and additional software.
    - **Use Case**: Quickly launching and scaling applications.
    - **Example**: Deploying a fleet of servers with a specific configuration for a new project.
6. **Snapshots**: These are backups of your EBS volumes. It's like taking a photograph of your data so that you can restore it later if needed.
    - **Use Case**: Data backup and recovery.
    - **Example**: Regularly taking snapshots of a database for backup purposes.
7. **Security Groups**: These act as a virtual firewall for your EC2 instances, controlling inbound and outbound traffic. Think of it as a security guard who checks who comes in and goes out of your building.
    - **Use Case**: Ensuring network security by controlling access to EC2 instances.
    - **Example**: Restricting access to a server to only certain IP addresses.
8. **Elastic IPs**: These are static IP addresses designed for dynamic cloud computing. Like having a permanent phone number for your business, even if you change locations.
    - **Use Case**: Having a fixed IP address for your application.
    - **Example**: Hosting a website that needs a constant IP address.
9. **Placement Groups**: These are ways to influence how instances are placed on the underlying hardware. It's like choosing a seat in a theater for the best view.
    - **Use Case**: Optimizing performance for high throughput or low latency.
    - **Example**: Deploying high-performance computing applications that need low network latency.
10. **Key Pairs**: These are used for secure login to your EC2 instances. Think of it like having a secure key to access your home.
    - **Use Case**: Securely logging into your instances.
    - **Example**: Admins accessing servers to deploy applications or perform maintenance.
11. **Network Interfaces**: These represent a network card for your EC2 instance. Just as your computer needs a network card to connect to the internet, EC2 instances use network interfaces to communicate.
    - **Use Case**: Managing networking aspects of EC2 instances.
    - **Example**: Setting up a network interface with specific security groups and IP addresses for a specialized application.
    
    ### **What are Security Groups in EC2?**
    
    Security Groups in Amazon EC2 act as a virtual firewall that controls the traffic for one or more instances. When you launch an instance, you associate one or more security groups with it. Each security group contains a set of rules that filter traffic coming into and going out of an instance.
    
    ### **Key Characteristics:**
    
    - **Stateful**: If you send a request from your instance, the response traffic for that request is allowed to flow in regardless of inbound rules.
    - **Supports Allow Rules Only**: You can only specify allow rules. Deny rules are not supported.
    - **Elasticity**: You can modify the rules for a security group at any time; the new rules are automatically applied to all instances associated with the security group.
    
    ### **Components of a Security Group Rule:**
    
    1. **Protocol**: The protocol type (TCP, UDP, ICMP).
    2. **Port Range**: The port or range of ports that can be accessed.
    3. **Source/Destination**: The source (for inbound rules) or destination (for outbound rules) of the traffic. It can be an IP address, a CIDR block, or another security group.
    
    ### **Steps to   Create and Configure a Security Group:**
    
    1. **Log into AWS Management Console**.
    2. **Navigate to EC2 Dashboard** and select "Security Groups" in the "NETWORK & SECURITY" section.
    3. **Create a New Security Group**:
        - Click “Create Security Group”.
        - Enter a name and description.
        - Select the VPC where the security group will be used.
    4. **Set Inbound and Outbound Rules**:
        - Choose "Add Rule" for each new rule.
        - Select the type, protocol, port range, and source/destination.
        - For example, to allow HTTP traffic, set Type to HTTP, Protocol to TCP, Port Range to 80, and Source to **`0.0.0.0/0`** (or a specific IP range).
    5. **Associate with an EC2 Instance**:
        - While launching an EC2 instance, select the security group.
        - Or, associate an existing instance from the "Actions" menu in the instance's details.
    
    ### **Example Scenario:**
    
    Imagine you're setting up a web server:
    
    - **Inbound Rules**:
        - Allow HTTP (port 80) and HTTPS (port 443) from any IP address (**`0.0.0.0/0`**).
        - Allow SSH (port 22) from a specific IP range for secure admin access.
    - **Outbound Rules**:
        - By default, all outbound traffic is allowed. You might restrict this to specific services if needed.
    
    ### **Best Practices:**
    
    1. **Principle of Least Privilege**: Only open ports that are absolutely necessary.
    2. **Regular Audits and Reviews**: Regularly review your security group settings to ensure they align with current requirements.
    3. **Avoid Using Broad IP Ranges**: Restrict IP ranges to known addresses where possible.
    
    ### **Common Use Cases:**
    
    - **Hosting Web Servers**: Allowing HTTP and HTTPS traffic.
    - **Database Servers**: Allowing specific ports like 3306 for MySQL, only from application server IPs.
    - **Admin Access**: Allowing SSH (Linux) or RDP (Windows) access from trusted IPs.
    
    ## Auto Scaling
    
    In auto-scaling group - 
    
    **Minimum instances** - 2
    
    **Maximum instances** - 4
    
    There are 3 scaling options - 
    
    1. Manual Scaling - You can scale minimum and maximum instances in an group, but ‘manually’.
    
    1. Scheduled Scaling - If you are aware about ‘load pattern’, then you can schedule scaling with relevant to time & date.
    2. Dynamic Scaling - Dynamic scaling is useful when you are unaware about load, so you can decide a threshold, and if load get above the threshold, then new instances will be created and vice versa. 
    
    **Benefits -** 
    
    Fault Tolerance - It will remove unhealthy instances and replace with new one.
    
    Availability - It wil increase and decrease instances based on load.
    
    Cost Management - It is cost-effective.
    
    ## VPC
    
    The private IP address ranges available in AWS, based on the IANA standards, are as follows:
    
    1. **10.0.0.0 to 10.255.255.255**:
        - This range supports a total of 16,777,216 addresses (10.0.0.0/8). It is the largest private range and is often used for large networks.
    2. **172.16.0.0 to 172.31.255.255**:
        - This range includes 1,048,576 addresses (172.16.0.0/12). It's a medium-sized range, suitable for many business applications.
    3. **192.168.0.0 to 192.168.255.255**:
        - With 65,536 addresses (192.168.0.0/16), this is the smallest range and is commonly used for small networks, like home networks.
    
    **Difference between NACL and Security Groups**
    
    | Feature | Security Groups | Network Access Control Lists (NACLs) |
    | --- | --- | --- |
    | Scope | Associated with individual instances. | Associated with one or more subnets within a VPC. |
    | Level of Operation | Operate at the instance level. | Operate at the subnet level. |
    | Statefulness | Stateful - if a request is allowed, the response is automatically allowed, regardless of inbound rules. | Stateless - inbound and outbound rules are defined and enforced separately. |
    | Rule Evaluation | Evaluates all rules before deciding whether to allow traffic. | Processes rules in order, starting with the lowest numbered rule, until it finds a match. |
    | Type of Rules | Only allows for 'allow' rules. | Allows both 'allow' and 'deny' rules. |
    | Default Setting | By default, all inbound traffic is denied, and all outbound traffic is allowed. | By default, denies all inbound and outbound traffic until rules are added to allow traffic. |
    | Flexibility | Offers fine-grained control at the instance level. | Offers a broader level of control at the subnet level. |
    | Application | Best suited for controlling traffic to and from individual instances. | Best suited for controlling traffic going in and out of a subnet. |
    | Modification Impact | Changes apply immediately to all instances associated with the security group. | Changes apply immediately to all instances in the associated subnets. |
    | Complexity | Generally simpler to set up and manage for instance-specific traffic control. | More complex due to statelessness and the need to carefully configure inbound and outbound rules. |
    
    **How many IPs are reserved for AWS?**
    
    - 10.0.0.0: Network address.
    - 10.0.0.1: Reserved by AWS for the VPC router.
    - 10.0.0.2: Reserved by AWS. The IP address of the DNS server is the base of the VPC network range plus two. For VPCs with multiple CIDR blocks, the IP address of the DNS server is located in the primary CIDR. We also reserve the base of each subnet range plus two for all CIDR blocks in the VPC. For more information, see Amazon DNS server.
    - 10.0.0.3: Reserved by AWS for future use.
    - 10.0.0.255: Network broadcast address. We do not support broadcast in a VPC, therefore we reserve this address. If you create a VPC or subnet using a command line tool or the Amazon EC2 API, the CIDR block is automatically modified to its canonical form. For example, if you specify 100.68.0.18/18 for the CIDR block, we create a CIDR block of 100.68.0.0/18.
    
    | Aspect | DOS Attack | DDOS Attack |
    | --- | --- | --- |
    | Definition | A Denial of Service (DOS) attack is an attempt to make a machine or network resource unavailable to its intended users. | A Distributed Denial of Service (DDOS) attack is similar to DOS but it is launched from multiple machines. |
    | Source of Attack | Originates from a single internet connection or a small number of them. | Involves multiple compromised systems, often spread across the globe, to launch the attack. |
    | Scale of Attack | Limited in scale due to the capabilities of a single source. | Potentially massive in scale due to the use of numerous sources. |
    | Intensity and Power | Relatively less powerful compared to DDOS. | Significantly more powerful due to the cumulative attack power of multiple sources. |
    | Ease of Detection | Easier to identify and mitigate as it comes from a single or limited sources. | More challenging to detect and mitigate due to the distributed nature of the attack. |
    | Common Techniques | Overloading a server with requests, exploiting software vulnerabilities, etc. | Botnets, exploiting control of multiple devices, synchronized flooding attacks, etc. |
    | Mitigation Complexity | Relatively simpler to mitigate as blocking a single source can often stop the attack. | More complex to mitigate; requires sophisticated filtering, rate limiting, and traffic analysis. |
    | Example Tools | LOIC (Low Orbit Ion Cannon), Slowloris. | HOIC (High Orbit Ion Cannon), Botnets like Mirai. |
    | Impact Duration | Typically short-lived due to the limitations of a single source. | Can last longer and cause more damage due to the collective power of multiple sources. |
    | Target | Often targets smaller websites or services. | Capable of targeting and bringing down large networks or services. |
    
    ## Steps to Create NAT Gateway
    
    1. First create a VPC (172.0.0.0/16)
    2. Then create 2 Subnets: one public (172.0.3.0/24) and second private (172.0.2.0/24)
    3. Then create route table
    4. Then create Internet gateway and attach to VPC
    5. Attach Internet gateway with default Route table. (No need to create one)
    6. Create one more route table
    7. Create 2 instance, one for public, another for private.
    8. Take SSH of public instance and check if its connecting to internet
    9. Then create NAT gateway, attach it to public subnet
    10. Explicit Associate 2nd route table with private subnet
    
    ## Steps to Create NAT Gateway (Simple Steps)
    
    1. **Setup VPC**
    - CIDR range - 12.0.0.0/16
    1. Create Subnet
    - First create public subnet; i.e test-subnet-public
    - CIDR - 12.0.1.0/24
    - Add one more subnet, i.e test-subnet-private
    - CIDR - 12.0.2.0/24
    - Click on create subnet
    1. Create Internet Gateway to attach with Public Subnet
    - Name Internet Gateway; i.e test-igw-public
    - Attach it to VPC
    1. Create Route tables
    - Create one public route table; i.e test-rt-public
    - To attach igw to public route table, click on ‘Edit Routes’
    - Click on Add Routes & select 0.0.0.0/0 (to access internet from anywhere) and attach igw
    - Go to the subnet association, click on edit subnet association and attach public subnet
    - Now, create one private route table i.e test-rt-private and select vpc to attach with.
    - Go to “Edit Subnet associations” and select the private subnet i.e test-subnet-private
    1. Setup NAT Gateway
    - Create NAT gateway named as - test-natgw
    - Under subnets menu, click on public subnet - test-subnet-public
    - Select ‘Public’ connectivity for VPC. [Private connectivity is used to communicate with other VPCs present in your AWS account, it wont have access to internet]
    - Then allocate Elastic IP to NAT gateway, finally create NAT Gateway
    1. Update Route Table (Private subnet)
    - Go to the Route Tables section, click on private route table that we create - test-rt-private
    - Click on ‘Edit Routes’ and select ‘0.0.0.0/0’ and ‘NAT Gateway’
    1. **Setup EC2**
    - Launch an instance named as - test-ec2-public
    - Create new keypair named as ‘nat-gateway-key’ & download it
    - Edit ‘Network Settings’ and select our VPC that we created.
    - Then select the public subnet and enable ‘auto assign public IP’
    - Under security groups, add HTTP request from anywhere
    - Go back to ‘instances’ and launch another instance - test-ec2-private
    - Select the same key that we created & downloaded earlier i.e nat-gateway-key
    - Edit network settings, select our VPC,  and select private subnet.
    - Make sure ‘auto assign public IP’ is disabled
    - Under security groups, enable HTTP from anywhere
    1. Test NAT Gateway
    - First we need to ssh public instance then from there we can ssh private instance
    - Go to EC2 dashboard, select public EC2, click on connect
    - Follow the on-screen instructions and test if its able to access internet.
    - Once you pinged successfully, now we need to access private subnet. For that, locate the key that we downloaded while creating EC2 instance, use the ‘cat’ command to copy content of the key.
    
    ## CloudWatch
    
    1. First Create EC2 instance, (4 instances) also provide tags for each instance
    2. Now jump to CloudWatch
    3. Create Dashboard
    4. Select Data Source
    5. Now we need to add EC2 metrics,
    
    NFSv4 Port number - 2049
    
    ---
    
    ## #Questions
    
    ### ****What is Cloud Computing?****
    
    Cloud Computing is like a virtual infrastructure that provides resources and services like networking, storage, servers etc with pay-as-you-go feature. It is more faster, flexible and cheaper than traditional computing where pyhical infrastructure is used
    
    ### ****Deployment Model in Cloud****
    
    1. **Public Cloud**: This is like renting a space in a large, shared building. You get services on servers that are open for public use. It's cost-effective and you don't worry about maintenance, but you share the space with others.
    2. **Private Cloud**: It is like owning a private property. It's exclusive to one business or organization. More secure and controllable, but it comes with the responsibility of maintenance and higher costs.
    3. **Hybrid Cloud**: This is a mix-and-match of public and private cloud. You use both public and private clouds, depending on what you need. It offers a balance of security, cost efficiency, and scalability.
    
    ### ****Service Model in Cloud****
    
    1. **Infrastructure as a Service (IaaS)**: This is like renting the basic building blocks - servers, storage, and networking. You get the raw infrastructure, but you have to manage everything else.
    2. **Platform as a Service(PaaS)**: Think of this as renting a workshop with tools included. You get the infrastructure plus the environment to develop, test, and manage your apps.
    3. **Software as a Service (SaaS)**: This is like subscribing to a service. Everything is managed for you, and you just use the software over the internet, like email services or office tools.
    
    ### **Why Do We Use Region in Cloud Computing?**
    
    Using a region in cloud computing is like choosing a location for you. It's like placing your applications and data close to your users to reduce latency, which provide higher fault tolerance.
    
    ### **What is a Service & What are Resources in Cloud Computing?**
    
    In cloud computing, a service is like a tool you use or the application that you access over the internet, like S3 or EC2 to run, test and deploy apps. Resources, on the other hand, are the individual components needed to run these services, such as virtual machines, network equipment, and storage devices.
    
    ### **Deployment Model in IAM**
    
    IAM doesn't have a deployment model like cloud computing does. It's a part of AWS services, so it's already set up in the cloud.
    
    ### **Identities in IAM**
    
    In IAM, identities are basically who or what you're giving access to. There are three main types: users, groups, and roles.
    
    ### **What is an IAM User?**
    
    An IAM user is like an individual user for a person or service that needs to use AWS. Think of it as a specific account with a set of permissions that define what actions they can or cannot do in AWS.
    
    ### **What is the IAM Group?**
    
    An IAM group is like putting a bunch of users into one team. Instead of giving permissions to each user one by one, you can put them in a group and manage their permissions all together.
    
    ### **What is the IAM Policy?**
    
    An IAM policy is a set of rules that define what actions are allowed or denied. It's like the rulebook for users, groups, and roles in IAM
    
    ### **What is the IAM Role?**
    
    An IAM role is a bit different from a user. It's like a temporary identity you can set for a specific task. You use roles to give necessary permissions to users from other AWS accounts or services without having to share long-term access keys.
    
    ### **Where Do We Attach Identity Based Policy?**
    
    Identity-based policies are attached directly to IAM identities, which means you can attach them to users, groups, or roles within IAM.
    
    ### **Where Do We Attach Resource Based Policy?**
    
    Resource-based policies are attached to AWS resources themselves. This means you put the policy on things like S3 buckets or EC2
    
    ### **Can We Be Able to Create Policy via JSON Code?**
    
    Yes, you can create policies using JSON code.
    
    ### **If One User Has Created It by Default, Which Permission Has Been Assigned to That User?**
    
    When a user is created in IAM, by default, they are not assigned any permissions. This means they can't do anything in AWS unless you gave them permission by yourself
    
    ### ****What is Dominator Policy?****
    
    Dominator policy is like a specific policy that you give to a particular user and the user gets administrative access to services.
    
    ### **What is ARN? What Are the Fields in ARN?**
    
    ARN stands for Amazon Resource Name. It's a unique identifier for resources in AWS. An ARN includes several fields: the service name, the region, the account ID, the resource type, and the resource name.
    
    ### How Many Types of ARN Partitions?
    There are three types of ARN partitions in AWS: aws for global resources, aws-cn for China regions, and aws-us-gov for US government regions.
    
    ### **What are Tags?**
    
    Tags in AWS are like labels or stickers you put on resources. It helps us to identify users or resources easily. It is like giving them a second name.
    
    ### Difference between Block storage & Object Storage ?
    
    - **Block Storage**: Block storage divides data into evenly sized blocks of data, each with its own address but without any additional metadata. It's like storing data in fixed-sized boxes where each box is given a unique label. Block storage is excellent for data that requires frequent editing, as it allows for accessing and modifying small parts of a file without affecting the entire file. Commonly used in SAN (Storage Area Network) environments, it's ideal for databases or transactional data.
    - **Object Storage**: In contrast, object storage handles data as distinct units called objects. Each object includes the data, a variable amount of metadata, and a globally unique identifier. Object storage is great for storing massive amounts of unstructured data, like photos, videos, or backup files. It's the backbone of cloud storage services because of its scalability, metadata characteristics, and the ability to store vast amounts of unstructured data.
    
    ### Difference between static website & dynamic website ?
    
    A static website consists of fixed content, and each page displays the same information to every visitor. These websites are written in HTML, CSS, and JavaScript, and the content does not change unless manually updated by the webmaster. They are straightforward to develop and host, making them suitable for small websites and landing pages.
    
    A dynamic website, on the other hand, can display different content and provide user interaction by using advanced programming and databases. They are built using server-side languages like PHP
    
    ### What are the naming rules ?
    
    1. Capital letters not allowed
    2. No IP address
    3. unique username
    4. No special characters

### What is the major resource of S3 Bucket ?

### Why do we need to host static websites instead of dynamic websites ?

Hosting static websites is often preferred over dynamic ones for simplicity, speed, and cost-effectiveness. Static websites are easier and cheaper to host since they require less server processing and fewer resources. They're faster to load and less prone to security issues, as they don't involve server-side processing or databases.

### What is versioning & Why do we need versioning ?

Versioning in AWS S3 is a means of keeping multiple versions of an object in the same bucket. It's like having a history of your files, where every update creates a new version rather than overwriting the existing file.

## What are the objects and types of objects that we are uploading into the S3 Bucket ?

The objects you can upload into an S3 Bucket are virtually any type of file: text documents, images, videos, audio files, backups, and so on.

### Why is MFA Delete important in S3 Bucket object level ?

MFA adds an extra layer of security over bucket, so that nobody can delete or modify the bucket unless they have MFA code.

### What is S3 Multipart Upload?

Imagine you have a really large file, like a huge video or a big set of data, and you need to upload it to Amazon S3, which is like an online storage space. Uploading it all at once might take a long time and can fail if your internet isn’t stable. S3 Multipart Upload is like breaking that big file into smaller, manageable pieces, uploading each piece separately, and then putting them all back together in S3. This way, if the upload of one piece fails, you only have to re-upload that small part, not the whole huge file.

### What are the Storage Classes in Amazon S3?

Standard: For frequently accessed data.
Intelligent-Tiering: Automatically moves data between two tiers based on how often you access it.
Standard-IA (Infrequent Access): Cheaper for data you don’t access often, but need to retrieve quickly when you do.
One Zone-IA: Like Standard-IA but stored in a single location, making it less costly.
Glacier: For long-term storage, where you can wait a bit to get the data back.
Glacier Deep Archive: The most affordable for data you rarely access.

### What is ACL?

ACL stands for Access Control List. It’s a way to decide who can see and use your files in S3. Think of it like a list of rules that say who can read or write (modify) your files.

### Why Do We Need ACL?

We need ACL to keep our files secure and to make sure only the right people can access them.

### What is a Lifecycle Policy? Why Do We Need to Use the Lifecycle Rule?

A Lifecycle Policy in S3 is like setting up automatic rules for your files over time. For instance, you can have a rule that automatically moves your old files to a cheaper storage class if you haven’t used them in a while, or even delete files that you no longer need. This helps manage your storage space and cost effectively.

### How can we make our bucket public ?

- Select the bucket you want to make public.
- Click on the 'Permissions' tab.
- Scroll down to the 'Block Public Access' settings and click 'Edit'.
- Uncheck all the boxes under 'Block Public Access settings' to allow public access.
- Click 'Save Changes' and confirm by typing "confirm".

### How can we give public access to our bucket ?

Go to the 'Permissions' tab for your bucket.

Scroll to the 'Bucket Policy' section.

Click 'Edit' and enter a bucket policy that grants public read access. You can use the policy generator or manually write a policy.

### Aws pricing factor of the S3 Service.

### How can we make our object public ?

Select the bucket and then the object you want to make public.
Click on the 'Permissions' tab for the object.
Under the 'Object permissions', click 'Edit'.
Check the box next to 'Everyone (public access)'.
Under 'Access to this object', select 'Read'.
Click 'Save changes'.

### **How Can We Configure Static Website Logs in S3?**

1. **Go to your S3 bucket** where your website is.
2. **Click on ‘Properties’** at the top.
3. **Find the ‘Server access logging’ section**, and click on it.
4. **Set up logging** by selecting another S3 bucket to store the logs.
5. **Give a name for the log files** and save it.
6. Now, your website's visits and activities will be logged in the other bucket.

### **What is CORS?**

CORS  is Cross-Origin Resource Sharing. It's like a rulebook for your website that tells browsers if it's okay to get resources from different places. For example, if your website on one server needs to access images from another server, CORS decides if that’s allowed.

### **What is S3 Inventory?**

S3 Inventory is like a regular report of your S3 bucket. It gives you a list of all your files (objects) in the bucket and details about them, like size, when they were last changed, and if they are encrypted.

### **What Does it Mean by Requester Pays?**

'Requester Pays' in S3 is like asking someone else to pick up the tab for the data transfer costs. Usually, the owner of the S3 bucket pays for the data transfer, but with 'Requester Pays,' anyone who gets data from your bucket has to pay the cost of moving that data.

### **What is a CloudTrail?**

CloudTrail is like a detective in AWS. It keeps track of what's happening in your AWS account. Every time someone does something like creating a new EC2 instance or changing a setting, CloudTrail writes it down. It’s good for security and figuring out what happened if something goes wrong.

### **Why Do We Use Trails, and What is the Exact Purpose of Enabling the Trail in Cloud Production Accounts?**

We use trails to keep an eye on our AWS accounts. When you turn on trails in CloudTrail, it's like having a security camera. It records all activities and changes. This is super important in production accounts to make sure everything is secure and to help find and fix any problems that come up.

### **Explain How We Can Create a Trail in AWS CloudTrail?**

1. **Open AWS CloudTrail** in the AWS Management Console.
2. **Click on ‘Trails’** on the left, then ‘Create trail’.
3. **Name your trail**.
4. **Choose a bucket** to store the logs.
5. **Set up the trail** to log what you need (like all management events).
6. **Save your trail**. Now, it'll start recording activities in your AWS account.

### How Can We Enable Logging for an S3 Bucket Using CloudTrails?

Open CloudTrail, and go to your trail.
Click on the trail and look for ‘Data events’.
Click ‘Configure’ in the Data events section.
Choose S3 as your data event source.
Select your S3 bucket you want to log.
Save your changes. CloudTrail will now log activities for that S3 bucket.

### **How Do You Get the List of All Created Trails in Your Production Account?**

1. **Open AWS CloudTrail**: Go to the AWS Management Console and open CloudTrail.
2. **Click on ‘Trails’**: On the left side, there's a menu. Click on ‘Trails’.
3. **View the List**: You’ll see a list of all the trails created in your account.

### **Can We Create a Trail for a Multi-Region, and How Can We Configure It?**

1. **Create a New Trail**: In CloudTrail, start making a new trail.
2. **Select ‘Apply to All Regions’**: There's an option to make the trail apply to all regions. Choose that.
3. **Complete the Setup**: Fill out the rest like normal (naming the trail, choosing a bucket) and save it.

### **How Can We Disable the Logging for Certain Events, Services in CloudTrail?**

1. **Go to the Trail Configuration**: In CloudTrail, click on your trail.
2. **Edit the Trail**: There's an option to edit or configure the trail.
3. **Change Data Event Settings**: In the ‘Data events’ section, you can choose which data sources to log. Uncheck the ones you don’t want.
4. **Save Your Changes**: After deselecting, save the new settings.

### **Real-Time Use Case of CloudTrail**

An example is keeping track of changes in a big company’s AWS resources. Say someone accidentally deletes an important S3 bucket. With CloudTrail, you can find out who did it and when, which helps in fixing the problem and preventing future issues.

### **What is CloudTrail Event History?**

Event history in CloudTrail is like a recent activity log. It shows the last 90 days of actions taken in your AWS account. You can see things like who accessed what resource and what changes were made. It’s handy for a quick check of your account's activity.

### **What is Log File Integrity Validation in CloudTrail?**

Log file integrity validation in CloudTrail is like a security check. It helps you make sure that no one has messed with your logs. When it's turned on, CloudTrail adds a digital signature to each log file. You can then use this signature to verify that the log files haven’t been changed or tampered with since CloudTrail wrote them.

### **What is VPC?**

A VPC, or Virtual Private Cloud, is like having a piece of the cloud that's just for you. It's a section of AWS where you can place your own services and resources, like websites or databases. It's private, which means you control who can access what, almost like having a private network in the cloud.

### **What are Subnets when working with VPC?**

Subnets in a VPC are like dividing a big plot of land (your VPC) into smaller plots (subnets). Each subnet can be used for different purposes. Some can be for public stuff, like a website, while others can be private, just for things like databases. This way, you can organize and secure your resources better.

### **What is NAT Device?**

A NAT device, or Network Address Translation device, in a VPC is like a translator for internet addresses. It lets computers inside your VPC (which have their own private addresses) talk to the internet, while keeping those computers hidden from the outside world. It's like having a secret passage from your private network to the public internet.

### **Difference Between Stateful & Stateless Filtering**

- **Stateful Filtering**: This is like a smart security guard who remembers who you allowed in and out of your house. In tech terms, if a request is allowed in one direction, the response is automatically allowed back in the other direction.
- **Stateless Filtering**: This is like a basic rule list. It checks incoming and outgoing traffic separately against a set of rules, without remembering any past interactions.

### **Advantages of Using Default VPC**

Using a default VPC in AWS is like moving into a pre-furnished apartment. It's easy and ready to use. You don't need to set up basic stuff like subnets, an internet gateway, or default security settings. It's great for beginners or if you want to start quickly without customizing your network setup.

### **What is the Internet Gateway in VPC?**

An Internet Gateway in a VPC is like a door between your private cloud network and the big wide internet. It lets your VPC connect to the internet, allowing computers and services in your VPC to send and receive data from the internet.

### **What is Network ACL in VPC?**

Network ACL, or Access Control List, in a VPC, acts like a bouncer. It's a set of rules that control traffic in and out of your subnets. You can set up rules to decide what internet traffic can enter and leave your subnets, helping to keep your VPC secure.

### **What is the Security Group in VPC?**

A Security Group in a VPC is like a personal bodyguard for your services, like EC2 instances. It sets rules that control incoming and outgoing traffic to these services. Think of it as setting up who can visit you (your instances) and who you can visit.

### **What is an Elastic IP Address in VPC, and Why Do We Need to Use It?**

An Elastic IP Address in a VPC is a static, unchanging internet address. You'd use it when you need a fixed address for your services, like if you're hosting a website and you don't want the address to change.

**Real-time Example**: Imagine you have a shop (your website) in a mall (the internet). If your shop keeps moving to different locations (changing IP addresses), your customers will get confused and might not find you. An Elastic IP makes sure your shop stays in one spot, making it easy for customers to come back.

### **Steps to Assign an Elastic IP:**

1. **Get the Elastic IP**: Go to the AWS console, and in the EC2 dashboard, allocate a new Elastic IP.
2. **Attach to an Instance**: Choose an EC2 instance you want to attach the Elastic IP to.
3. **Associate It**: Associate the Elastic IP with the selected instance. Now, this instance has a fixed, public IP address.

### **Can We Attach One Production Elastic IP to the New Prod Server?**

Yes, you can attach a production Elastic IP to a new prod server. Here's how to do it in simple steps:

1. **Get an Elastic IP**: Go to AWS and find the Elastic IP section. Get a new Elastic IP if you don't have one already.
2. **Detach from Old Server**: If the Elastic IP is currently attached to another server, you need to detach it from there first.
3. **Attach to New Server**: Now, go to your new prod server in AWS and attach the Elastic IP to it.

### **How Does ELB Affect a VPC?**

ELB (Elastic Load Balancer) helps spread out incoming internet traffic across multiple servers in your VPC (Virtual Private Cloud). It's like having a traffic cop directing cars (internet traffic) to different lanes (servers) so no single lane gets too crowded.

### **What are the Limitations of VPC’s, Gateway, and Subnets?**

1. **VPCs**: You can only have a certain number of VPCs per region in AWS.
2. **Gateways**: Each VPC can have only one Internet Gateway.
3. **Subnets**: Each subnet is in one Availability Zone, so its resources are limited to that zone. Plus, there are limits on how many subnets you can have in a VPC.

### **What is a Public IP Address and Why Do We Use It?**

A public IP address is like your home’s street address on the internet. We use it so the rest of the internet can find and send information to your computer (or server). It's needed for any device that you want to be accessible from the internet.

### **Explain Bastion Host Concept**

A Bastion Host is like a secure, special door into your private network in AWS. You use it to safely get into your private network without exposing everything else to the public internet. It's like having a guarded entrance to a private community.

### **When Do We Need to Create a New Customized VPC?**

You create a new custom VPC when you need a specific, separate space in AWS for your project. It's like building a new playground with its own fences and rules, different from the public parks (default VPCs).

### **What is Peering? Why Do We Need to Peer at Two VPC’s?**

Peering is like creating a private connection (VPCs). We do this so they can share resources or communicate without using the public roads (internet). It's used for security and to keep traffic private.

### **What is VPN? Where Do We Use VPN Tunnel?**

VPN i Virtual Private Network. It's like a secret, secure tunnel on the internet.

Here’s how you use a VPN tunnel:

1. **Set Up VPN**: You create a VPN connection in AWS.
2. **Connect Your Network**: Link your company’s network to the VPN.
3. **Safe Passage**: Now, your data can travel safely through this tunnel from your place to AWS without being exposed on the open internet.

## EC2

### **What is EC2, Why Do We Need EC2 Service in Cloud Computing?**

EC2 stands for Elastic Compute Cloud. It's a service in the cloud that lets you use computers for pretty much anything you'd use a real computer for, like running apps or storing data. We need EC2 because it's like having a bunch of extra computers whenever we want, without having to buy them. You can make them more powerful or turn them off when you don't need them, which can save you money and hassle.

### **Features of Amazon EC2**

Amazon EC2 has some cool features:

- You can choose different sizes of EC2, depending on how strong you want them to be.
- You can control them completely, like your own computer.
- They're safe because Amazon keeps them in big, secure buildings.
- You can have as many as you need and stop using them when you don't.

### **What is Hypervisor? and Its Types?**

A hypervisor is like a boss that manages how virtual machines use the physical computer's resources. It makes sure each virtual machine runs smoothly without interfering with others.

There are two main types:

- **Type 1**: These are like the foundation of a house. They run directly on the hardware. Think of them as the ground floor.
- **Type 2**: These are like setting up a tent inside your house. They run on top of an operating system, like having a second layer.

### **Where We Use Hypervisor**

We use hypervisors in places like:

- Data centers, where lots of virtual machines are needed.
- Cloud services, like AWS or Azure, to create and manage virtual machines.
- In companies, to run different services on the same physical machine without them messing with each other.

### **Steps to Create an EC2 Instance**

Here's how you make a new EC2 instance, step by step:

1. Sign in to AWS and go to the EC2 Dashboard.
2. Click 'Launch Instance'.
3. Pick an Amazon Machine Image (AMI) - it's like the type of computer you want.
4. Choose an Instance Type - like picking how strong the computer should be.
5. Configure the instance details - like how many you want.
6. Add storage if you need more space.
7. Set up security groups - these are like rules for who can visit your computer.
8. Review everything, and if it looks good, hit 'Launch'.
9. Pick a key pair for access, and you're all set.

### **EC2 Instance State**

EC2 instance state is like the mood of your EC2. It can be:

- Running: It's on and working.
- Stopped: It's off, but not gone. You can start it again.
- Terminated: It's gone for good, like when you recycle your old computer.

### **How Many Types of EC2 Instance-State Codes?**

There are several instance-state codes, but here are the main ones:

- 0: pending
- 16: running
- 32: shutting-down
- 48: terminated
- 64: stopping
- 80: stopped

### **What is the Meaning of Server Hibernating Mode?**

Server hibernating mode is like when your computer goes to sleep. It saves your work so you can pick up where you left off. The EC2 saves stuff in the RAM to the disk, and it stops charging you for the server. When you wake it up, it starts right back up without having to set everything up again.

### **What is KMS?**

KMS stands for Key Management Service. It's like having a bunch of keys to lock your secret stuff up in the cloud. You can lock and unlock your data, and only people with the right key can see it. It helps keep your things safe in the cloud.