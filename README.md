Postgres
========

This role is written for internal use by Awesto and not designed to cover
more general use-cases. You probably do not want to use it.

Requirements
------------

None.

Role Variables
--------------

postgres_version: the version of PostgreSQL to use, e.g:

```
    postgres_version: 9.4
```

postgres_databases: a list of mappings such as this:

```
    - postgres_databases:
      - database: mydb
        username: myuser
        password: secret
```

Dependencies
------------

None

Example Playbook
----------------

- hosts: dbservers
  roles:
    - postgres
  vars:
    - postgres_version: 9.4
    - postgres_databases:
      - database: mydb
        username: myuser
        password: secret

License
-------

BSD

Author Information
------------------

René Fleschenberg <rene@fleschenberg.net>
