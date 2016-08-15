# Ansible book

This is a simple ansible book to set up a few or several of my personal hosts
automatically.

It includes tasks such as adding my own keys or cloning other repositories I
own.

To run, execute:

```bash
ansible-playbook -i staging site.yml
```

## Custom Variables

These are useful for when a command is supposed to be run once in very specific
conditions.

These are to be appended to the executed line as such:

```bash
ansible-playbook -i stagin site.yml -e "<variable>=<value>"
```

* `pdns_first_run`. When true, tells that PowerDNS is being run for the first
time and a database file should be created.
