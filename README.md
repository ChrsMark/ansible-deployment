# ansible-deployment

Using this playbook, we automate the proccess of deploying an updated version of a desired Web Application.

Assume we run our WebApp using supervisoctl.

To achive the deployment we have 2 main taks:
 - pull the updated version of master branch of your repo
 - restart supervisorctl
 
 On the very begining of this playbook we notify our slack channel that a deployment is going to take place, so as to inform all team members.
 Also once the last task of the playbook is executed we notify a handler to notify slack again that deployment is completed and what is the last deployed commit.
 
 Usefull:
 - http://docs.ansible.com/ansible/latest/slack_module.html
 - http://docs.ansible.com/ansible/latest/git_module.html
 - http://docs.ansible.com/ansible/latest/supervisorctl_module.html
 
