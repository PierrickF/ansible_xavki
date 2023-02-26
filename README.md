[Full Ansible training course](https://www.youtube.com/playlist?list=PLn6POgpklwWoCpLKOSw3mXCqbRocnhrh-)

# 1. Concepts and Definitions

* **control node**<br>
A dedicated machine where Ansible is installed, to push from or pull to.

* **managed nodes**<br>
Machines we want to configure with Ansible.

* **inventory**<br>
One or multiple files, listing machines and variables.

* **groups**<br>
Machines can be organized in groups in the inventory.

* **group_vars**<br>
Variables for entire groups.

* **host_vars**<br>
Variables for a specific machine.

* **tasks**<br>
Actions such as commands, anything that is *done*.

* **modules**<br>
Scripts that can be called by tasks.

* **roles**<br>
Sets of tasks, variables and such that work together.

* **playbooks**<br>
Files that map roles to the inventory.

* **plugins**<br>
Packages, libraries, plugins for Ansible.

# 2. Installation

* With `apt`<br>
```
sudo apt install ansible
```
* With `pip`<br>
```
sudo apt install python3-pip
pip3 install ansible
```

* The managed node requires Python.<br>
If Ansible fails to detect it we can specify it in the inventory file:<br>
```
ansible_python_interpreter=/usr/bin/python3
```
