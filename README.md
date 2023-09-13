# Ansible Script for Kanboard Installation

## How to install

* Update the variable for `version` inside the `site.yml`.
* Update the apache2 config under `roles/common/config/kanboard.conf`
* Update the `hosts` file with the correct IP-Adresses

To run this script, just execute the following:

```
ansible-playbook -v -i hosts.yml site.yml
```

## How to update Kanboard from Archive

1. Decompress the new archive
1. Copy the data folder into the newly uncompressed directory
1. Copy your custom config.php if you have one
1. If you have installed some plugins, use the latest version
1. Make sure the directory data is writeable by your web server user
1. Modify .htaccess if needed (f.e. forcing SSL)
1. Test
1. Remove your old Kanboard directory