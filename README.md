# Clicktor (Vechouse) playbook
This playbook can help you to install clickhouse and vector and deploy your vector config on your RHEL-like machines
# Version
There will be no more versions anymore
# How to use
> [!TIP]
> All what you need to change located in global_vars directory
### all vars:
- ssh_key_file - value is path to your private ssh key
- ansible_username - username to ssh connect
### clickhouse vars:
- clickhouse_version - clickhouse version that you need to install
- clickhouse_packages - list of required packages for clickhouse server
- clickhouse_address - address for your machine
### vector vars:
- vector_version - vector version that you need to install
- vector_install_dir - directory to download and unarchive vector package
- vector_service_file - *DO NOT CHANGE* need to register vector as a service
- vector_config_file - location to save your vector config *IF YOU CHANGE vector_install_dir YOU NEED TO CHANDGE THIS TOO*
- vector_address - address for your machine
- vector_config_path - local path to vector config file
## After changes in vars you can start playbook site.yml with inventory/prod.yml inventory file
By command

`ansible-playbook -i inventory/prod.yml  site.yml`

# Screenshots