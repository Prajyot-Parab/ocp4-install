ocp-upgrade: Upgrade OCP cluster
=========

This module will upgrade existing OCP cluter to a latest nightly version.

Requirements
------------

 - Running OCP 4.x cluster is needed.

Role Variables
--------------

| Variable                 | Required | Default                            | Comments                                                  |
|--------------------------|----------|------------------------------------|-----------------------------------------------------------|
| upgrage_release_file_url | no       | https://mirror.openshift.com/pub/openshift-v4/ppc64le/clients/ocp-dev-preview/latest-4.4/release.txt | URL to release.txt file of a latest nightly build |

Dependencies
------------

 - None

Example Playbook
----------------

    - name: Upgrade OCP cluster
      hosts: bastion
      roles:
      - ocp-upgrade

License
-------

See LICENCE.txt

Author Information
------------------

Prajyot Parab (prajyot.parab@ibm.com)

