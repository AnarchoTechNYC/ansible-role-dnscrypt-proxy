# Anarcho-Tech NYC: dnscrypt-proxy [![Build Status](https://travis-ci.org/AnarchoTechNYC/ansible-role-dnscrypt-proxy.svg?branch=master)](https://travis-ci.org/AnarchoTechNYC/ansible-role-dnscrypt-proxy)

An [Ansible role](https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html) for installing a [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) server. Notably, this role has been tested with [Raspbian](https://www.raspbian.org/) on [Raspberry Pi](https://www.raspberrypi.org/) hardware. This role's purpose is to make it simple to install and run a `dnscrypt-proxy` instance, either locally or as a server, with minimal resources.

## Role variables

* `dnscrypt_proxy_version` - Version of `dnscrypt-proxy` as released from [the `DNSCrypt/dnscrypt-proxy` repository](https://github.com/DNSCrypt/dnscrypt-proxy/releases) to download and use.
* `dnscrypt_proxy_install_prefix` - Absolute filesystem path prefix in which to install `dnscrypt-proxy`. Default: `/opt/local`.
* `dnscrypt_proxy_listen_address` - Address on which to offer `dnscrypt-proxy`'s services. The package default is `127.0.0.1:53`, but this role's default is `:53` (port 53 on all interfaces).

See the [`defaults/main.yaml`](defaults/main.yaml) file for a more thorough example.
