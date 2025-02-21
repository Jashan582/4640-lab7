Commands:

Step one: 

The first step is to create our  key pairs using the command

ssh-keygen -t rsa -b 4096 -f ~/.ssh/aws

This command creates our public and private keys

Step Two:

The second step is to add the key to the SSH agent

ssh-add ~/.ssh/aws


Step three: 

Then we Cd into the dirictory that has import_lab_key and run 

./import_lab_key ~/.ssh/aws.pub

This command imports the import key into the .ssh/aws.pub

Step four:

Run the play book the command will change a bit depending on the directory you are in 

ansible-playbook -i inventory/hosts.yml playbook.yml

This command runs a ansible playbook on the hosts defined in the inventory file


