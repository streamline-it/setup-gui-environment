Role Name
=========

setup-gui-environment installs XOrg on a RHEL or FreeBSD system.

Requirements
------------

None.

Role Variables
--------------

# FreeBSD.yml under vars
setup_gui_environment_pkgs:
  - xorg

setup_gui_environment_svcs:
  - 

# defaults file for setup-gui-environment

# name of the driver
setup_gui_environment_driver_name:

# name of the video driver package
setup_gui_environment_driver_pkg:
# will usually contain "kld_list"
# Ex.

# setup_gui_environment_sysrc_directive:
#  - name: kld_list
#    value: "{{ setup_gui_environment_driver_name }}"
setup_gui_environment_sysrc_driver_directive: 
  - 
# user allowed to user the gui
setup_gui_environment_user: 
  - username:
    groups:


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        setup_gui_environment_driver_pkg: drm-kmod

        setup_gui_environment_driver_name: radeonkms

        setup_gui_environment_sysrc_directive:
          - name: kld_list
            value: "{{ setup_gui_environment_driver_name }}"
 
      roles:
        - name: setup-gui-environment 

License
-------

BSD

Author Information
------------------
streamline-it


