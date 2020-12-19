# luci-proto-modemmanager

For OpenWrt 19.xx and aboe only. Users of newer OpenWrt/LuCI versions should use the upstream version. This luci-protocol adds support to set up and configure basic options for a modem using ModemManager and LuCI on OpenWrt. Requires ModemManager. Assumes a modem is installed and working.
Features

    Automatically detects the modem
    Offers several APN's to choose from, users can add more
    Works with the default OpenWrt BusyBox configuration

Requirements

    ModemManager installed and running
    grep (included in BusyBox by default)
    tr (included in BusyBox by default)

Install

    Edit your feeds.conf and add the configuration of the new feed:

    $ vim feeds.conf
        src-git luci_proto_modemmanager https://github.com/rickydee/luci-proto-modemmanager.git

    Update the feed:

    $ ./scripts/feeds update luci_proto_modemmanager

    Install all packages from the feed:

    $ ./scripts/feeds install -p luci_proto_modemmanager -a

    enable in menuconfig
