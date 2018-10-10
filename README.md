This kolla-ansible fully function verified install openstack Queens with:
1. ceph integration with config merge feature for:
   - nova
   - cinder
   - glance
   - manila
   - gnochi - not verified

=============================================================================
openstack keypair create --public-key ~/.ssh/id_rsa.pub mykey
openstack flavor create --id 0 --vcpus 2 --ram 1024 --disk 10 m1.nano

openstack image create "centos" --file /home/iso/CentOS-7-x86_64-GenericCloud-1808.qcow2 --disk-format qcow2 --container-format bare --public

 openstack image create "cirros" --file /home/iso/cirros-0.4.0-x86_64-disk.img --disk-format qcow2 --container-format bare --public

openstack network create --provider-network-type flat --provider-physical-network dmz_core mynet

openstack subnet create --network mynet --subnet-range 172.16.16.0/24 --allocation-pool start=172.16.16.100,end=172.16.16.250 --gateway 172.16.16.1 my-subnet

openstack security group list

openstack security group rule create --proto tcp --dst-port 22 <security-group-id>
openstack security group rule create --proto icmp <security-group-id>
