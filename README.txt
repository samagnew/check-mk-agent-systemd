Installation Instructions
-------------------------
1. Put check_mk_agent and waitmax into location /usr/local/bin/ on host
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
