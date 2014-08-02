# Ansible Hosts Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-role-hosts.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-role-hosts)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-role-hosts.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-role-hosts)

> `hosts` is an [ansible](http://www.ansible.com) role which: 
> 
> * adds `/etc/hosts` entries

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.hosts
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.hosts
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-role-hosts.git
```

## Variables

```
# hosts:
#   - { ip: '127.0.0.1', domain: 'foobar.com' }

# array of ip and domain names to add to /etc/hosts
hosts: []
```

## Example playbook

```
- host: all
  roles: 
    - franklinkim.hosts
  vars:
    hosts:
      - { ip: '127.0.0.1', domain:'foobar.com' }
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-role-hosts.git
$ cd ansible-role-hosts
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
