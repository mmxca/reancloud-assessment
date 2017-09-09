REANCloud Assessment - Option #1
-----------------------------------

**Objective:**
Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress. Setup a sample site. Automate the solution using CloudFormation template.
 
**Deliverable:**
A CloudFormation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

**Plan:**
 1. Establish a GitHub repository
 2. Create CloudFormation template to establish a AmazonLinux VPC with necessary subnets
 3. Extend CloudFormation template to establish an Ansible Instance with an existing AMI
 4. Using the Ansible instance, configure the host installing necessary prerequisites
 5. Using Ansible, install and configure the Wordpress installation
 6. Populate the Wordpress site with some sample posts
 7. Add additional parameters (such as selection of 
 7. Document any necessary assumptions  & retrospectives
 8. Perform repetitive tests to ensure the assignment is completed thoroughly to match the requirements of the assessment

**Iteration 1:**
You Are Here!

**Iteration 2:**
After struggling a bit with no knowledge of CloudFormation templates, a Google Search led me to https://www.youtube.com/watch?v=6R44BADNJA8 which provided a great deal of information, examples, hints, and things I hadn't thought to include in my plan.  This iteration and the next should flow smoothly and because CloudFormation is easier - at least in appearance - than I thought it would, I am revising the plan to include some additional tasks will make the solution robust and should not impact timeline.

Working through this iteration I came across a "stock" AMI that is available for EC2 which I will use rather than a docker container.

One thing I should note, is that I found no reference as to how to create EC2 KeyPairs, so I created this manually through the console.  I will also reach out to the team to see if they have any expertise in that regard and can either confirm it is not possible or provide information how to accomplish this in CloudFormation.
