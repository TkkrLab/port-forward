# port-forward
Script to simplify port forwarding




## iptables.conf example:

*nat
<OTHER TABLES>
:PFORWARD -
\#PFORWARD chain is used by the scirpt iptables-forward
-A PREROUTING -i <INTERFACE> -j PFORWARD -m comment --comment "Port forwards"
