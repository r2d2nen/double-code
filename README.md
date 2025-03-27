# Headder

This is for testing



## Steps taken for double repo storage

1. Set up a repo
	1. git init
	2. git add .
	3. git commit -m "first commit"

2. Push the code to first storage
	1. git remote set-url origin <SSH-link>

3. Set up SSH Authentication (if not there)
	1. Have SSH-key: 
		- Coppy public key and add to GitLab
	2. Don't have SSH key:
		- In terminal type: ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
		- Coppy public key and add to GitLab

4. 
