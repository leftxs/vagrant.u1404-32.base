=====================
vagrant.u1404-32.base
=====================

Vagrant Base Box for based on `Ubuntu`_ 14.04 with `Ansible`_ as provisioner.

This will setup a Ubuntu 14.04 - 32 bit server with Jenkins and Apache. The network is bridged, you can change that in the Vagrantfile.

This is written for `Debian`_ and `Ubuntu`_ , the Makefile will most likely **not work** on other OS's, same goes for the virtualenv setup.

Features
========

- Makefile for easy setup
- `vagrant-cachier plugin <http://fgrehm.viewdocs.io/vagrant-cachier>`_
- provioning is done via `Ansible`_


Dependencies
============

- virtualenv
- ...

Installation
============

Install/Setup it like that::

    git clone https://github.com/leftxs/vagrant.u1404-32.base.git

Run Makefile::

    make bootstrap
    source bin/activate

This will setup a virtualenv in vagrant.jenkins and will install Ansible via pip

If you don't want to use the Makefile you can also do it from hand::

    virtualenv --python=python2.7 .
    source bin/activate
    pip install ansible
    vagrant plugin install vagrant-cachier

Now work with vagrant as usual::

    vagrant up

You can get now a cup of coffee or something else, because that will take a while....
After the building is done you can browse to $IPOFVBOX and should see Jenkins

Contribute
----------

- Issue Tracker: github.com/leftxs/vagrant.u1404-32.base/issues
- Source Code: github.com/leftxs/vagrant.u1404-32.base

License
-------

GPLv2



.. _Jenkins: http://jenkins-ci.org/
.. _Ubuntu: http://www.ubuntu.com/server
.. _Debian: https://www.debian.org/
.. _Ansible: http://www.ansible.com/home

