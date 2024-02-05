# Docker compose and ansible scripts for tei-publisher.com

The ansible scripts and templates in `./ansible` are used to create the entire tei-publisher.com website.

To build everything, including acquiring a certificate:

```sh
ansible-playbook -i hosts --ask-vault-pass site.yml
```

Obviously you need to know the password for the vault and have the correct host definition in your ssh config.

Updating the site:

```sh
ansible-playbook -i hosts --ask-vault-pass update.yml
```