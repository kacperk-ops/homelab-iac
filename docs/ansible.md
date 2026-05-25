# Initial configuration

1. Install required collections via ansible-galaxy

`ansible-galaxy collection install -r requirements.yml`

2. Change **remote_user** and **private_key_file** in **ansible/ansible.cfg** to match your enviroment

3. Create Ansible Vault based on **ansible/group_vars/vault.yml.example**

`ansible-vault create ansible/group_vars/vault.yml`

4. Install required helm charts

`helm repo add prometheus-community https://prometheus-community.github.io/helm-charts`

`helm repo add gitea-charts https://dl.gitea.com/charts/`

5. Install required helm plugins

`helm plugin install https://github.com/databus23/helm-diff --verify=false`

6. Install required python libraries

`pip install kubernetes`