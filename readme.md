# asbl-files_copy

## Description

This repo contain the ansible role copy files from local source to destination.
- copy files from local path to remote location
- fix rights on remote location

## Prerequisite

- None

## Usage

### Use role

- Add the role git source in "requirements.yml" file :
```
  - name: role_name
    scm: git
    src: git@github.com:tiny-company/<repository_name>.git
    version: main
```

- And then use the galaxy command to load the file dependencies :
```
ansible-galaxy install -r requirements.yml
```

- Or manually get the playbook as collection (with ansible-galaxy) :
```
ansible-galaxy collection install git@github.com:tiny-company/<repository_name>.git
```

### Variables

For an exhaustive list of variables check the [defaults](defaults/main.yml)
file. Ideally, all values will have commentaries describing what are their
purposes and by the default value you can tell the type.

## Source :

- [stackoverflow article about copying multiple files using ansible](https://stackoverflow.com/questions/36696952/copy-multiple-files-with-ansible)
- [ansible copy module](https://docs.ansible.com/ansible/2.9/modules/copy_module.html)