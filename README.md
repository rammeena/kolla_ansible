Its a Full working branch with all core components alongwith
monitoring stack, components are below:
1. Keystone
2. Glance
3. Nova
4. Neutron
5. Cinder
6. Heat
7. Elasticsearch => rocky image does not work, so tag has to be changed to queens release
8. Kibana => rocky image does not work, so tag has to be changed to queens release
9. fluentd
10. telegraf
11. redis
12. memcached
13. mariadb
14. rabbitmq
15. etcd

Tag change process on controllers:

[root@labctl1 ~]# docker images|grep -i kibana
kolla/centos-source-kibana                       queens              dedb6e66dfc3        20 hours ago        570MB
kolla/centos-source-kibana                       rocky               804b3603a01c        20 hours ago        630MB

[root@labctl1 ~]# docker rmi 804b3603a01c

[root@labctl1 ~]# docker tag kolla/centos-source-kibana:queens kolla/centos-source-kibana:rock

Same applies for elasticsearch tag change.


