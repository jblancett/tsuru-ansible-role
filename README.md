# tsuru-ansible-role
Ansible role for installing tsuru

Each service can be skipped or disabled using the variables listed below or via command line with --skip-tags

Variables
---------
Set any of these to false to disable the associated service:
* tsuru_install_docker
* tsuru_install_mongodb
* tsuru_install_redis
* tsuru_install_hipache
* tsuru_install_gandalf-server
* tsuru_install_archive-server
* tsuru_install_docker-registry
* tsuru_install_tsuru-server

* tsuru_docker_options
  command line options for starting the docker daemon
  default: --insecure-registry="0.0.0.0/0" -H tcp://0.0.0.0:2375 -H unix:///var/run/docker.sock

* tsuru_mongodb_config
  A hash you can use to set extra config options in mongodb.  By default it is empty

* tsuru_server_config
  This hash contains all of tsuru server's config options.

* tsuru_hipache_config
  Same as above but for hipache

* tsuru_gandalf_config
  Same as above but for gandalf-server