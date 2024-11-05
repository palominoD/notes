# This is the network config written by 'subiquity'
network:
  version: 2
  renderer: networkd
  ethernets:
    ens32:
        addresses:
           - 192.168.20.76/24
        routes:
          - to: default
            via: 192.168.20.254
        nameservers:
             addresses: [8.8.8.8, 8.8.4.4]
