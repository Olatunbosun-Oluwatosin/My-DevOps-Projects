## _Ansible-Automate Project_

### _Installation of ansible_
![](./img/1.%20ansible-installed.png)
Ansible was successfully installed on jenkins-server using the comand below.
"sudo apt update" &&
"sudo apt install -y ansible"

### _ansible-config-mgt_
![](./img/2.%20Job-triggered-automatically.png)

A freestyle job was initiated on jenkins with webhook set to tigger ansible build and this was done successfully.

### _git clone repo_
![](./img/3.%20git-clone-repo.png)
This task was completed using the command "git clone <ansible-cinfig-mgt repo link> as seen in the image.

### _new branch created_
![](./img/4.%20new-branch-created.png)
To begin ansible development, a new branch was expected to be created according to the manual guide. This was done as seen in the image and the name of the new branch is "ansible-newdev".

### _checkout new branch_
![](./img/5.%20newbranch-checkout.png)
New branch checkout was done

### _creation of directories_
![](./img/6.%20step3-task6-completed.png)
According to the guide, we are expected to create directories, "playbooks" & "inventory" in ansible-config-mg.

### _dev inventory_
![](./img/7.%20inventory-dev.png)
These are the values of the hosts.

### _playbook tasks_
![](./img/8.common.yml-file.png)
This yaml file contain the tasks for the playbook which captured all the hosts in consideration.

### _ping module_
![](./img/9.ping-pong-request.png)
This shows a successful ping module request to the hosts(web01, nfs, lb, & web02)

### _pull request_
![](./img/10.pull-request-gitRepo.png)
pull request initiated from the new repository "ansible-config-mgt".

### _merge tasks_
![](./img/11.pull-request-successfully-merged.png)

### _job triggered in jenkins_
![](./img/12.jenkins-job-triggered.png)
After the pull request and merge on github, the job automatically triggered on jenkins due to webhook integration.

### _DB-server playbook_
![](./img/13.db-playbook-executed.png)
The playbook was executed correctly without error.

### _playbook for webservers & other host_
![](./img/14.playbook-executed-successfully.png)
This was done and executed approriately without error.

### _wireshark version_
![](./img/15.%20wireshark-version.png)
This shows that wireshark was installed on the host with the playbook.

Thank you

