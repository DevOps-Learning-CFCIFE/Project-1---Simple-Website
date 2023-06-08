Here's a reviewed version of your README content:

# Project-1---Simple-Website
The task of this project is to provision a web server in a Vagrant box with automation and deploy a website onto it.

### Architecture
The project architecture involves using a shell script to run the Vagrant installation from a Vagrantfile. The Vagrantfile, in turn, executes an Ansible playbook responsible for the configuration management of the web server.

## Requirements
To set up and test the project, make sure you have the following requirements fulfilled:

- Install [Vagrant](https://developer.hashicorp.com/vagrant/downloads) and [VirtualBox](https://www.virtualbox.org/wiki/Downloads) on your local machine.
- Clone this repository and navigate to the project directory.
- Run the `start-vagrant.sh` script to initiate the Vagrant setup process.
- Once the virtual machine (VM) is up and running, you can access the website by opening a web browser and entering the IP address of the VM.
- To test the deployment locally, open a web browser on your local machine and enter the IP address `127.0.0.1:8080`. Vagrant forwards port 8080 on your machine to port 80 on the VM, where Apache is running.
- Verify that the website is accessible and displaying the content of your `index.html` file.
- If you encounter any issues with the Vagrant box, you can troubleshoot by running `vagrant ssh` from the directory where the `.vagrant` files are located.

Feel free to customize the website content and structure according to your needs.

If you have any questions or need further assistance, please don't hesitate to ask.