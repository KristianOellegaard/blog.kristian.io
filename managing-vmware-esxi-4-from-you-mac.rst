Managing VMware ESXi 4 from you mac
###################################
:date: 2011-05-11 14:16
:category: Mac, System administration

.. raw:: html

   <p>

For my own reference, and maybe others i found this very usefull link:
`http://www.howconfig.com/linux/how-to-open-cli-to-vmware-esxi-how-to-clone-virtual-machines/`_
This will be a direct quote, in case the site will ever change:

    You can access the CLI by switching to terminal 1 using Alt-F1. Now
    type “unsupported”, This is not echoed so you won’t see anything. If
    you get it right, you will get a prompt asking for the root pasword.
    ( This might not work in ESXi 4.0 as VMWare is trying to limit ESXi
    for their own corporate reasons ) That drops you at a shell prompt.
    (ash is our shell). Hint: editor = vi Now you can you modify
    /etc/inetd.conf and uncomment the ssh line so that you can ssh into
    it unless you are planning always being at the console. Reboot (
    init 6 ) Cloning Virtual machines in ESXi vmkfs tools -i
    /vmfs/volumes/datastore/YourVM/YourVM.vmdk
    /vmfs/volumes/datastore/NewVM/newvm.vmdk vim-cmd vmsvc/getallvms
    vim-cmd vmsvc/power.reset xx check out these ( with vim-cmd
    vmsvc/command ): power.off power.on power.reboot power.reset
    power.shutdown power.suspend esxtop = is your top tool

My tips: Just ssh to your ESXi server e.g. ssh root@esxi and run the
above commands. It might tell you that its unsupported, unfortunately
there is no supported client to mac, so thats not really usefull
information anyway Use at your own risk.

.. raw:: html

   </p>

.. _`http://www.howconfig.com/linux/how-to-open-cli-to-vmware-esxi-how-to-clone-virtual-machines/`: http://www.howconfig.com/linux/how-to-open-cli-to-vmware-esxi-how-to-clone-virtual-machines/
