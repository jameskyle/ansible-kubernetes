Role Name
=========

Role for deploying kubernetes binaries.

Configuration
------------

The role expects to find the binaries for kubernetes in a directory named after 
the arch of system in files. For example, if deploying to an x86\_64 system, it 
will look for binaries in files/x86\_64/.

Role Variables
--------------

primary\_docker\_host
    hostname for the docker host with the kubernetes controller and proxies.
    default: dock1

mgmt\_addr
    main management interface address. used for services.
    default: ansible_default_ipv4.address

primary\_group
    The main group this host belongs to. Group should contain all the 
    kubernetes docker hosts.
    default: dockers

domain
    domain name for hosts.
    default: localdomain


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: kubernetes, domain: foo.com, mgmt_addr: 192.168.1.10 }


License
-------

BSD

Author Information
------------------

James A. Kyle  
james@jameskyle.org  
https://github.com/jameskyle  
