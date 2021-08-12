# OpenNDS

OpenNDS is a high performance, small footprint Captive Portal,
offering by default a simple splash page restricted Internet connection
yet incorporates an API that allows the creation of sophisticated
authentication applications.

# Installing

After installing the snap you can adjust the configuration file in 
/var/snap/opennds/common/opennds/opennds.conf following
the documentation at https://openndsdocs.readthedocs.io/en/stable/

Then you need to allow the snap access to the firewall, network configuration,
mount information and some system and hardware resources with the commands

    sudo snap connect opennds:firewall-control
    sudo snap connect opennds:hardware-observe
    sudo snap connect opennds:mount-observe
    sudo snap connect opennds:network-control
    sudo snap connect opennds:system-observe

After connecting these snap interfaces, the opennds daemon will start
automatically. To interact with the daemon the snap package ships
the ```opennds.ndsctl``` command

# Building

You can just build this snap by calling ```snapcraft``` in the toplevel
of this source tree

