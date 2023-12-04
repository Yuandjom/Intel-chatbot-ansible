# Customer Chatbot Environment Setup with Ansible
## Overview
This repository contains an Ansible playbook for setting up a customer chatbot environment. It is designed to automate the deployment and configuration of a chatbot application,
leveraging the AI Starter Kit for Customer Chatbot using Intel® Extension for PyTorch, as found in the [oneapi-src/customer-chatbot](https://github.com/oneapi-src/customer-chatbot) GitHub repository.

## Project Structure
The Ansible playbook is structured into multiple roles, each handling a specific part of the setup process:

- **setup_environment:** Configures environment variables and workspace directory.
- **install_dependencies:** Installs necessary packages like Git and Apache2 Utils.
- **setup_conda:** Handles the installation and setup of the Miniconda environment.
- **setup_python:** Sets up Python in the Conda environment and installs required Python packages.
- **setup_git_repo:** Clones the necessary GitHub repository and sets up the project structure.
- **setup_data_dir:** Sets up data directories and downloads necessary data files.
- **setup_torchserve:** Installs TorchServe and its dependencies.
Each role has its own directory under the `roles/` directory, with a `tasks/main.yml` file containing relevant tasks.

## Prerequisites
Ansible 2.9 or later.
Access to an Ubuntu-based system where you have administrative privileges.

## Usage
1. **Clone the Repository:** Start by cloning this repository to your local machine or the control node.

```
git clone https://github.com/yuandjom/ansible-customer-chatbot.git
cd ansible-customer-chatbot
```
2. **Configure Variables:** Edit the vars/main.yml file to set up your workspace path and other variables.

3. **Run the Playbook:** Execute the Ansible playbook.
```
ansible-playbook -i hosts.ini setup_customer_chatbot.yml -vv
```
This command will run the playbook and execute each role sequentially.

## Customization
You can customize the playbook according to your requirements by editing the tasks in the respective roles. Ensure that you understand each role's functionality before making changes.

## Contributing
Contributions to this playbook are welcome. Please follow the standard GitHub pull request process to submit your changes.

## References
AI Starter Kit for Customer Chatbot using Intel® Extension for PyTorch: [GitHub Repository](https://github.com/oneapi-src/customer-chatbot)
