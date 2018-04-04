Ansible role casssandra
=========

Installs Apache Cassandra database

Requirements
------------
Traffic on following ports needs to be allowed between cluster hosts:
7000/tcp # Cassandra inter node
9042/tcp # Cassandra client rpc_port
7199/tcp # Cassanrda JMX

Role Variables
--------------

#### `cassandra_repo_baseurl` (optional)

Apache Cassandra repository url.

#### `cassandra_repo_gpgkey` (optional)

Apache Cassanra repo gpgkey

#### `casssanrda_prerequirements` (optional)

Pre-requirement packages

#### `cassandra_user` (optional)

Apache Cassandra service user

#### `cassandra_user_id` (optional)

Apache Cassandra service user's id

#### `cassandra_group` (optional)
Apache Cassandra service user's group

#### `cassandra_group_id` (optional)
Apache Cassandra service user's group id

#### `cassandra_cluster_name` (required)

Name of the Apache Cassandra cluster.

#### `cassandra_seeds` (required)

Apache Cassandra seeds

#### `cassandra_rpc_address` (optional)

Apache Cassandra RPC address (default 0.0.0.0)

#### `cassandra_listen_address` (optional)

Address to listen

#### `cassandra_broadcast_rpc_address`(optional)

Apache Cassandra broadcast RPC address

#### `cassandra_endpoint_snitch` (optional)

 Endpoint snitch (default SimpleSnitch)

#### `cassandra_dc` (required)

Name of the datacenter

#### `cassandra_rack` (required)

Name of the rack


Dependencies
------------
None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cassandra, tags: cassandra }

License
-------

MIT

Author Information
------------------

Tuomas Vallaskangas
tvallas@iki.fi
