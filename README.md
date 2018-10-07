This kolla-ansible branch install openstack Queens with:
1. ceph integration with config merge feature for:
   - nova
   - cinder
   - glance
   - manila
   - gnochi

Ceph integration files are available in this directory in etc folder.
This files are placed in /etc/kolla/config directory when installation.

2. This branch also use custom ml2conf.ini configuration for custom
   bridge mappings on labnet1 node. Config files are available in this directory
   in etc directory however on real it goes into /etc/kolla/config/neutron dirs

3. This branch excutes installation successfully however functional testing is pending.

4. Next branch will be dedicated to functional testing.
