# depi framework CHANGELOG

This file is used to list changes made in each version of the depi framework.
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

* central configuration system (depi/conf)

* Dynamically management AWS security groups

* Two systems: chef and depi. Each launched separately.

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
