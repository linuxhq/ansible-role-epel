# ansible-role-epel

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-epel.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-epel)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-epel-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/epel)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

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

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
