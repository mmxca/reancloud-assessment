REANCloud Assessment - Option #1
-----------------------------------

**Objective:**
Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress. Setup a sample site. Automate the solution using CloudFormation template.
 
**Deliverable:**
A CloudFormation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

**Plan:**
 1. Establish a GitHub repository
 2. Create CloudFormation template to establish a AmazonLinux VPC with necessary subnets
 3. Extend CloudFormation template to establish a Docker Capable AmazonLinux VPC in the same subnet, and auto-launch the Ansible Instance
 4. Using the Ansible instance, configure the host installing necessary prerequisites
 5. Using Ansible, install and configure the Wordpress installation
 6. Populate the Wordpress site with some sample posts
 7. Document any necessary assumptions  & retrospectives
 8. Perform repetitive tests to ensure the assignment is completed thoroughly to match the requirements of the assessment

