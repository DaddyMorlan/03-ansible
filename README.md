# Clicktor (Vechouse) playbook + Lighthouse
This playbook can help you to install clickhouse and vector and deploy your vector config on your RHEL-like machines
UPD: this playbook also install and deploy lighthouse trough nginx
# Version
Ver.2
# Requirements
Centos 7
# How to use
> [!TIP]
> All what you need to change located in global_vars directory
### all vars:
- `ssh_key_file` - value is path to your private ssh key
- `ansible_username` - username to ssh connect
### clickhouse vars:
- `clickhouse_version` - clickhouse version that you need to install
- `clickhouse_packages` - list of required packages for clickhouse server
- `clickhouse_address` - address for your machine
### vector vars:
- `vector_version` - vector version that you need to install
- `vector_install_dir` - directory to download and unarchive vector package
- `vector_service_file` - *DO NOT CHANGE* need to register vector as a service
- `vector_config_file` - location to save your vector config *IF YOU CHANGE vector_install_dir YOU NEED TO CHANGE THIS TOO*
- `vector_address` - address for your machine
- `vector_config_path` - local path to vector config file
### lighthouse vars:
- `lighthouse_address` - address for your machine
- `lighthouse_install_dir` - directory to download and unarchive lighthouse package
- `nginx_config_path` - local nginx config path
- `nginx_config_file` - *DO NOT CHANE* path to save nginx config
- `nginx_package` - name of nginx package
- `nginx_port` - port to access lighthouse
## After changes in vars you can start playbook site.yml with inventory/prod.yml inventory file
By command

`ansible-playbook -i inventory/prod.yml  site.yml`

# Screenshots
![](https://github.com/DaddyMorlan/03-ansible/blob/main/screenshots/03%20check.png)
![](https://github.com/DaddyMorlan/03-ansible/blob/main/screenshots/03%20lint.png)
![](https://github.com/DaddyMorlan/03-ansible/blob/main/screenshots/03%20diff.png)
![](https://github.com/DaddyMorlan/03-ansible/blob/main/screenshots/03%20lighthouse.png)
