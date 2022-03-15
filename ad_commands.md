File Transfer

ansible agents -m copy -a "src=abc.txt dest=/home/ansible/abc.txt”

Installing Package:
ansible all -b -m yum -a "name=tree state=present"

Uninstalling Package:
ansible master -b -m yum -a "name=httpd state=absent“

Creating user:
ansible all -b -m user -a "name=raju password=12345678“

Deleting user:
ansible all -b -m user -a "name=raju state=absent" 

Managing services:
ansible  servers  -m service -a "name=jenkins state=started"  

Getting Facts: ansible all -m setup
![image](https://user-images.githubusercontent.com/97225776/158425709-85d07980-4b96-4bc5-99b4-7754329a846b.png)
