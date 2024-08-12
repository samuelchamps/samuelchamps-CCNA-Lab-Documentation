# How to configure Routers
``` plaintest
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)# do sh ip int br
R1(config)# interface GigabitEthernet0/0
R1(config-if)# ip address 15.255.255.0 255.0.0.0
R1(config-if)# desc ## SW1 ##
R1(config-if)# no shutdown
R1(config-if)# ip address 182.98.255.254 255.255.0.0
R1(config-if)# desc ## SW2 ##
R1(config-if)# no shutdown
R1(config-if)# ip address 201.191.20.254 255.255.255.0
R1(config-if)# desc ## SW1 ##
R1(config-if)# no shutdown
R1(config-if)# do sh ip int br
R1# copy running-config startup-config
R1#
```
## Result
![Screenshot (85)](https://github.com/user-attachments/assets/b342fa13-5dd3-4c16-9176-b2d1d3738046)
![Screenshot (87)](https://github.com/user-attachments/assets/ea304745-c6ab-4f9e-ae18-a922776c3f49)
