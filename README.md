# Ansible Playbook: Provisioning Nginx and Docker

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Playbook Structure](#playbook-structure)
- [Tasks](#tasks)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [License](#license)


## Overview

This repository contains an Ansible playbook for automating the provisioning of an Nginx web server and Docker on remote hosts.

## Features

- **Automated Infrastructure Provisioning**: Automates the installation and configuration of Nginx and Docker.
- **Task Tags**: Organizes tasks using tags for easier management and execution.
- **Simple and Efficient**: Simplifies the process of setting up a web server and Docker environment.

## Prerequisites

- Ansible installed on the control machine.
- Proper SSH access to the remote hosts.
- Target hosts listed in the Ansible inventory file.

## Playbook Structure

- **Name**: playbook_1
- **Hosts**: nginx
- **Remote User**: ubuntu
- **Become**: true (using sudo)
- **Tags**: Tags are used to categorize tasks for easier management.

## Tasks

1. **Update and Upgrade Server**:
   - Updates and upgrades the server using `apt`.

2. **Install Nginx**:
   - Installs the Nginx package.

3. **Start Nginx**:
   - Ensures the Nginx service is started and enabled.

4. **Make Nginx Folder**:
   - Creates a folder named "nginx".

5. **Install Docker**:
   - Installs the Docker package.

6. **Start Docker**:
   - Ensures the Docker service is started and enabled.

7. **Make Docker Files**:
   - Creates a folder named "docker_files".
  
## How to Use

1. **Clone Repository**:
   ```bash
   git clone https://github.com/sanjukuruvilla/Ansible-Nginx-Docker-Provisioning.git
   ```

2. **Navigate to Directory**:
   ```bash
   cd Ansible-Nginx-Docker-Provisioning
   ```

3. **Run the Playbook**:
   ```bash
   ansible-playbook -i inventory playbook.yml
   ```

4. **Optional: Use Tags**:
   - You can selectively run tasks using tags:
     ```bash
     ansible-playbook -i inventory playbook.yml --tags "update_upgrade,install_nginx"
     ```

## Contributing

Contributions are welcome! If you find issues or have suggestions for improvements, please open an issue or a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
