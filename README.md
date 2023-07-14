## CKAN Ansible Deployment
This repository contains Ansible playbooks and configurations for deploying and managing CKAN, an open-source data management platform. The provided Ansible scripts automate the setup and configuration of CKAN instances, making it easier to deploy and maintain CKAN in a standardized and reproducible manner.


Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/ckan-ansible-deploy.git
cd ckan-ansible-deploy
```

Edit the inventory file hosts vars and add the target deployment servers' IP addresses or hostnames.

Customize the deployment configurations in group_vars/all.yml to match your requirements. Modify any necessary variables such as database credentials, CKAN versions, and other specific settings.

Run the Ansible playbook to deploy CKAN:

```
ansible-playbook playbook.yml
```

## Configuration

The  `host_vars/_01.yml` file contains configuration variables that can be customized according to your deployment needs. These variables include database credentials, CKAN version, data storage paths, and other CKAN-specific settings. Review and modify these variables before running the Ansible playbook.

## Contributing
We welcome contributions to enhance and improve this CKAN Ansible deployment repository. If you have suggestions, bug fixes, or new features, feel free to submit a pull request. Please follow the contribution guidelines outlined in the CONTRIBUTING.md file.

## License
This repository is licensed under the MIT License. You are free to use, modify, and distribute this repository in accordance with the terms specified in the license.
