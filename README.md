# ansible-role-epel

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-epel.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-epel)

RHEL/CentOS - Extra Packages for Enterprise Linux

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    epel_dist: "{{ ansible_distribution_major_version }}"
    epel_disablerepo: []
    epel_enablerepo: []
    epel_packages: []
    epel_repository_epel: false
    epel_repository_epel_debuginfo: false
    epel_repository_epel_source: false
    epel_repository_testing: false
    epel_repository_testing_debuginfo: false
    epel_repository_testing_source: false

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.epel
          epel_packages:
            - nload
          epel_repository_epel: true

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
