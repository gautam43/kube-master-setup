kube_master_setup
=========
This role is used to setup the master node in the kubernetes cluster 

Requirements
------------
To use this rule, first requirement is to launch the ec2_launcher role which launches instances and copy the master IP to the inventory in a [kube-master] group and similarly worker IP in the [kube-worker]. use the dynamic inventory concept to add the IPs dynacally.
Role Variables
--------------
1. cidr - The CIDR pool used to assign IP addresses to pods in the cluster. By default, each node in the cluster is assigned a /24 network from this pool for pod IP assignments.
2. loc_dir - This variable is used for the location of the directory or workspace where the role is located or resides.
Dependencies
------------
Other roles required are gautam43.ec2_launcher for launching the instances of master and slave
Example Playbook
----------------
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: kube-master
      roles:
         - role: gautam43.kube-master-setup
License
-------
MIT
Author Information
------------------
For the Queries contact me on:-
Gmail - gautamkhatri43@gmail.com
