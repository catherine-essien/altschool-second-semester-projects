<!-- @format -->

# Setting Up Vagrant

Vagrant is a powerful tool for managing virtualized development environments. This guide will walk you through the steps to set up Vagrant on your system.

## Prerequisites

Before you begin, ensure that you have the following prerequisites:

- A computer running a supported operating system (Linux, macOS, or Windows).
- Virtualization software like VirtualBox, VMware, or Hyper-V installed (Vagrant supports various providers).
- A command-line terminal for running Vagrant commands.

## Installation

Follow these steps to install Vagrant:

1. **Download Vagrant**: Visit the official Vagrant website at [https://www.vagrantup.com](https://www.vagrantup.com) and download the installer for your operating system.

2. **Install Vagrant**: Run the installer and follow the on-screen instructions.

3. **Verify Installation**: To confirm that Vagrant has been installed successfully, open a terminal and run:

    ```bash
    vagrant --version
    ```

    This command should display the installed Vagrant version.

## Getting Started

Now that Vagrant is installed, let's get started by creating a simple Vagrant environment.

1. **Initialize a Vagrant Project**: Create a new directory for your Vagrant project and navigate to it in your terminal. Initialize a new Vagrant project:

    ```bash
    mkdir my_vagrant_project
    cd my_vagrant_project
    vagrant init
    ```

    This will create a `Vagrantfile` in your project directory. The `Vagrantfile` is used to configure your virtual machine.

2. **Choose a Box**: Vagrant uses "boxes" as base images for virtual machines. You can find a variety of boxes at [https://app.vagrantup.com/boxes/search](https://app.vagrantup.com/boxes/search) or create your custom box.

3. **Configure the `Vagrantfile`**: Open the `Vagrantfile` in a text editor and specify the box you want to use and any additional configuration. For example, to use the "ubuntu/bionic64" box:

NB don't forget passwd
    ```ruby
    Vagrant.configure("2") do |config|
      config.vm.box = "ubuntu/focal64"
    end
    ```

4. **Start the Virtual Machine**: In your project directory, run the following command to start the virtual machine:

    ```
    vagrant up
    ```

5. **SSH into the Virtual Machine**: After the virtual machine is up and running, you can SSH into it using:

    ```
    vagrant ssh
    ```

6. **Shutdown and Destroy**: When you're done with the virtual machine, exit the SSH session and run:

    ``
    vagrant halt
    ```

    To completely remove the virtual machine and associated resources, use:

    ```
    vagrant destroy
    ```







