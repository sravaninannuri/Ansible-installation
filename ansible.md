create a new user
passwd user
add the user to sudoers file
visudo 
ansadmin all=(all) nopasswd:all
next enable password based login
vi /etc/ssh/sshd_congiguration
service sshd reload
enable passwd based authentication yes
ssh-key-gen
copy ssh keys to the manged node ssh-copy-id ansadmin@ip addreess of manged node
do the same thing on managed node
create a new user
passwd user
add the user to sudoers file
visudo 
ansadmin all=(all) nopasswd:all
next enable password based login
vi /etc/ssh/sshd_congiguration
service sshd reload
enable passwd based authentication yes
install the ansible
yum install ansible
the defaule locaton of ansible is /etc/ansible
in this you will find ansible.cfg/hosts/roles
changes to be made and used ina configuration file which will processed in follwing order

* ANSIBLE_CONFIG (AN ENVIRONMENT VARIABLE)
*ansible.cfg (in the current directory)
*ansible.cfg (in the home direwctory)
*/etc/ansible/ansible.cfg
