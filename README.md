# Baas_Credential - Repo

##  This playbook is maintained by cloud ops team and used for provisioning access of BaaS users on to K8-Worker & Shell Servers.

* Check if users in the list provided by Ryan have home directory on Quincy filer "10.50.20.*".
* Create a ticket to create home directory, refer to INC2606983.
* Once ticket is completed, login on to AWX server (qnc-ccp-awx-prod-01.juniper.net) at path /root/baas/ update or appened users list provided by Ryan in the file baas_user.
* Run the Job from template "Users access to BaaS Env - Workers_Shell servers" [http://qnc-ccp-awx-prod-01.juniper.net/#/templates/job_template/143]
