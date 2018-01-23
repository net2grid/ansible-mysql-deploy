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
	  - script1.sql
	  - script2.sql
	
	mysql_scripts_repository:
	  url: "git@github.com:somebody/some-repository.git"
	  branch: "some_branch" 
	
	checkout_path: "/some/directory"
	
## License

MIT / BSD

## Author Information

This role was created in 2017 by NET2GRID BV.
