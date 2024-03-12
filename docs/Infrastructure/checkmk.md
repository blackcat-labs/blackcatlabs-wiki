# CheckMk
Black Cat infrastructure is monitored using [:octicons-link-external-16: CheckMk](https://checkmk.com/) raw edition.

## Servers
Currently CheckMk is running on the following servers:  
- [:material-arrow-right: Beholder](<Servers/Server Inventory/beholder.md>)

## Docs
Helpful documentation:
- [:octicons-link-external-16: CheckMk Docs: Setting up monitoring](https://docs.checkmk.com/latest/en/intro_setup_monitor.html)  
- [:octicons-link-external-16: Proxmox Monitoring: How to Do it Efficiently with Checkmk](https://checkmk.com/blog/proxmox-monitoring)  
- [:octicons-link-external-16: Network Monitoring with Checkmk: 3 rules to rule them all](https://checkmk.com/blog/network-monitoring-with-checkmk-2-0)

## Adding a host
1.  Add a new host in the control plane
    1.  *On the CheckMk server,* Click to *Setup > Hosts > Hosts*
    1.  Click *Add host*
    1.  Fill out the following information:
        1.  Hostname: the server name (e.g. for `beholder.blkcat.space`, you would use `beholder`.)
        2.  IP address family: leave default to `IPv4 only`
        3.  IPv4 address: check the box and enter the server's **Tailnet IP address** (starts with `100.`)
        4.  Leave all other settings as defaults.
   2.  Click *Save & view folder*
2.  Install the CheckMk agent
    1.  *On the CheckMk server,* Click to *Setup > Agents > Linux* to verify the Packaged Agent version to download
    2.  *On the host to be monitored,* Run the following commands with the latest Packaged Agent version:  
    ``` bash
    wget https://beholder.blkcat.space/blackcat_prod/check_mk/agents/check-mk-agent_2.2.0p23-1_all.deb
    sudo dpkg -i check-mk-agent_2.2.0p23-1_all.deb
    ```
    3. You'll see that the agent is running in Insecure Mode. We'll fix that in the next step.
3.  Register the CheckMk agent
    1.  *On the host to be monitored,* Run the following command, replacing `--hostname CHANGEME` with the hostname you set in the *Add host* step above.
    ``` bash
    cmk-agent-ctl register --hostname CHANGEME --server beholder.blkcat.space --site blackcat_prod --user register
    ```
4. Confirm
