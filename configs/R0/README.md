# R0 configuration

## R0 (ASN 65007 - Uruguay)

```
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname R0
!
boot-start-marker
boot-end-marker
!
!
!
no aaa new-model
clock timezone -03 -3 0
mmi polling-interval 60
no mmi auto-configure
no mmi pvc
mmi snmp-timeout 180
!
!         
!
!
!
!
ip cef
no ipv6 cef
!
multilink bundle-name authenticated
!
!
!
!
!
!
!
!
!
redundancy
!
!
! 
!
!         
!
!
!
!
!
!
!
!
!
interface Ethernet0/0
 description RO <--> R2
 ip address 198.18.144.1 255.255.255.252
 ipv6 address 2002:F000:E:20::1/64
!
interface Ethernet0/1
 description RO <--> R1
 ip address 198.18.144.9 255.255.255.252
 ipv6 address 2002:F000:E:10::1/64
!
interface Ethernet0/2
 no ip address
 shutdown
!         
interface Ethernet0/3
 no ip address
 shutdown
!
router bgp 65007
 bgp router-id 10.0.0.1
 bgp log-neighbor-changes
 neighbor 198.18.144.2 remote-as 65007
 neighbor 198.18.144.2 description R0 <--> R2
 neighbor 198.18.144.10 remote-as 65007
 neighbor 198.18.144.10 description R0 <--> R1
 !
 address-family ipv4
  neighbor 198.18.144.2 activate
  neighbor 198.18.144.2 soft-reconfiguration inbound
  neighbor 198.18.144.2 route-map NADA in
  neighbor 198.18.144.10 activate
  neighbor 198.18.144.10 soft-reconfiguration inbound
  neighbor 198.18.144.10 route-map NADA in
 exit-address-family
!
ip forward-protocol nd
!         
!
no ip http server
no ip http secure-server
!
!
ip prefix-list DENY-ALL seq 5 deny 0.0.0.0/0
!
route-map NADA permit 10
 match ip address prefix-list DENY-ALL
!
!
!
control-plane
!
!
!
!
!
!
!
line con 0
 logging synchronous
line aux 0
line vty 0 4
 login
 transport input all
!
!
end

```

