# Ansible

These are my personal ansible roles & playbooks, mainly intended to deploy web
servers with Drupal or regular web applications (php, python, static).

***This is a continuous work in progress***

## Requirements from Ansible Galaxy

Install ansible-galaxy external roles

`ansible-galaxy install -r galaxy.yml`

## Structure

    ├── README
    ├── ansible.cfg
    ├── galaxy.yml
    ├── hosts
    │   └── hosts_example
    │   └── hosts                   (not versionned)
    ├── playbooks
    │   ├── playbook-example.yml
    │   └── playbook.yml            (not versionned)
    └── roles
        ├── debian_common
        ├── apache
        ├── mysql
        ├── php                     ( version 5.6 or 7 )
        └── drupal                  ( version 7 or 8, install composer & drush)

## Examples

Run the main playbook on every hosts :

    ansible-playbook playbooks/playbook.yml

Specify a custom inventory :

    ansible-playbook -i hosts/another_hosts_file playbooks/playbook.yml

Specify a custom host :

    ansible-playbook -l <myhost> playbooks/playbook.yml

## Todo

- Use Vault to store secret (MySQL root password, ...)
- Manage MySQL db & user
- Manage vhosts file
- Nginx role

## Credits & special thanks

- JocelynD for your [ansible roles](https://code.crapouillou.net/jocelyn/ansible-roles) and personnal explanations.
- [Jeff Geerling](https://github.com/geerlingguy) for all your generic roles !
- Sanpi for your [ansible roles](https://gitlab.com/sanpi/ansible/)
