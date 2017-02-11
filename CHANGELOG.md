This file is used to list changes made in each version of the depy framework.

## 0.0.20

### Highlights
 * Bumping versions - clm and jenkins
 * Infrastructure abstraction - Using platform names instead of ami versions. Platform is depended by application version.
 * Jenkins feature toggle - scm_sync and slack
 * Application Versions - dedicated config file
 * chef.io component - nodejs application
 * chef.io upgrades improved by utilizing AWS Elastic Beanstalk capablities.
 * logging - MVP version. Each function, begin+end, prints its name

### Full list
 * clm - bumping to version 6.0.2 ifix008 and 6.0.3 ifix002
 * clm - standardize the jbe component deployment for all versions
 * depy-backend - lmb.spotinst ansible role renamed -> depy.spotinst
 * depy-backend - infrastructure abstraction - application configuration requires platform name instead of AMI. MVP version - implemented for clm
 * clm/ansible - fixed typos in __screen_capture.yml file.  admin.password instead of admin.passord
 * clm refactoring - upstart/systemd is depended on the platform version instead of clm version
 * depy-backend - settings.py refactoring - settings_load_features was renamed to settings_load which loads several types of configuration files
 * Jenkins/Chef - fixed typos in scm_sync recipe
 * Jenkins/Chef - feature recipe now installs its dedicated plugins
 * Jenkins/Chef - feature recipe for slack. MVP version, deploys plugins.
 * depy-backend - Printing info messages before deploy begins
 * depy-backend - Splitting application versions from main config file to <app>/versions.json file. MVP version - implemented for Jenkins.
 * Jenkins - bumping to version 2.45 including plugins upgrades
 * depy - moved chef.io application to a dedicated private repo
 * depy - documentation updates
 * depy-utils - addeded chef.io component to the release process
 * depy-utils - upgrading chef.io prod environment with upgrade_environment function instead of terminating/creating environment.
 * depy-backend - logging option. MVP Version.

## 0.0.19

### Highlights
 * Feature Toggle - Features will be controlled by configuration file conf/\<company\>/\<application\>/features.json. The active key will be set to true if feature deployment is desired.
 * RTCSample.jar is no longer included statically in the chef cookbook, but, built and linked dynamically on the git node
 * DEPY name in depy.io webapp switched from previous name: DEPI
 * Github organization depy-io. Moved depy repo from user: lioramilbaum to the organization
 
### Full list
 * depy webapp environment upgrade - terminate/create prod environment (AWS Elastic Beanstalk) using boto3 library from the publish process
 * Chef - chef.io bumping to version 12.18.31
 * Chef - chefdk bumping to version 1.2.22-1
 * Chef - berkshelf bumping to version 5.6.1 due to new warnings introduced in version 5.6.0 which is the default in chefdk 1.2.22-1
 * Chef/JKEBanking Sample - Fixing a bug where user credentials were hard coded insted of utilizing the user.json configuraiton file #193
 * Chef/Jenkins - Uploading features.json using conversion from json to ruby #194
 * Jenkins/scm_sync feature - feature toggle #195
 * chef upload - feature toggle #196
 * depy/clean - feature toggle #197
 * Jenkins - Bumping to version 2.43 #198
 * webapp - DEPY name in depy.io switched from previous name: DEPI
 * webapp - Github organization depy-io. Moved depy repo from user: lioramilbaum to the organization
 

## 0.0.18

 * Renaming the service. Used to be depi. Now it is depy. 
 * depy website - www.depy.io
 * feature toggle - initial release with Jenkins/scm_sync
 * git/Chef - Fixed a bug. Since jenkins config file included git* attributes (plugin names), knife search returned all nodes which included those attributes. Moved the plugin list from environment to jenkins-master role.
 * rcl/Chef - Fixed a bug. rcl should be deployed before depending applications: UCD, UCR, RPE
 * depy.io nodejs application is deployed with AWS Elastic Beanstalk
 * git/Chef - pinned git version to 2.7.4
 * refactoring - git-server role is dynamically generated from template
 * refactoring - deploy applications loop (according to the list in aaa.json) replacing hard coded application list
 * Bumping:
 	* Ansible - 2.2.1
 	* route53/Chef cookbook - 1.2.1
 	* runit/Chef cookbook - 3.0.4
 	* Jenkins - 2.42
 	* Jenkins plugins - latest and greatest of various plugins
 
## 0.0.17

 * HelloWorld Sample/Ansible 
 * Docker Engine/Ansible - version 1.13.0
 * git/Ansible
 * Jenkins/Chef - Bringing to the same baseline as in Ansible
 * Jenkins/Chef - Bumping cookbook to 4.2.1
 * git/Chef - Bumping cookbook to 5.0.2
 * Ansible - Bumping to version 2.2.1
 * iptables/Chef - Bumping cookbook to 3.1.0
 * chefdk - Bumping to version 1.1.16
 * clm/Chef - code refactoring
 * RPE/Chef - fixed deployment error
 * depy deploy scripts - converted from bash to python
 * Jenkins - Pinning plugin versions and bumping to the latest
 
