
##  Cloud ops team maintains this playbook and is used to provide BaaS users access to BaaS Worker & Shell Servers.

* Login to any shell server as * * root * * to check if users in the Ryan list have a home directory on the Quincy filer. Run the command underneath.
                    *python /root/preflightcheck.py <user1> <user2> <user3>*

  - If the result is *<user1> ==> Missing Home*, create Service-Now ticket for user home directory creation in QNC filer with unix team. ( eg: INC2648614, INC2606983 ). Once the ticket has been completed, provide access to keep the process complete.

  - If the result is *<user1> ==> Missing Account*. Check if there is a user [https://find.juniper.net]. If not, proceed with providing access to the rest of the users.

* Run the Job from template "Users access to BaaS Env - Workers_Shell servers" [http://bng-ccp-awx-prod-01.juniper.net/#/templates/job_template/113]

* Provide usernames as a list or comma-separated.

* Once job is completed successfully, login to any shell sever to verify the status by running command
                  *python /root/preflightcheck.py <user1> <user2> <user3>*
