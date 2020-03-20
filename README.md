# redhat-install

### update packages

```
sudo yum update
# reboot after update
reboot
```

### install node, npm & yarn
```
sudo yum install -y gcc-c++ make
curl -sL https://rpm.nodesource.com/setup_12.x | sudo -E bash -
sudo yum install nodejs
# install yarn
curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
sudo yum install yarn
```

### install git

> from https://www.tecmint.com/install-git-centos-fedora-redhat/

```
sudo yum install git
```

### install nginx

> from https://www.cyberciti.biz/faq/how-to-install-and-use-nginx-on-centos-7-rhel-7/

write in file  `/etc/yum.repos.d/nginx.repo`
``
[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/mainline/rhel/7/$basearch/
gpgcheck=0
enabled=1
```
then run commands
```
sudo yum install nginx
sudo systemctl enable nginx
