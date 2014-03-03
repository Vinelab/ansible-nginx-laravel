# Ansible NGINX - Laravel
Install nginx and configure it for the [Laravel Framework](http://laravel.com) on Centos/Red Hat

## Installation
Clone this repository inside your ```roles``` directory

## Usage
There must be an ```app``` var with ```sites``` inside it defined as follows:

```yml
vars:
  app:

    sites:
      - title: my-site.com
        domains: www.my-site.com my-site.com admin.my-site.com
        path: /home/my-site
        public_path: /home/my-site/public

      - title: another-site.url
        domains: www.another-site.url another-site.url cdn.another-site.url
        path: /home/another-site
        public_path: /home/another-site/public
````

> you may also specify ```app:``` in a separate YAML file and include it in ```vars_files```