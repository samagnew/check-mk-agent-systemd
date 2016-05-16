# check-mk-agent-systemd
Service and Socket files for running the Check_MK agent under systemd

Note: The provided files will work with the "check_mk_agent" and "waitmax" files in "/usr/local/bin" as you might do on a RedHat-based Atomic host. If you have installed the check-mk-agent package via "yum" you will find these files are installed in "/usr/bin" instead. In this case you should alter the paths in the "socket" and "service" files.

See the README.txt file for installation instructions.
