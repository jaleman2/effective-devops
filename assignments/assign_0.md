* sudo rpm -i 'http://pkgs.repoforge.org/rpmforge-release/rpmforge-release-0.5.3-1.el6.rf.x86_64.rpm'
* sudo vi /etc/yum.repos.d/rpmforge.repo
Change "enabled 0" to "enabled 1". The section should look as follows:

```

[rpmforge-extras]
name = RHEL $releasever - RPMforge.net - extras
baseurl = http://apt.sw.be/redhat/el6/en/$basearch/extras
mirrorlist = http://mirrorlist.repoforge.org/el6/mirrors-rpmforge-extras
#mirrorlist = file:///etc/yum.repos.d/mirrors-rpmforge-extras
# The following line will change!! 
enabled = 1
protect = 0
gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
gpgcheck = 1

```
* sudo yum update git
