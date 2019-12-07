Rabbitmq_cluster
================

A role that sets up a RabbitMQ cluster on docker.

Requirements
------------

None

Role Variables
--------------

* rabbitmq_user: "rabbitmq"
* rabbitmq_group: "rabbitmq"
* rabbitmq_image: "rabbitmq:3.8.2-management"
* rabbitmq_port: "5672"
* rabbitmq_persistence_path: "/rabbitmq/data"
* rabbitmq_no_containers: 3 #Number of total containers to set up
* rabbitmq_network_name: "rabbitmqnet"

**Must define**:

* rabbitmq_erlang_cookie: "rabbit"
* rabbitmq_default_password: "rabbit"
* rabbitmq_default_user: "rabbit"


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        rabbitmq_erlang_cookie: "123456789"
        rabbitmq_default_user: "rabbit"
        rabbitmq_default_password: "alice01"
      roles:
         - { role: username.rolename }

License
-------

GNU-GPL V3.0

Author Information
------------------

[Francisco Fregona](franciscofregona@gmail.com)
