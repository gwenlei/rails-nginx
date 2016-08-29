Role Name
=========
gwenlei.rails-nginx

Requirements
------------
ubuntu16.04 xenial

Role Variables
--------------
defaults/main.yml

app_name: demo
nginx_url: http://nginx.org/keys/nginx_signing.key
nginx_repo_install: 'deb http://nginx.org/packages/ubuntu/ xenial nginx'
nginx_user: www-data
nginx_group: www-data
nginx_workers: 2
nginx_connections: 1024
nginx_port: 80
nginx_hostname: localhost
nginx_frame_opt: DENY #(DENY | SAMEORIGIN | ALLOW-FROM)
nginx_accept_mutex: 'on' # if worker_processes > 1 change to on

Dependencies
------------
none

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: gwenlei.rails-nginx }

License
-------
MIT

Author Information
------------------
onecloud
