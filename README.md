# Ansible NGINX - Laravel

## Installation
Clone this repository inside your ```roles``` directory

## Usage
There must be an ```app``` var defined with:

- ```domains``` will be the ```server_name``` which should list your domains/sub-domains
- ```public_path``` representing the app's root directory

> you may also specify ```app:``` in a separate YAML file and include it in ```vars_files```

```yaml
vars:
    - app:
        domains: domain.com sub.domain.com
        public_path: /var/www/public
```