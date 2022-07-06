# webserver-ec2

This CI script is writing in yaml

This playbook automates the setup of a webserver and an instance to run that webserver

It main point of entry is the main.yml file

It has 1 play which is the 
-setup

The setup workflow
-updates dependences
-creates a web folder
-copies files to that folder and serves the web files
The path to the setup play is roles/setup/tasks/main.yaml
The web file is a javascript file, that is in the roles/files/index.js

It also comes with a custom CI script to automate the job of building and testing the code for our webserver

To run this playbook localy ensure that you have ansile configured locally by running the show command python3 -m pip show ansible

and run the playbook with the following command ansible-playbook main.yml
