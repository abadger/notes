---
tags: ansible-releng, template, email
title: Major release announcement
---

Hi all,

We're happy to announce that the Ansible 5.0.0 alpha1 package is now available! This update is based on the ansible-core-2.12.x package which is a major update from the one used by Ansible 4.  Ansible 4 was based on Ansible Base 2.11.x. There may be backwards incompatibilities in the core playbook language.  Please see the porting guide for details.

This is an alpha release so we encourage people to use it to test that their playbooks and workflows work with the upcoming major release and report any bugs to the relevant bug trackers (https://github.com/ansible/ansible/ for bugs in ansible-core and the relevant collection for bugs in a collection's modules and plugins).


How to get it
-------------

Due to a limitation in pip, if you are upgrading from Ansible 3 (or earlier), you need to uninstall Ansible and Ansible Base before installing Ansible 5:

```
$ pip uninstall ansible ansible-base
$ pip install ansible==5.0.0a1 --user
```

The tar.gz of the release can be found here:

* Ansible 5.0.0a1:
https://pypi.python.org/packages/source/a/ansible/ansible-5.0.0a1.tar.gz

  SHA256: d96c8db1fa61c18421c3775b3d24cd8c0ac48c85dc13b511a802c144626082a4
  
What's new in Ansible 5.0.0
---------------------------

* This version of Ansible is based on Ansible Core 2.12 which is a new major update of the ansible-core package.  It may contain backwards incompatible changes to the playbook language and command line programs.  Please see the porting guide (linked at the bottom) for more information.

* ansible-core-2.12 now requires Python 3.8 or greater on the controller (where you run ansible-playbook).  Managed nodes continue to support Python 2.7 and Python 3.6 or greater unless noted otherwise in a specific module's documentation.

* Collections which have opted into being a part of the Ansible 5.0.0 unified changelog will have an entry on this page:
  * https://github.com/ansible-community/ansible-build-data/blob/main/5/CHANGELOG-v5.rst

* For collections which have not opted into the unified changelog, consult the list of included collections in the link below and check their entry on https://galaxy.ansible.com for information about their changes.
  * https://github.com/ansible-community/ansible-build-data/blob/main/5/ansible-5.0.0.deps

* You can find more information for those on
https://galaxy.ansible.com/. For instance, the community.crypto collection listed in the ansible deps file has a galaxy page at https://galaxy.ansible.com/community/crypto/

* The changelog for Ansible Core 2.12, which this release of ansible installs, is located here: https://github.com/ansible/ansible/blob/stable-2.12/changelogs/CHANGELOG-v2.12.rst


What's the schedule for new Ansible 5.0.0?
---------------------------------------------------------

* The Ansible-5 final release is expected on 2021-11-30. For the full release schedule, including dates for other pre-releases, see the roadmap page:
  * https://docs.ansible.com/ansible/devel/roadmap/COLLECTIONS_5.html

* New minor releases will occur approximately every three weeks (Ansible 5.1.0, Ansible 5.2.0, etc).  They will contain bugfixes and new features but no backwards incompatibilities.

* Once Ansible 5.0.0 final has been released, updates to Ansible 4 will stop.
  * We've been putting together a document on issues that would need to be addressed if someone would like to volunteer to create long term updates: https://hackmd.io/plQlGzcFRFGLnPXIeg3cwQ


Porting Help
-------------

A unified porting guide for collections which have opted-in is available here: https://docs.ansible.com/ansible/devel/porting_guides/porting_guide_4.html