# Ansible NGINX - Laravel
Install nginx and configure it for the [Laravel Framework](http://laravel.com) on Centos/Red Hat

## Installation
Clone this repository inside your ```roles``` directory
or add as submodule: `git submodule add git@github.com:Vinelab/ansible-nginx-laravel roles/nginx`

## Usage

- **required**
    - `title` being the title of the site, will be used to name the config/logs file(s)
    - `domains` the domains that provides reachability to this site, will be the `server_name` in nginx config
    - `path` the root of the site
    - `public_path` the public document where the site will be served from
- optional
    - `listen` specify the port that the site listens to

```yaml
vars:

  nginx:
    sites:
      - title: my-site.com
        domains: www.my-site.com my-site.com admin.my-site.com
        path: /home/my-site
        public_path: /home/my-site/public

      - title: another-site.url
        listen: 8080
        domains: www.another-site.url another-site.url cdn.another-site.url
        path: /home/another-site
        public_path: /home/another-site/public

```
