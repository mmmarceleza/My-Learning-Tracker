# ANSIBLE

[![HOME](../../img/button_home.png)](https://github.com/mmmarceleza/My-Learning-Tracker#marcelos-learning-tracker) &nbsp; &nbsp; [![MY ARTICLES](../../img/button_article.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/my-articles.md#my-articles) &nbsp; &nbsp; [![PORTFOLIO](../../img/button_portfolio.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/portfolio.md#portfolio) &nbsp; &nbsp; [![LEARNING LOG](../../img/button_log.png)](https://github.com/mmmarceleza/My-Learning-Tracker/blob/master/content/learning-log.md#learning-log)

***

## What is Ansible?

Ansible is an open source tool that enables automation, configuration and orchestration of infrastructure.

## Characteristcs:

It makes your job easier:
- automating deployment of applications
- easily manage multi server systems
- make configurations one time
- reduces all around complexity
	
Introduces infrastructure as code
- build out entire systems in code
- store all code in source control
- roll back changes if needed
- share code with other team members
	
Builds confident
- produce reliable and repeatable systems
- ensure technologies and configurations are properly setup
- reduces human error and other risks
	
Simple to integrate
- simple to install and integrate into your current setup
- easy to learn syntax
- start automation configuration and infrastructure in minutes
	
Other key features
- written in python
- script commands using YAML syntax
- sends commands to nodes via SSH
- commands area executed sequentially on each node
- each node runs commands in parallel
- Ansible is owned by Red Hat
	
## Why, when and where use Ansible

1. Mass Deployments: Ansible helps solves the problem of manually updating servers one by one.
2. Scaling: Ansible can be used as a configuration management tools to ensure identical environments when scaling to meet demands.
3. Migrating Environments: Ansible can be used as a tool for migrating applications from integration, testing and production in a reliable and dependable way.
4. Failure Prevention: Ansible can be used as a tool for reviewing change logs and rolling back applications if failures do occur.

## Similar tools

- Ansible
    - only install once
    - pushed based
    - uses YAML as syntax
    - control machine must be Linux/Unix
- Puppet
    - must be installed on all machines
    - pull based
    - uses Puppet DSL as syntax
    - control machine must be Linux/Unix

- Chef
    - must be installed on all machines
    - pull based
    - uses Ruby as syntax
    - control machine must be Linux/Unix

- Salt
    - must be installed on all machines
    - pull/pushed based
    - uses YAML as syntax
    - control machine must be Linux/Unix