# Keepalivedvrrp - Александр Шевцов
![image](https://user-images.githubusercontent.com/25949605/234556082-6876731c-8e65-4434-aff5-df3798a307f9.png)
'''
vrrp_instance test_ip {
state MASTER
interface enp0s3
virtual_router_id 15
priority 100
advert_int 4
authentication {
auth_type AH
auth_pass 1111
}
unicast_peer {
192.168.0.108
}
        virtual_ipaddress {
        192.168.0.150 dev enp0s3 label enp0s3:vip
}
}

