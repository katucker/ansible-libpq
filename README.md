# ansible-libpq
An Ansible role to install the PostgreSQL libpq node module.

This role installs a libpq node.JS module on a Linux system. It handles the details of installing the PostgreSQL
packages and node.JS modules needed for building the libpq module.

This role depends on a variant of the Galaxy Project PostgreSQL role, published as https://github.com/katucker/ansible-postgresql.

The default is to install the original source of the libpq module, https://github.com/brianc/node-libpq, but an alternative version to install can be specified in the Ansible variables for a playbook that uses this role.

The table below defines the variables supported by this role.

|Variable name|Description|Default value|
|-------------|-----------|-------------|
|libpq_pg_version|Version of PostgreSQL to install.|9.4|
|libpq_repo_url|URL of the node-libpq git repository to install.|https://github.com/brianc/node-libpq.git|
|libpq_repo_version|Refspec to check out once the git repository is cloned.||
|dest_folder|Full path to the directory in which the libpq git repository is cloned.|~/node-libpq| 
