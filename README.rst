===================
Packer Cloud Images
===================

|Travis| |License|

.. |Travis| image:: https://img.shields.io/travis/adfinis-sygroup/packer-cloud-images.svg?style=flat-square
   :target: https://travis-ci.org/adfinis-sygroup/packer-cloud-images
.. |License| image:: https://img.shields.io/github/license/adfinis-sygroup/packer-cloud-images.svg?style=flat-square
   :target: LICENSE

Build your own AWS and Azure Packer images from scratch within minutes.

Features
========
Most cloud providers like AWS or Azure provide prebuilt images for different
Linux distributions through a marketplace. The quality and usability differs
from image to image. Therefore it makes sense to build your own images to
provide VMs tailored to your use case. In addition it gives you full control
how and when the images are updated.

This repository makes use of Packer_ and Ansible_ to build custom images for a
few Linux distributions. These images should fullfil the following requirements:

* Minimal installation
* Tailored to the corresponding cloud
* Support for either AWS or Azure

After building the images upload them to the specific cloud and start spawn VMs
from them.

Requirements
============
Ensure the following requirements are installed:

* Ansible_
* Packer_
* QEMU / KVM
* azure_linux_image_ Ansible role

.. _Ansible: http://docs.ansible.com/ansible/latest/intro_installation.html
.. _Packer: https://www.packer.io/intro/getting-started/install.html
.. _azure_linux_image: https://galaxy.ansible.com/adfinis-sygroup/azure_linux_image

Installation
============
Follow the steps below to build the images:

.. code:: shell

       $ ansible-galaxy install -r requirements.yml
       $ packer-io build centos7.5-lvm-qemu.json

Pick any of the available JSON files to build an image for the required
distribution.

Contributions
=============
Contributions are more than welcome! Please feel free to open new issues or
pull requests.

License 
=======
GNU GENERAL PUBLIC LICENSE Version 3

See the `LICENSE`_ file.

.. _LICENSE: LICENSE
