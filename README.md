# Wazuh
Simple Wazuh decoder and rules for Stormshield firewall.

You need to redirect syslog to your Wazuh server

# How to use 🛠️
1) Copy **stormshield_rules.xml** in **/var/ossec/etc/rules**
2) Copy **stormshield_decoder.xml** in **/var/ossec/etc/decoders**
3) Dont forget to chmod/chown ! (*chmod 660* and *chown wazuh:wazuh*)
4) Configure your manager to accept theses log using [remote](https://documentation.wazuh.com/current/user-manual/reference/ossec-conf/remote.html) 
```
<remote>
  <connection>syslog</connection>
  <port>514</port>
  <protocol>tcp,udp</protocol>
  <allowed-ips>192.168.1.0/24</allowed-ips>
</remote>
```
5) Restart wazuh-manager

That all.

Enjoy :)
