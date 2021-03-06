Dopr
========

A minimal CLI tool for Provisionning Digital Ocean Droplets, and Creating Domains/Subdomains.

Pre-requisites
------

- Set your Digital Ocean Token as an environment variable **DO_TOKEN**

Installation

:: 

    $ pip install python-digitalocean 
    $ pip install --index-url  https://test.pypi.org/simple/ dopr

------

OR 

::

    $ pipenv install
    $ python setup.py bdist_wheel
    $ pip install -I dist/dopr-0.1.0-py2.py3-none-any.whl

Usage
------

List Droplets :

::

    $ dopr -l


Destroy All droplets & domains

::

    $ dopr --clean

Destroy Specific Resource

::

    $ dopr -d droplets
    $ dopr -d domains



Create Droplets :

::

    $ dopr -c 1 centos s-1vcpu-1gb


Create Droplets and Install some packages :

::

    $ dopr -c 1 centos s-1vcpu-1gb -p python vim

Create Droplets with an Ansible inventory

::

    $ dopr -c 3 ubuntu s-1vcpu-1gb --with-inventory app db redis
    # an inventory file will be created for the 3 instances, each instance with each label, eg: [app]


Droplets Status :

::

    $ dopr -s


Add Domains & Subdomains :

::

    $ dopr -a 1.1.1.1 domain.com sub1 sub2
    # domain.com will be created for IP 1.1.1.1, and also sub1.domain.com / sub2.domain.com



Python Support
---------------

- Python 2 & 3  :grinning:




















