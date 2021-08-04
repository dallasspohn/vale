# TODO

The team needs to check the consistency of private automation hub. Some things to consider:

    Chapter 4.4 (Ansible Builder Validation) automates the installation of private automation hub using custom certificates.

  # Install private automation hub with custom certificates
  install_hub
  
  
  ====================================================================

    Chapter 7.2 (Private Automation Hub Installation) manually installs private automation hub.
        The GE runs the installation from workstation, not hub.
        The GE references hub.example.com not hub.lab.example.com.
        The GE does not use custom certificates.
    Chapter 7.4 (Private Automation Hub Access) might use the same playbooks as 4.4.
    Chapter 7.6 (Private Automation Hub Content) uses a different set of playbooks and certificates to install private automation hub.

Concerns:

    In order to run the manual installation in chapter 7, the hub machine will need to be reset after using it in chapter 4. Individual machine resets have been problematic in the past, so this needs to be tested and I believe the platform team might need to be consulted as well.






    It would be nice for the automated installation in chapter 4 and chapter 7 to use the same playbooks for consistency and ease of maintenance. I don't know which playbooks should be used though.



Worked on chapter 7 privhub-install and content, This is combined with the card Private Automation Hub consistency. 





guides/en-US/sg-chapters/topics/execution/handling-ge.adoc



wget http://materials.example.com/additional_files/ansible-automation-platform-20-early-access/ee-supported-rhel8.tar


START
  setup_check_ansible ${target}
  download_lab_materials ${labname}
  setup_check_podman ${target}

FINISH
  remove_lab_materials ${labname}


