# PhantomFloodlight: Floodlight SDN connector for Phantom
This project connects the [Floodlight](http://www.projectfloodlight.org/floodlight/) Software Defined Networking (SDN) controller
to the [Phantom](https://www.phantom.us/product.html) security orchestrator.

This allows Phantom to perform command and control functions for Floodlight.

## Currently supported actions

* clear static flows - Remove all static flow rules.
* delete static flow - Remove a static flow rule.
* add static flow - Add a static flow rule.
* list static flows - List static flow rules.
* get uptime - Get time since SDN controller startup.
* list devices - List devices tracked by the SDN controller.
* list external links - List multi-hop links discovered via BDDP.
* list internal links - List single-hop links discovered via LLDP.
* list switches - List SDN switches managed by the controller.
* list firewall rules - List firewall rules stored in the controller.
* delete firewall rule - Delete a firewall rule.
* disable firewall - Disable the firewall.
* enable firewall - Enable the firewall.
* get firewall status - Get the enable/disable state of the firewall.
* unblock flow - Unblock network traffic matching flow parameters.
* block flow - Block network traffic matching flow parameters.
* unblock arp - Unblock ARP packets sourced from this MAC.
* block arp - Block ARP packets sourced from this MAC.
* unblock subnet - Unblocks traffic to/from the matching IP subnet.
* block subnet - Block traffic to/from the matching IP subnet.
* unblock mac address - Unblocks traffic to/from the matching MAC.
* block mac address - Block traffic to/from the matching MAC
* unblock ip - Unblocks traffic to/from the matching IP
* block ip - Block traffic to/from the matching IP.
* test connectivity - Validate the asset configuration for connectivity.

## Deployment instructions

1. Obtain [Phantom](https://www.phantom.us/product.html) appliance from Phantom Cyber (works with Community Edition or Licensed)
2. `tar czf floodlightapp.tgz -C floodlightapp .`
3. From the Phantom web interface, select "Import App" from the *Administration->Apps* tab.
   * Select the `floodlightapp.tgz` file created above
   * Check *"Replace an existing app"* if app is already installed
