Notes
=======
```
sudo apt-get install dh-systemd  bzr python-paramiko dh-autoreconf pbuilder build-essential
```

cat ~/.dput.cf
```
[haproxy-1.5]
fqdn = ppa.launchpad.net
method = sftp
incoming = ~makinacorpus/haproxy-1.5
login = kiorky
allow_unsigned_uploads = 0
```
# MERGE UPSTREAM
git remote rm o
git remote add o http://git.haproxy.org/git/haproxy-1.5.git/
git fetch --all
git rebase -i o/master
./mc_packages/sync_debian.sh


Packaging (/debian) is the last DSC for vbernat ppa (no vivid package for a long time)

