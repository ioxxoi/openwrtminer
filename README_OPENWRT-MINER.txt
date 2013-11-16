##############################################################################
#                                                                            #
#    OpenWrtMiner:  Bitcoin Miner based in OpenWrt capable AP and Routers    #
#                        V 0.1.0 - 2013 / 11 / 16                            #
#                                                                            #
##############################################################################
#                                                                            #
#    Copyright 2013 Daniel San Miguel IoXoI < ioxoi /a/ downby /·/ net >     #
#                                                                            #
#    This file is part of OpenWrtMiner.                                      #
#                                                                            #
#    OpenWrtMiner is free software: you can redistribute it and/or modify it #
#    under the terms of the GNU General Public License as published by the   #
#    Free Software Foundation, either version 3 of the License, or (at your  #
#    option) any later version.                                              #
#                                                                            #
#    OpenWrtMiner is distributed in the hope that it will be useful, but     #
#    WITHOUT ANY WARRANTY; without even the implied warranty of              #
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU        #
#    General Public License for more details.                                #
#                                                                            #
#    You should have received a copy of the GNU General Public License along #
#    with OpenWrtMiner. If not, see http://www.gnu.org/licenses/.            #
#                                                                            #
#                                                                            #
##############################################################################

This is a Solution Hand Made to convert yout OpenWrt Capable Router or
Access Point in a Bitcoin Miner controlling one or more ASIC Miners.
This project is not part of OpenWrt Project, only are a extension of OpenWrt
based system.

Actually are supported  BFL Miners:

 - Jalapenos      4.5 and  5 Gh/s
 - Little Singles 30  and 25 Gh/s
 - Singles        60  and 50 Gh/s

But other mining hardware probabily work but is untested, please notify me at
ioxoi /a/ downby /·/ net if you test with or without success any other Mining
Hardware supported by  bfgminer

This solution add the next functionality:

 - Auto startup and restart without user intervention (electricity power fail) 
   Or reboot by remote hands
 - Web status interface with mining stats updated in real time
 - Auto-check of the system based on GHh/s in last 5 sec, to restart the
   applications or system in case of fail or any component.
 - Hardware configured by OpenWrt web admin interface.
 - Flash based mining controller with low power consuming, no mobile hardware
   and ready to stop and restart without file system corruption.


FILES
------
WARNING: If you untar the .tgz file in / you overwrite your root crontab, 
if you make a previous change make a previous backup of /etc/crontabs/root

/www/miner.php              #Bfgminer web interface
/etc/bfgminer.cfg           #configuration of bfgminer
/etc/crontabs/root          #root crontab to check status of mining
/etc/init.d/bfgminer     
/usr/local/bin/bfgminer.cron
