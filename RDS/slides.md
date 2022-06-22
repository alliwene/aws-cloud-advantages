---
theme: seriph
background: ./images/rds_logo.jpeg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Amazon RDS 
drawings:
  persist: false
layout: cover
title: Amazon RDS 
---

<!--

-->

#  Amazon Relational Database Service 

Week 6.5

---

# What you will Learn 


<v-clicks>

*  Give an overview of Amazon RDS 
*  Describe some of the options that Amazon RDS offers 
*  Explore Amazon RDS backup options 
*  Explain the six database types on Amazon RDS 
*  Establish high availability, which Amazon RDS offers  
*  Examine a few uses cases for Amazon RDS

</v-clicks>


---

# Introduction to Amazon RDS

<v-clicks> 

* Amazon Relational Database Service (Amazon RDS) is a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud.
* Running an unmanaged, standalone relational database can be time-consuming and have limited scope. 
* To address these challenges, AWS provides a service that sets up, operates, and scales the relational database without any ongoing administration. 
* Amazon RDS provides cost-efficient and resizable capacity while automating time-consuming administrative tasks.
* Amazon RDS frees you to focus on your application so you can give the applications the performance, high availability, security, and compatibility that they need. 
* With Amazon RDS, your primary focus is your data and optimizing your application.

</v-clicks>


---

# Introduction to Amazon RDS

<v-clicks> 

* It supports seven popular engines - [Amazon Aurora with MySQL compatibility](https://aws.amazon.com/rds/aurora/?pg=ln&sec=hiw), [Amazon Aurora with PostgreSQL compatibility](https://aws.amazon.com/rds/aurora/?pg=ln&sec=hiw), [MySQL](https://aws.amazon.com/rds/mysql/?pg=ln&sec=hiw), [MariaDB](https://aws.amazon.com/rds/mariadb/?pg=ln&sec=hiw), [PostgreSQL](https://aws.amazon.com/rds/postgresql/?pg=ln&sec=hiw), [Oracle](https://aws.amazon.com/rds/oracle/?pg=ln&sec=hiw), and [SQL Server](https://aws.amazon.com/rds/sqlserver/?pg=ln&sec=hiw) — and deploy on-premises with [Amazon RDS on AWS Outposts](https://aws.amazon.com/rds/outposts/?pg=ln&sec=hiw).

</v-clicks>


---

# Amazon RDS DB Instances

<figure>
  <center>
    <img src="images/db_instance.png" style="width:500px;height:220px;">
  </center>
</figure>

<v-clicks> 

* The basic building block of Amazon RDS is the DB instance. 
* A DB instance is an isolated database environment. 
* It can contain multiple user-created databases and can be accessed by using the same tools and applications that you use with a standalone database instance. 
  
</v-clicks>


---

# Amazon RDS DB Instances

<figure>
  <center>
    <img src="images/db_instance.png" style="width:500px;height:220px;">
  </center>
</figure>

<v-clicks> 

* The resources in a database instance are determined from its database instance class, and the type of storage is determined by the type of disks.
* Database instances and storage differ in performance characteristics and price, which enable you to customize your performance and cost to the needs of your database. 
* When you choose to create a DB instance, you must first specify which database engine to run. 
  
</v-clicks>


---

# Amazon RDS Backup

<v-clicks> 

* Because Amazon RDS is a fully managed service, one task that it automatically performs is the periodic backup of a DB instance. 
* The entire instance is backed up to a storage volume snapshot during a specified backup window. 
* It is retained according to a specified backup retention period. 
* The first snapshot of a DB instance contains the full data. 
* Subsequent snapshots are incremental and contain only the data that changed since the most recent snapshot.
* Optionally, you can back up a database instance manually by creating a snapshot.
* For more information about working with backups, see [Backing up and restoring an Amazon RDS DB instance](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_CommonTasks.BackupRestore.html).

</v-clicks>


---

# High Availability with Amazon RDS

<figure>
    <img src="images/high_availability.png" style="width:100%;height:270px;">
</figure>

<v-clicks>

* You can configure a database instance with high availability by using a Multi-AZ deployment. 
* This configuration automatically generates a standby copy of the database instance in another Availability Zone in the same virtual private cloud (VPC). 

</v-clicks>


---

# High Availability with Amazon RDS

<figure>
    <img src="images/high_availability.png" style="width:100%;height:270px;">
</figure>

<v-clicks>

* After you make the initial full copy, transactions are synchronously replicated to the standby copy. 
* Running a database in multiple Availability Zones can enhance availability during planned system maintenance. 
* It can also help protect your database against database failure and disruptions to Availability Zones.

</v-clicks>


---

# High Availability with Amazon RDS: Failover

<figure>
    <img src="images/failover.png" style="width:100%;height:270px;">
</figure>

<v-clicks>

* If the primary database instance fails, Amazon RDS automatically brings the standby database instance online as the new primary instance. 
* Requests from both applications are then directed to the new primary instance. 

</v-clicks>


---

# High Availability with Amazon RDS: Failover

<figure>
    <img src="images/failover.png" style="width:100%;height:270px;">
</figure>

<v-clicks>

* The requesting applications use the Amazon RDS Domain Name System (DNS) endpoint to reference the database by name. 
* As a result, the failover happens without needing to change the application code. 
* No data loss occurs because of the synchronous replication.

</v-clicks>

---

# Amazon RDS Read Replicas

<v-clicks>

* Understand how internal operations gain compliance on AWS.
* Access to recommended training, self-paced labs, and auditing resources from the compliance website.
* For more information, refer to the [Cloud Audit Academy](https://aws.amazon.com/professional-services/) learning path.
  
</v-clicks>


---

# AWS Compliance Solutions Guide 

<v-clicks> 

* Access frequently used resources and processes, using the AWS Compliance Solutions Guide.
*  Learn about the available compliance solutions, such as 
   *  Understanding the shared responsibility model 
   *  Requesting a compliance report 
   *  Completing a security questionnaire


</v-clicks>


---

# More AWS Compliance Resources

<v-clicks> 

* More AWS compliance resources include: 
* **Services in Scope** – Details about which services are currently in scope and which are in progress.
* **AWS Security Blog** – The blog is a good way to learn about the newest updates to AWS security programs.
*  **Case Studies** – Provide insightful information on some of the AWS current customer experiences with security.
*  To learn more, refer to [Compliance Resource](https://aws.amazon.com/compliance/resources/)

</v-clicks>

---

# Key Takeaways

<v-clicks>

*  Different types of available security resources include:
   * AWS account teams 
   * AWS Enterprise Support 
   * AWS Professional Services and the AWS Partner Network (APN) 
   * AWS advisories and bulletins  
   * AWS auditor learning path 
   * AWS compliance solutions guide

</v-clicks>
