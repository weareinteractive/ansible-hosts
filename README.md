# Ansible weareinteractive.hosts role

[![Build Status](https://img.shields.io/travis/weareinteractive/ansible-hosts.svg)](https://travis-ci.org/weareinteractive/ansible-hosts)
[![Galaxy](http://img.shields.io/badge/galaxy-weareinteractive.hosts-blue.svg)](https://galaxy.ansible.com/weareinteractive/hosts)
[![GitHub Tags](https://img.shields.io/github/tag/weareinteractive/ansible-hosts.svg)](https://github.com/weareinteractive/ansible-hosts)
[![GitHub Stars](https://img.shields.io/github/stars/weareinteractive/ansible-hosts.svg)](https://github.com/weareinteractive/ansible-hosts)

> `weareinteractive.hosts` is an [Ansible](http://www.ansible.com) role which:
>
> * manages hosts entries

**Note:**

> Since Ansible Galaxy supports [organization](https://www.ansible.com/blog/ansible-galaxy-2-release) now, this role has moved from `franklinkim.hosts` to `weareinteractive.hosts`!

## Installation

Using `ansible-galaxy`:

```shell
$ ansible-galaxy install weareinteractive.hosts
```

Using `requirements.yml`:

```yaml
- src: weareinteractive.hosts
```

Using `git`:

```shell
$ git clone https://github.com/weareinteractive/ansible-hosts.git weareinteractive.hosts
```

## Dependencies

* Ansible >= 2.4

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---
# hosts_entries:
#   - { ip: '127.0.0.1', domain: 'foobar1.com' }
#   - { ip: '127.0.0.2', domain: 'foobar2.com' }

# list of /etc/hosts entries
hosts_entries: []

```


## Usage

This is an example playbook:

```yaml
---

- hosts: all
  become: yes
  roles:
    - weareinteractive.hosts
  vars:
    hosts_entries:
      - { ip: '127.0.0.1', domain: 'foobar1.com' }
      - { ip: '127.0.0.2', domain: 'foobar2.com' }
      - { ip: '127.0.0.3', domain: 'foobar3.com' }

```


## Testing

```shell
$ git clone https://github.com/weareinteractive/ansible-hosts.git
$ cd ansible-hosts
$ make test
```

## Contributing
In lieu of a formal style guide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

*Note: To update the `README.md` file please install and run `ansible-role`:*

```shell
$ gem install ansible-role
$ ansible-role docgen
```

## License
Copyright (c) We Are Interactive under the MIT license.
