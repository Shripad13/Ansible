ansible.builtin.debug - for print a messg, like echo in bash

ansible.builtin.shell - allows you to run shell commands using the system’s shell

ansible.builtin.command - runs the command directly, which is safer and preferred when shell features aren’t needed.

ansible.builtin.package - This modules manages packages on a target without specifying a package manager module
(like ansible.builtin.dnf, ansible.builtin.apt, …)




✅ state: present  #means:"Make sure the package is installed."
If the package is already installed, Ansible does nothing (it's idempotent). If it's not installed, Ansible will install it.
✅state: absent   #Ensure the package is removed/uninstalled.
✅state: latest   #Ensure the latest version of the package is installed.

state: started        #Ensures the service is running.
enabled: yes          #Configures the service to start automatically on boot.
become: yes           #Instructs Ansible to escalate privileges (e.g., using sudo) for executing tasks.

# In Ansible if one taks fails then successive task will not execute & stops there only, so for exceptions handling sometimes you can use below -

ignore_errors: True          # ignore_errors is a predefined keyword in Ansible to ignore the errors of a task, if the task fails, it will not stop the playbook execution.

