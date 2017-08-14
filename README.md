# Ansible Role: MySQL Deploy

Configures databases using .sql scripts read from the ./sql subdirectory.

## Requirements

No special requirements.

## Dependencies

None.

## Example Playbook

    - hosts: db-servers
      become: yes
      vars_files:
        - vars/mysql-scripts.yml
      roles:
        - { role: net2grid.mysql-deploy }

*Inside `vars/mysql-scripts.yml`*:

    mysql_scripts:
      - file1.sql
      - file2.sql

## License

MIT / BSD

## Author Information

This role was created in 2017 by NET2GRID BV.
