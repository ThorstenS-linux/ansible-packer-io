# ansible-packer-io
installs packer from HashiCorp under /usr/local/bin/

## example

```
#! /usr/bin/ansible-playbook
---
# run it with
#           ansible-playbook packer-io.yml
#        or ./packer-io.yml
#                        Thorsten Strusch 2017-06-28
####################################################
- hosts: localhost
  become: yes
  gather_facts: true

  vars:
    packer_version: '1.0.2'

  environment:                                                                                                          
    http_proxy: http://proxy:3128/
    https_proxy: http://proxy:3128/

  roles:
    - packer-io

```
