# ansible-role-epel

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-epel.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-epel)

RHEL/CentOS - Extra Packages for Enterprise Linux

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    epel_pkg: epel-release
    epel_ver: latest
    epel_rel: "{{ ansible_distribution_major_version }}"
    epel_arch: noarch
    epel_baseurl: "https://dl.fedoraproject.org/pub/epel"
    epel_release: "{{ epel_pkg }}-{{ epel_ver }}-{{ epel_rel }}"
    epel_fetch: "{{ epel_baseurl }}/{{ epel_release }}.{{ epel_arch }}.rpm"
    epel_repos:
      epel: False
      epel_debuginfo: False
      epel_source: False
      epel_testing: False
      epel_testing_debuginfo: False
      epel_testing_source: False

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.epel
          epel_repos:
            epel: True

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
