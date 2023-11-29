# Wazuh
Simple Wazuh decoder and rules for Stormshield firewall.

You need to redirect all stormshield syslog to your Wazuh manager and configure your manager to accept theses log using [remote](https://documentation.wazuh.com/current/user-manual/reference/ossec-conf/remote.html) section.

Example:
```
<remote>
  <connection>syslog</connection>
  <port>514</port>
  <protocol>tcp,udp</protocol>
  <allowed-ips>192.168.1.0/24</allowed-ips>
</remote>
```

# How to use 🛠️
1) Copy **stormshield_rules.xml** on **/var/ossec/etc/rules**
2) Copy **stormshield_decoder.xml** on **/var/ossec/etc/decoders**
3) Edit **ossec.conf** to add theses files.
4) Restart wazuh-manager

That all.

Enjoy :)
