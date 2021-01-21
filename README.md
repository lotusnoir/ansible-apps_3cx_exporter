# Ansible Role: ansible-apps_3cx_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_3cx_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_3cx_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_3cx_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_3cx_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_3cx_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_3cx_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_3cx_exporter.svg)](https://github.com/lotusnoir/ansible-apps_3cx_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_3cx_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_3cx_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_3cx_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_3cx_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_3cx_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_3cx_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_3cx_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_3cx_exporter)

Deploy [3cx_exporter](https://github.com/boynux/3cx-exporter) to expose 3cx metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `cx_exporter_version` | 1.9.1 | 3cx_exporter version |
| `cx_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `cx_exporter_force_install` | false | force install variable |
| `cx_exporter_3cx_host` | localhost | hostname or ip of the 3cx server |
| `cx_exporter_3cx_port` | 3128 | port of the 3cx service on the 3cx server |
| `cx_exporter_listen_port` | 9103 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_3cx_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_3cx_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
