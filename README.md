# Ansible Files Role

[![Build Status](https://img.shields.io/travis/weareinteractive/ansible-files.svg)](https://travis-ci.org/weareinteractive/ansible-files)
[![Galaxy](http://img.shields.io/badge/galaxy-franklinkim.files-blue.svg)](https://galaxy.ansible.com/list#/roles/)
[![GitHub Tags](https://img.shields.io/github/tag/weareinteractive/ansible-files.svg)](https://github.com/weareinteractive/ansible-files)
[![GitHub Stars](https://img.shields.io/github/stars/weareinteractive/ansible-files.svg)](https://github.com/weareinteractive/ansible-files)

> `files` is an [ansible](http://www.ansible.com) role which:
>
> * manages files

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.files
```

Using `requirements.yml`:

```
- src: franklinkim.files
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-files.git franklinkim.files
```

## Dependencies

* Ansible >= 1.9

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# files:
#   - path: /etc/foo.conf
#     state: touch
#     mode: "u+rw,g-wx,o-rwx"
#

# list of file definitions (http://docs.ansible.com/file_module.html)
files: files
```

## Example playbook

```
- hosts: all
  sudo: yes
  roles:
    - franklinkim.files
  vars:
    files:
      - path: /tmp/foo.conf
        state: touch
        mode: "u+rw,g-wx,o-rwx"
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-files.git
$ cd ansible-files
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
