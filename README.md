# AAP2 "Almost" Dynamic Surveys

Dynamic survey has been [a request from the community](https://github.com/ansible/awx/issues/20) for almost a decade.

The feature has yet to appear in AWX and Ansible Automation Platform (AAP). 

Until then, you're left with an "almost dynamic" option and one major limitation.

Indeed, survey specifications can be updated in an automated manner. 

The limitation I'm talking about is that if your AWX/AAP has multiple surveys enabled on a job template (e.g. name of the artifact and version of the artifact), you can't dynamicallly update the version of the artifact once chosen in the list.

You can update a survey by using `survey.yml` that can be used as a job template in AWX/AAP. You can schedule the job when the survey needs updating.

Now you can extend `survey.yml` to call external APIs and take the return values as input. A simple example is retrieving a list of VLANs from Netbox.
