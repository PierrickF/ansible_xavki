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

* With `apt`:<br>
`sudo apt install ansible`
* With `pip`:<br>
`sudo apt install python3-pip`<br>
`pip3 install ansible`

* The managed node requires Python.<br>
If Ansible fails to detect it we can specify it in the inventory file:<br>
`ansible_python_interpreter=/usr/bin/python3`

# 3. SSH Setup

1. If working with Docker, setup a virtual network:<br>
`docker network create my_network`

2. Add each container to the virtual network:<br>
`docker network connect my_network my_container`

3. Install SSH and start the SSH service on both machines.

4. Generate an SSH key on the control node with `ssh-keygen`.

5. Copy the key to the managed node with `ssh-copy-id`.

6. Check that Ansible can use SSH:<br>
`ansible -i "managed_node_name_or_ip," all -m ping`
