# ansible-primitive-apache-role (Study project)
This playbook just installs apache2 on your server and changes index.html from root directory (/var/www/html) on your page from [templates](https://github.com/OlgaKochneva/ansible-primitive-apache-role/tree/main/templates)   

Use this playbook -> https://github.com/OlgaKochneva/sopo

## Algorithm
1. Clone sopo repository
```bash
git clone https://github.com/OlgaKochneva/sopo'
```
2. Change hosts in `sopo/environments` (if you need)
3. Run `sudo su` and setup ssh-key
4. In `sopo` run:  
Setup role
```bash
ansible-galaxy install -fr roles/requirements.yml
```
**On success** -> Run playbook:  
```bash
ansible-playbook -i environments/localhost/inventory playbooks/apache.yml -D

```
5. Check on result  
192.168.56.101 - ip addres of vm, where apache2 is installed  
![image](https://user-images.githubusercontent.com/29632527/95781572-c73b0280-0cd6-11eb-91dd-875d555a425a.png)



> Complete uninstallation of apache2 - `apt-get --purge remove apache2 --autoremove`
