**DHCP traffic**
```
dhcp
```
```
bootp
```
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcp.PNG)
**Host name**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcphostname.PNG)
**Victim IP**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcpip.PNG)



```
nbns
```
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/nbns.PNG)

**SMB2 traffic from victim**
```
smb2 && ip.addr == 10.8.15.133
```
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2search.PNG)
**SMB2 session showing account name plucero**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2accountname.PNG)
**SMB2 session showing full name Pierce Lucero**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2fullname.PNG)

**Doman Name System**
```
dns
```
```
dns.qry.name contains "checkfedexexp"
```
**DNS query for quote.checkfedexexp.com**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dns1.PNG)
**DNS query for business.checkfedexexp.com**
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dns2.PNG)

**HTTP GET — ZIP lure download from quote.checkfedexexp.com**
```
http && ip.addr == 104.21.55.70
```

![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpzip.PNG)
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpstream1.PNG)

**HTTP BITS request — DLL payload from 72.5.43.29**
```
http && ip.addr == 72.5.43.29
```
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpdll.PNG)
![image](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpstream2.PNG)
