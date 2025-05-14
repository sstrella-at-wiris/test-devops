## Technical Test - Jr Devops - Santiago

1. **Install Prerequisites**:
    - Download and install [Vagrant](https://www.vagrantup.com/).
    - Download and install [VirtualBox](https://www.virtualbox.org/).

2. **Clone the Repository**:

    ```bash
        git clone <repository-url>
        cd <repository-folder>
    ```

3. **Start the Vagrant Environment**:
    - Run the following command to initialize and start the virtual machine:
      ```bash
      vagrant up
      ```

4. **Check if app is running**:
    - Go to the browser and put the following URL:
        ```localhost:8080 ```


4. **Access the Virtual Machine**:
    - SSH into the virtual machine in case you need to check it:
      ```bash
      vagrant ssh
      ```

6. **Shut Down the Environment**:
    - When done, stop the virtual machine:
      ```bash
      vagrant halt
      ```

7. **Destroy the Environment (Optional)**:
    - To remove the virtual machine completely:
      ```bash
      vagrant destroy -f
      ```

Refer to the project's documentation for additional details or troubleshooting steps.