# Wazuh
Simple Wazuh decoder and rules for Stormshield firewall.

# How to use 🛠️
1) Copy **stormshield_rules.xml** on **/var/ossec/etc/rules**
2) Copy **stormshield_decoder.xml** on **/var/ossec/etc/decoders**
3) Dont forget to chmod ! (*chmod 660* and *chown wazuh:wazuh*)
4) You need to redirect stormshield syslog to your Wazuh manager and configure your manager to accept theses log using [remote](https://documentation.wazuh.com/current/user-manual/reference/ossec-conf/remote.html) section.
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
