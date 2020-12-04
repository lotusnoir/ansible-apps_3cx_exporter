# Ansible Role: ansible-apps_3cx_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_3cx_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_3cx_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__3cx_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_3cx_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_3cx_exporter/tags)

Deploy [3cx_exporter](https://github.com/boynux/3cx-exporter) to expose 3cx metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `3cx_exporter_version` | 1.9.1 | 3cx_exporter version |
| `3cx_exporter_3cx_host` | localhost | hostname or ip of the 3cx server |
| `3cx_exporter_3cx_port` | 3128 | port of the 3cx service on the 3cx server |
| `3cx_exporter_listen_port` | 9103 | port to expose prometheus metrics |

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

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
