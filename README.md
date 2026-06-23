# AAP2 "Almost" Dynamic Surveys

Dynamic survey has been [a request from the community](https://github.com/ansible/awx/issues/20) for almost a decade.

The feature has yet to appear in AWX and Ansible Automation Platform (AAP). 

Until then, you're left with an "almost dynamic" option.

Indeed, survey specifications can be updated in an automated manner!

This repository contains an example of playbook that can be used as a job template and scheduled on a regular basis in AAP.

Now you can extend this example playbook to call external APIs. A simple example is retrieving a list of VLANs from Netbox.

The job template can also be included as a step in an AAP workflow. Let's assume a new VLAN has been deployed but the survey is not yet up to date, you can run the survey update prior to running the provisioning step.
