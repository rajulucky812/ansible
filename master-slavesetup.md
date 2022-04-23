Do Master and agent side:
useradd ansible
passwd ansible

edit visudo
ansible    ALL=(ALL)       NOPASSWD:ALL

edit /etc/ssh/sshd_config
PasswordAuthentication yes

systemctl restart sshd

su ansible
ssh-keygen -t rsa

exit

----------------------------------------------
Master:
ssh-copy-id ansible@agentpublicip

/etc/ansible/hosts
[agents]

35.159.33.236 ansible_user=ansible


/etc/ansible/ansible.cfg

sudo_user = anisble

inventory      = /etc/ansible/hosts
