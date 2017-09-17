SyncToGoogleStorage
===================

Sync content into Google Compure Storage (with gsutil).

![Build status](https://travis-ci.org/jylitalo/SyncToGoogleStorage.svg?branch=master) 

Requirements
------------

gsutil command line utility and project in Google Computing Environment.

Role Variables
--------------

* bucket: where content will be stored
* chdir: where content is stored locally
* gsutil: define if gsutil is not in PATH
* location: EU/US/us-central1 (depends on storage_class)
* project: project name in Google Compute Environment
* storage_class: Standard/regional/...
* dirs:
  - {src: ".", dest: "", extra_args: "-x images"}
  - {src: "images", dest: "images", extra_args: ""} 

Dependencies
------------

None

Example Playbook
----------------

    - hosts: server
      tasks:
      - include_role
        name: SyncToGoogleStorage
      vars:
        dirs: {src:".", dest:"", extra_args:""}

License
-------

MIT

Author Information
------------------

Juha Ylitalo, juha.ylitalo@gmail.com, http://www.ylitalot.com/
