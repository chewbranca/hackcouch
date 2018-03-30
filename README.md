# hackcouch

Debian based Vagrant VM dev environment for CouchDB.

# Setup

```
mkdir ~/boxes
mkdir ~/src

git clone https://github.com/chewbranca/hackcouch.git src/hackcouch

ln -s ~/src/hackcouch/VagrantFile ~/boxes/couchdb
ln -s ~/src/hackcouch/playbook.yml ~/boxes/couchdb
ln -s ~/src/hackcouch/erlang.yml ~/boxes/couchdb
ln -s ~/src/hackcouch/couchdb.yml ~/boxes/couchdb

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