## 0.0.16

 * CLM - Bumping to version 6.0.3 iFix01
 * RCL/Chef - Bumping to version 8.1.4.5
 * Java/Chef - Bumping cookbook to version 1.46.0
 * RPE/Chef - version 2.1.1, Report Builder web service
 * poise_archive -> ark/chef - Switching cookbooks
 * CLM - Replaced hard coded user info with variables
 * depy_integrations/Chef - git-rtc recipe performance boost. perl installation only for windows and libgit2 is installed via Ubuntu 16.04 official package 
 * IIM - Added support for master password file generation required by IBM repos
 * GIT/Chef - Switched to Ubuntu 16.04 platform
 
## 0.0.15

 * Jenkins/Chef - Initial support for test Kitchen
 * Jenkins/Ansible - Disable Administrative Monitor Notification
 * Jenkins/Ansible - Enable Elastic IPs
 * Jenkins/Ansible - add flexiable-publish & pipeline plugins
 * Jenkins/Ansible - JDK configuration
 * Jenkins script - Backup jobs config XML to git repo
 * Jenkins - bumping to version 2.39
 * Jenkins/Ansible - add a policy to the IAM role to enable push to S3
 * Jenkins/Ansible - Deploy AWS CLI on jenkins node
 * CLM/Ansible+Chef - adding version 5.0.2 support (including screen capture)
 * frontend application - home page
 * Jenkins - Documentation
 
## 0.0.14

 * Initial support for IBM RPE
 * Initial support for centric user management. Already implemented for Jenkins/Ansible
 * Jenkins/Ansible - Run Build job
 * Jenkins/Ansible - Port forwarding, network interface as a parameter
 * Jenkins/Ansible - Attached an AWS policy to an IAM Role
 * Jenkins - bumping to version 2.38
 * Jenkins/Ansible - security. Job list listed before logging in
 * Jenkins/Ansible - configure sbt plugin

## 0.0.13

 * Jenkins - bumping to version 2.37
 * route53 chef cookbook - bumping to versin 1.1.1
 * compat_resource chef cookbok - bumping to version 12.16.3
 * CLM - Switched Capture Screen applications for RTC/RQM due to certificates expirations
 * Refactoring

## 0.0.12

 * Jenkins - bump version 2.36
 * IBM Installation Manager - bump version 1.86
 * Jenkins - switched to Ubuntu 16.04
 * IBM CLM - switched to Ubuntu 16.04
 * IBM CLM - bump version 6.0.3
 * Spotinst - fixed a bug instance launched as ondemand instead of spots
 * compat_resource - bump chef cookbook version 12.16.2

## 0.0.11

 * Jenkins instances infra switched to Ubuntu 16.04 due to dependency created by ansible role - kobanyan.jenkins-jnlp-slave
 * Jenkins instances - Bump Java version to 8 according to Jenkins system requirements recommendations
 * Bump geerlingguy.java ansible role to 1.7.1
 * Ansible - Adding support for private dns names via AWS route53 service
 * Route53 - generic attribute values. Moved chef attributes setting to conf files. Fixed build failure due to missing values.
 * Jenkins/Ansible - Can't login with admin user. user not created during deployment.
 * Jenkins/Chef - Version conf attribute is not picked up
 * runit/chef - Bumped cookbook 3.0.3
 * Jenkins/chef - port forwarding 80->8080
 * Jenkins - configurable http port. Adding http_port conf attribute.
 * Jenkins - wrong default builder credentials
 * Jenkins/Chef - node component recipe didn't run
 * Jenkins/Chef - cookbook refactoring
 * Build breaks when no AWS security group to delete
 * RTC-git/Chef - Fixing the integration
 * CLM/Chef - No space left on device
 * Release process deleted conf/<company> files
 * AWS Security topology improvements - switched to a more generic topology without loosing security level
 * AWS Security - Delete security group failed due to resource dependency. Build failure.
 * Conf files/Ansible - Do not override files during build
 * Jenkins/Chef - Adding node component
 * Jenkins/Chef - Bump jenkins cookbook 4.1.2

## 0.0.9 

Major code refactoring:

* central configuration system (depy/conf)

* Dynamically management AWS security groups

* Two systems: chef and depy. Each launched separately.

* spotinst api token central function

* Applied function naming conventions according to file name

Bumps:

* nodejs chef cookbook - 3.0.0

* Ansible - 2.2.0

## 0.0.8

Consolidated users files in conf/users.json

## 0.0.7

Rename git repo names #12

Merge backend git repos #13

jenkins cookbook dependency is not locked for all cookbooks #42

Bump Jenkins Chef recipe to 4.1.0 #50

Add licensing #48

## 0.0.6

Option to choose between hosted chef and private chef #38

Clean() doesn't delete spotinst groups #25

Use lower case in all values #23

Central configuration file #11

Chef/UCD - Bump to version 6.2.2 #36

## 0.0.5

Using spot instances via SpotInst service

## 0.0.4

Chef/Bump and lock jenkins cookbook to 3.0.0

Chef/Lock compat_resource cookbook to 12.14.7

Ansible/RTC Buildengine node

## 0.0.3

CLM application component deployment by Ansible

System Requirments:

Bumped Chef Development Kit Version: 0.18.30 

## 0.0.1-0.0.2

Initial stages of the project
