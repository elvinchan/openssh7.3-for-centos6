# openssh7.3-for-centos6

refer to https://gist.github.com/faishal/add912b9b4c3899ec26c488a91446a84

the scripts is:
```
cd /opt
timestamp=$(date +%s)
curl -L https://github.com/elvinchan/openssh7.3-for-centos6/releases/download/package/openssh-7.3.tar.gz | tar zx -C /opt/openssh-7.3
cd openssh-7.3
cp /etc/pam.d/sshd pam-ssh-conf-$timestamp
rpm -U *.rpm
yes | cp pam-ssh-conf-$timestamp /etc/pam.d/sshd
/etc/init.d/sshd restart
```
