# Synergy Configuration with Ansible

A group of ansible scripts produced on an account in DXC.technology for OneView in order to configure the Proof of Concept Synergy server

In this GitHub, it holds the structure of files in order for the Ansible playbooks to work.

## PLAYBOOKS: 
All the plabooks are in the path of: roles, where you will see the set of folders. Each folder holds a tassk file and a main.yml file which is the playbook itself. In order to get items to work with Ansible Tower, we have commented out the config file and any reference to variable directory. If running playbooks outside of Ansible Tower (Using Putty), then these will need to be commented back in.

#### Tower run Playbooks:
This folder is for the Ansible Tower to use to run the playbooks stored in this GitHub. They are structured very similar to the site.yml file as this is the formate Ansible Tower reads the playbooks. They hold very small functions that call out the playbooks

## VARIABLES: 
If needing a variable file, ensure a 'vars' folder has been created in each folder on the same level as the 'tasks' folder. Then ensure the playbooks are linked up to this directory.
The account variable file is not on here, but an example one is. If needing the used file, please contact someone in the Synergy POC team

## CONFIG FILE:
The file details are not on the site for security reasons. If required, please contact the Nucleus Synergy POC team. When recieved, the file should go in the 'top' folder (same location as the current ansible.cfg file)

### TIP:
If wanting to produce Ansible with multiple functions (example delete multiple ethernet functions), copy the required code and paste directly under and change the relevant details. Ansible will read the playbook and complete the tasks
