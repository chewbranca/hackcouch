# hackcouch

Debian based Vagrant VM dev environment for CouchDB.

# Setup

```
mkdir ~/boxes
mkdir ~/boxes/couchdb
mkdir ~/src

git clone https://github.com/chewbranca/hackcouch.git ~/src/hackcouch

ln -s ~/src/hackcouch/VagrantFile ~/boxes/couchdb
ln -s ~/src/hackcouch/playbooks_enabled/ ~/boxes/couchdb/playbooks_enabled

cd ~/boxes/couchdb
vagrant up
...

vagrant ssh
tmux -2

cd src/couchdb
./configure
make couch
./dev/run --with-haproxy --haproxy /usr/sbin/haproxy --admin=adm:pass

Hack the planet!
```
