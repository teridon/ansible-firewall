ansible-firewall
=========

I want to use the ansible firewalld module to manage my firewall rules on my Redhat guests.  But managing guests in multiple groups was problematic because ansible does not merge dicts easily.  I did not want to change the global behavior for several reasons.  This is based on code from https://witchychant.com/ansible-cumulative-inventory-variables/

Requirements
------------

ansible, python3 (dict merging -- at least with my example code --  does NOT work in python2.7)

Role Variables
--------------

Default rules are included; to add additional rules, add group or host vars, with one the prefixes below

firewall_rules_services_
firewall_rules_ports_
firewall_rules_rich_


Example Playbook
----------------


    - hosts: localhost
      roles:
        - firewall_test

License
-------

BSD

