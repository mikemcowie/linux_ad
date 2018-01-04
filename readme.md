This is a framework for adding linux servers to AD. I intend to make it as generic as possible for use with different clients.
This is meant to conform with Red Hat's recommended configuration 3 from https://access.redhat.com/sites/default/files/attachments/rhel-ad-integration-deployment-guidelines-v1.5.pdf

The playbook variables need to be adjusted to reflect the client dns and kerberos names, ideally this will all be done in the group_vars folder and not in the playbook or task.

You need ssh access -preferably by key - with the user specified in the playbook join.yml, and sudo access (password will later be able to be entered in the vault but for now it needs passwordless sudo access).

The servers that it runs on are specified in the hosts file.

Invoke it by changing into the main directory , running ansible-playbook -i hosts join.yml 
