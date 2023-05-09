There are some manual steps that must be done before running this playbook:

Install ansible and a couple of roles:

    sudo apt-get install ansible
    sudo ansible-galaxy collection install community.general
    sudo ansible-galaxy collection install ansible.posix
    sudo ansible-galaxy install lean_delivery.java

The file "/home/sesam/.docker/config.json" must be manually created (either by copying the file from an
existing build agent, or by running "docker login" for the "sesamci" user.


Example: To install the playbook on the "performance-test-agent2" box, ssh to the "performance-test-agent2" box 
         go to this folder and run the following command:

    sudo ansible-playbook site.yml --extra-vars "custom_teamcity_single_agent_name=performance-test-agent2"

Machine needs to be rebooted after ansible playbook is installed.
