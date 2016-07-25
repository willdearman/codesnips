## Use new SSH Keys
1) Create new keys
```
ssh-keygen -t rsa -b 4096 -C "will@willdearman.com"
-- /Users/w/.ssh/id_rsa
```
2) Copy files to SSH
```ssh-add ~/.ssh/id_rsa```