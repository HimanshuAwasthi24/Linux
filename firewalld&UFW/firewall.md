# Firewalld
```bash
rpm -qa | grep firewalld // Check for firewalld in RPM
dpkg -l | grep ufw // fur debian
```
*Note:* Manage process using `systemctl start/restart/stop/status/enabled firewalld.service or ufw` <br>

*Imp:* **Firewall Zones, Adding & removing a service from firewall permanent temporary, Blocking incoming & outgoing traffic by applying rich rules , Blocking ICMP incoming trafic** 