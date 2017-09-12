REANCloud Assessment - Option #1
-----------------------------------

**Objective:**
Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress. Setup a sample site. Automate the solution using CloudFormation template.
 
**Deliverable:**
A CloudFormation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

**Experience:**
After struggling a bit with no knowledge of CloudFormation templates, a Google Search led me to https://www.youtube.com/watch?v=6R44BADNJA8 which provided a great deal of information, examples, hints, and things I hadn't thought to include in my plan.  

One thing I should note, is that I found no reference as to how to create EC2 KeyPairs, so I created this manually through the console.  I will also reach out to the team to see if they have any expertise in that regard and can either confirm it is not possible or provide information how to accomplish this in CloudFormation.

After establishing a standalone Ansible installation as well as a standalone webserver for the WordPress installation, the decision was made to have the Ansible installation in a private subnet and the webserver installation be in a public subnet.  This required the introduction of AWS NAT Services and an Elastic IP address in order for the Ansible server to be able to access the internet and download updates, as well as ansible scripts from this git repository.

Using an existing ansible playbook for the installation of wordpress allowed me to customize it for the Amazon Linux AMI selected for installation.

**Assumptions:**
* The JSON used is expected to be run in absence of existing systems (fresh)
* The installation is specifically destined for the us-east-1a availaility zone.  Examples of extending this script to include this as a dynamic parameter abound.
* The Database user is "root", password can be specified at stack creation time.
* The first hit to the public url will take you to the set up where you specify personal information such as email address, site name, etc.
* Full installation takes 10-15 minutes.

**External Resources Used:**

https://www.youtube.com/watch?v=6R44BADNJA8

http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-sample-templates.html 

http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html

http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html

https://github.com/gcis/ansible_wordpress

