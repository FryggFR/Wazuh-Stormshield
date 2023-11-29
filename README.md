# Wazuh
Simple Wazuh decoder and rules for Stormshield firewall.

You need to redirect all stormshield syslog to your Wazuh manager.

# How to use 🛠️
1) Copy **stormshield_rules.xml** on **/var/ossec/etc/rules**
2) Copy **stormshield_decoder.xml** on **/var/ossec/etc/decoders**
3) Edit **ossec.conf** to add theses files.
4) Restart wazuh-manager

That all.

Enjoy :)
