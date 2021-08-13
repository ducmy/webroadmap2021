# Control source auth by ssh via Github
![alt text](https://lh4.googleusercontent.com/5yiydW8T6_dNMPhDrudotWlwtcGl7s1R4sRVhvCdcY5TD9JDMDvezppiu23JyHW95Z5jDUNqzcqsOwrHx3Zm4Q=w1920-h937-rw)

### Github
##### Create repo with private access

git@github.com:Ducmy/test_ssh.git (private access)

### Ubuntu PC
##### create work dir
``` bash
mkdir practice_ssh_gh
mkdir keys
```

#### Generating a new SSH key
``` bash
$ssh-keygen -t ed25519 -C "nguyenducmy393@gmail.com"

Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/cnvs_my/.ssh/id_ed25519): ./keys/testssh_repo
Enter passphrase (empty for no passphrase): (press password)
Enter same passphrase again: 				(press password again)
Your identification has been saved in ./keys/testssh_repo
Your public key has been saved in ./keys/testssh_repo.pub
The key fingerprint is:
SHA256:rVpHtGOhLs+BDBzTW... nguyenducmy393@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|        ... .    |
|     . o o+o o   |
|    o o +o=o. o  |
|   . = . =o+ . + |
|    + ....  .. o E|
|     o o B...= . |
|      + * o o.+  |
|       * o o ..o |
|      . o  .o ...|
+----[SHA256]-----+


$cat ./keys/testssh_repo.pub
ssh-ed25519 <hash> nguyenducmy393@gmail.com  (copy this and paste to key in github repo)
```
### Github
Pass to new key to https://github.com/Ducmy/test_ssh/settings/keys/new

Allow write access ? 


### Ubuntu PC
```bash
$git clone git@github.com:Ducmy/test_ssh.git
Cloning into 'test_ssh'...
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Resolutions

$ssh-add <private_key>

exp:
ssh-add keys/testssh_repo
Enter passphrase for keys/testssh_repo: 
Identity added: keys/testssh_repo (nguyenducmy393@gmail.com)
```

### SUMMARY
practice_ssh_gh (here you are ssh access auth, via ssh-add ./keys/testssh_repo)
  
 ```bash
├── keys
│   ├── testssh_repo		(private key: 
│   └── testssh_repo.pub
└── test_ssh				(your repo)
    └── test
 
$git clone
$git pull
```
								
### Note
	Each folder can be managed by ssh, shout specify which private for repo, or we
	can use the same key, whatever.
	
	Github have two common key
		1.For full repo access by managed https://github.com/settings/keys
		2.For repo access which practice by above steps

### 参考 Tham khao
https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/about-ssh
