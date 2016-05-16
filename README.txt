Installation Instructions
-------------------------
1a.
	A. Download the linux check-mk-agent from http://mathias-kettner.com/check_mk_download.php
	   (you have to download the whole check_mk package and then find the
	   agent files in a subdirectory)
	B. Put check_mk_agent and waitmax files into location /usr/local/bin/ on host
		-- OR --
1b. 
	A. Install package "check-mk-agent" using e.g. yum
	B. Edit the included "check_mk_agent@.service" and 
	   "check_mk_agent.socket" files so the paths to 
	   "check_mk_agent" and "waitmax" begin with "/usr/bin" instead of
	   "/usr/local/bin"

2. Put check_mk_agent@.service and check_mk_agent.socket into location /etc/systemd/system/ on host
3. There is no step three!

Activation Instructions
-----------------------
# systemctl enable check_mk_agent.socket ; systemctl start check_mk_agent.socket ; systemctl status check_mk_agent.socket

Test Instructions
-----------------
(From another host that can reach the host you are installing on)
# telnet <yourhost> 6556

Expected response: check_mk data regarding the host should echo to the terminal
