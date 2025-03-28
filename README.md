# Headder Changed

This is for testing



## Steps taken for double repo storage

### Set up first repo

1. Set up a repo
	1. git init
	2. git add .
	3. git commit -m "first commit"

2. Push the code to first storage
	1. git remote set-url origin "SSH-link"
		git branch -M main

3. Set up SSH Authentication (if not there)
	1. add SSH-key to website 
		1. Have SSH-key: 
			- Coppy public key and add to GitLab
		2. Don't have SSH key:
			- In terminal type: ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
			- Coppy public key and add to GitLab. Can be found at: ~/.ssh/id_rsa.pub
	2. make sure you use the SSH-key in your repo
		1. ssh-add -l
		2. If not set, set it by: ssh-add ~/.ssh/id_rsa

4. Push code with: git push -u origin main

### Set up second repo

1. Check where we are pushing currently: git remote -v
2. Add where next to push:
	1. git remote set-url --add --push origin "SSH-link"
	2. Make sure SSH-key is added
3. Check new destination is added pushing: git remote -v
	There should now be both push destinations.


## Extras

vim  ~/.ssh/config 


	Host git.aza.nu
	        HostName git.aza.nu
	        User User1
	        IdentityFile ~/.ssh/id_rsa


	Host github.com/rikard-helgegren
	        HostName github.com
	        User user2
	        IdentityFile ~/.ssh/id_rsa_personal_use


vim .git/config

	[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
        ignorecase = true
        precomposeunicode = true
	[remote "origin"]
	        url = git@gitlab.com:double-code/double-code.git
	        fetch = +refs/heads/*:refs/remotes/origin/*
	        pushurl = git@github.com:r2d2nen/double-code.git
	        pushurl = git@gitlab.com:double-code/double-code.git
	[user]
	        name = rikard-helgegren
	        email = qsx574@AB-G4VYFL91Q1
	[branch "main"]
	        remote = origin
	        merge = refs/heads/main



