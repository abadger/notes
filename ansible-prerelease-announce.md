Hi all,

We're happy to announce that the ansible-3.0.0 beta1 package is now available! This update is based on the ansible-base-2.10.x package just like ansible-2.10 was so the changes shouldn't be too major.  However, it does contain new major versions of many collections which means that there will be some backwards incompatible changes in the modules and plugins.

How to get it
-------------

Due to a limitation in pip, if you are upgrading from Ansible 2.9 (or earlier), you need to uninstall ansible before installing the 3.0.0b1 version:

```
$ pip uninstall ansible
$ pip install ansible==3.0.0b1 --user
```

The tar.gz of the release can be found here:

* Ansible 3.0.0b1
https://pypi.python.org/packages/source/a/ansible/ansible-3.0.0b1.tar.gz
SHA256: 1da8059604136e520cd4f6e0792309dbf6ef79b927e6c41afc194fb418b23855

What's new in Ansible 3.0.0b1
-----------------------------

* The Ansible package has moved to semantic versioning (https://semver.org/).  This standard allows you to tell if a new version of Ansible contains incompatibilities by looking at the version number.  Read the semver specification for more information.

* Collections which have opted into being a part of the Ansible-3.0.0b1 unified changelog will have an entry on this page:
https://github.com/ansible-community/ansible-build-data/blob/main/3/CHANGELOG-v3.rst

* For collections which have not opted into the unified changelog, consult the list of included collections in the link below and check their entry on https://galaxy.ansible.com for information about their
changes.
  * https://github.com/ansible-community/ansible-build-data/blob/main/3/ansible-3.0.0b1.deps

* You can find more information for those on
https://galaxy.ansible.com/. For instance, the community.crypto collection listed in the ansible-3.0.0b1.deps file has a galaxy page at https://galaxy.ansible.com/community/crypto/

* Changelog for ansible-base-2.10.6 which this release of ansible installs: https://github.com/ansible/ansible/blob/stable-2.10/changelogs/CHANGELOG-v2.10.rst

What's the schedule for new Ansible releases after 3.0.0b1?
-------------------------------------------------------------------

* Except for ansible-2.9.x, older versions of ansible are not seeing maintenance releases.  If there is a desire for maintenance releases of older versions, drop by a Community Working Group Meeting to discuss how you can help. (
https://github.com/ansible/community/tree/main/meetings#wednesdays )
* Since we have not updated the ansible-base major version in this release, we decided that a quick release schedule was preferred. There will be one release candidate, on February 9.  If no blockers are discovered, Ansible-3.0.0 final will happen on February 16, 2021.
* Minor releases of ansible-3.0.0 will be released approximately every three weeks.  Since we're now using semantic versioning, these new releases will be 3.1.0, 3.2.0, etc.  They will contain bugfixes and new features but no backwards incompatibilities.


Porting Help
-------------

There's a unified porting guide for collections which have opted-in. You can find that at:
https://github.com/ansible/ansible/blob/devel/docs/docsite/rst/porting_guides/porting_guide_3.rst 