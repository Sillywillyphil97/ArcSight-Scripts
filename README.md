# ArcSight Scripts
Useful scripts for dealing with Micro Focus' ArcSight products.
## SmartConnectors
* container_restart.ps1 -> Used with connector frameworks installed on windows host. 
* sclb_stop_start.sh -> Used to quicky stop and start the ArcSight Loadbalancing SmartConnector.
* thub_cert_store_builder.sh -> Used to quickly stand up a single cert store for connector destinations to use when sending to Transformation Hub over SSL
* nonappliance_sc_stop_start.sh -> Refer to the script below, exact same script without the interaction with the monit service. 
* appliance_sc_stop_start.sh -> Used to quickly stop and start a ArcSight SmartConnector Container on a ArcMC Appliance.

    ```bash
    $ ./container_restart_menu.sh 

    1- Container_1
    2- Container_2
    3- Container_3
    4- Container_4
    5- Container_5
    6- Container_6
    7- Container_7
    8- Container_8
    9- Exit
    Enter the number: 
    ```

## ArcMC
* update_marketplace_cert.sh -> Grabs latest marketplace cert for parser AUP downloading.

```bash
$./update_marketplace_cert.sh
```

## ADP Cluster
* node-restart-remote.sh -> Used with ArcSight ADP Cluster ver. 2021
    * drain.sh -> mating script to node-restart-remote.sh and goes locally on each node in /root/

    ```bash
    $ ./node-reboot-remote.sh
    ```
    
 * node-restart-local.sh -> What I was using before coming up with the remote version of this script. Must be ran on each node indidually and includes no checks.

    ```bash
    $ ./node-restart-local.sh
    ```
    

* node-cmd-sender.sh -> Used to send the same linux command to each node in the cluster.
    ```bash
    $ ./node-cmd-sender.sh ls

    node1:
    file1
    file2
    file3
    CMD:'ls' completed successfully on node1

    node2:
    file1
    file2
    file3
    CMD:'ls' completed successfully on node2
    ```
## Other
* cef_syslog_sender.py - Basic script to send test events to a syslogNG connector.
