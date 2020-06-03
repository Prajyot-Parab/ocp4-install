ocp-cs: Common Services on OCP
=========

This module will install Common Services on OCP.

Requirements
------------

 - Running OCP 4.x cluster is needed.

Role Variables
--------------

| Variable                 | Required | Default                            | Comments                                                  |
|--------------------------|----------|------------------------------------|-----------------------------------------------------------|
| cs_setup_dir             | no       | ~/setup-files/cs-setup             | Place for config generation of Common Services files      |
| cs_operator_name         | no       | ibm-common-service-operator        | Common Services operator name                             |
| cs_project_name          | no       | ibm-common-services                | Namespace to use for installing Common Services operators |
| cs_subscription_channel  | no       | dev                                | Update channel for operator subscription                  |
| cs_subscription_strategy | no       | Automatic                          | Approval stragergy for operator subscription              |
| cs_starting_csv          | no       | ibm-common-service-operator.v3.4.1 | Cluster Service Version for instaling Common Services     |
| cs_operand_list          | no       | ["ibm-cert-manager-operator","ibm-mongodb-operator","ibm-iam-operator","ibm-monitoring-exporters-operator","ibm-monitoring-prometheusext-operator","ibm-monitoring-grafana-operator","ibm-healthcheck-operator","ibm-management-ingress-operator","ibm-metering-operator","ibm-commonui-operator","ibm-ingress-nginx-operator"] | List of Common Services Operators to install |
| storageclass_name        | no       | managed-nfs-storage                | StorageClass name                                         |

Dependencies
------------

 - None

Example Playbook
----------------

    - name: Install common services
      hosts: bastion
      roles:
      - ocp-cs

License
-------

See LICENCE.txt

Author Information
------------------

Prajyot Parab (prajyot.parab@ibm.com)

