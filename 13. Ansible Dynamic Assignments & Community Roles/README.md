## Ansible Dynamic Assignments & Community Roles

### _import = Static_
### _include = Dynamic_
The module that enables dynamic assignments is _include_


### _dynamic-assignments_
![](./img/1.%20new-branch-created.png)
"dynamic-assignments" as a new branch was created on Github repository. On git-bash, the command "git checkout -b dynamic-assignments" was used to switch from the main branch to the new branch.

### _directory created_
![](./img/2.%20new-folder-created.png)
A new directory was created on the Jenkins-Ansible server with same name as the new branch. With "mkdir dynamic-assignments", a new directory was created.

### _content of env-vars.yml file_
![](./img/3.%20env-vars-file.png)
The yaml file is used to set variables for ansible dynamic assignments.

### _git exercise_
![](./img/4.%20git-output01.png)
while in a project directory inside the local jenkins-ansible server, "git init" was used to initialize a Git repository and other git commands follows as in the project guide.

### _MYSQL Role_
![](./img/5.%20geerlingguy-mysql.png)
"ansible-galaxy init geerlingguy.mysql" command was deployed to create a new MYSQL role.
A directory "mysql" was created and "mv geerlingguy.mysql/ mysql" move the output to the new created directory.

### _layout for geerlingguy_
![](./img/6.%20tree-geerlingguy.png)
The image display has the layout of the geerlingguy and this is achieved through the below command;
"tree mysql/geerlingguy.mysql/" within the role directory.

### _git push_
![](./img/7.%20git-push-upstream.png)
command "git push --set-upstream origin roles-feature". push commits from the local repository to a remote repository while setting the upstream branch for the current local branch. it tells Git to associate the local branch with a branch on the remote repository.
### _git pull request_
![](./img/8.%20git-pull-request.png)
The initial push request generated a pull request on the remote repository with the new branch "roles-feature"

### _git merge_
![](./img/9.%20git-online-repo-merge.png)
The new branch "roles-feature" was merge with the main branch on GitHub as seen in the image.

### _nginx & apache load balancer_
![](./img/10.%20ansible-role-nginx-apache-installed.png)
With the available roles from the community, nginx and apache load balancer was installed using the commands as seen in the image. 
### _roles rename_
![](./img/11.%20rename-role-nginx-apache.png)

### _variable value set as false_
![](./img/12.%20apache-variable-false.png)
According to the project guide/manual, the variable valuse for both load balancers are expected to be set to _"false"_.

### _nginx variable_
![](./img/13.%20nginx-variable-false.png)
variable value set at _"false"_ using vim editor.

### _environmental variable_
![](./img/14.%20environmental-variable.png)
To enable nginx and to activate the load balancer, this is set to true while apache load balancer is set to false.
### _ansible inventory run_
![](./img/15.%20ansible-inventory-accessible.png)
A ping module was initiated on ansible inventory to be sure that the master can communicate to other server via ssh and parameters provided in the inventory
### _git push_
![](./img/16.%20git-push-dynamic-assignments.png)
This is to push update to the remote repository on the branch specified "dynamic-assignments".
### _ansible playbook_
![](./img/17.%20playbook--.png)

After updating inventory for each environment, ansible was run against each environment.

Run command "ansible-playbook playbooks/site.yml -i inventory/uat.yml"

Learnt and practiced how to use Ansible configuration management tool to prepare UAT environment for Tooling web solution.
