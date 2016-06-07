# temporary_test_scripts_4_sqm-scripts
This repository is the home for work-in-progesss scripts for sqm-scripts development; these scripts will only be useful to test specific issues and should not be taken for granted.

To manually add these scripts to an existing openwrt/LEDE install with installed and actice sqm-scripts:

## "Installing" the current development version from git

Run the steps below on your own computer (not on the router) to retrieve the newest script version from this repository, create the scripts, then copy those new scripts to your router.

1. Make a local clone of the git repository (if you have not already):

    `git clone https://github.com/moeller0/temporary_test_scripts_4_sqm-scripts`

2. Change into the new directory:

    `cd ./temporary_test_scripts_4_sqm-scripts`

3. Make sure the source is updated:

    `git pull`

4. Now, use scp to copy the new scripts to the router. Change `$YOUR.SQM.HOSTNAME` to the address/DNS name for your computer - probably `192.168.1.1` or on cerowrt `gw.hom.lan`. If your account on the router is not "root", change "root" to your account:

    `scp -r ./TESTING* root@$YOUR.SQM.HOSTNAME:/usr/lib/sqm`

Note this does not offer a method to uninstall the new scripts againg, so simply delete them manually or even simpler just don't select that as $SCRIPT in sqm-scripts and they will be happily ignored...
