# Open.mp Startup Scripts (1.0.0)
Startup scripts for the Open.mp GTA server software - uses the "screen" command to manage a session. This also restarts the Open.mp process if it crashes.

---

These start up the Open.mp server at boot time with a "screen" process.

1. Copy **openmp** into **/home/openmpowner/bin** - make sure it is executable
2. Copy **startomp** into **/home/openmpowner/Open.mp** - make sure it is executable
3. Put **@reboot /home/openmpowner/bin/openmp start** into your crontab

When you want to view the Open.mp console, just enter "**screen -r**" in your shell.

To disconnect from the Open.mp console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /home/openmpowner/Open.mp/nostart**". To reenable it type "**rm /home/openmpowner/Open.mp/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
