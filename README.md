# Headder

This is for testing



## Steps taken for double repo storage

1. Set up a repo
	1. git init
	2. git add .
	3. git commit -m "first commit"

2. Push the code to first storage
	1. git remote set-url origin <SSH-link>
		git branch -M main

3. Set up SSH Authentication (if not there)
	1. add SSH-key to website 
		1. Have SSH-key: 
			- Coppy public key and add to GitLab
		2. Don't have SSH key:
			- In terminal type: ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
			- Coppy public key and add to GitLab
	2. make sure you use the SSH-key in your repo
		1. ssh-add -l
		2. If not set, set it by: ssh-add ~/.ssh/id_rsa

4. 


## Extras

vim  ~/.ssh/config 


	Host git.aza.nu
	        HostName git.aza.nu
	        User rikard.helgegren
	        IdentityFile ~/.ssh/id_rsa


	Host github.com/rikard-helgegren
	        HostName github.com
	        User rikard-helgegren
	        IdentityFile ~/.ssh/id_rsa_personal_use

ssh-add -l
ssh-add ~/.ssh/id_rsa
