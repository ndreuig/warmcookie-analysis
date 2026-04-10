# Wireshark Analysis — Screenshots

---

## 1. Victim Identification

### DHCP
> Filter: `dhcp` / `bootp`

![DHCP traffic](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcp.PNG)

| | |
|---|---|
| **Hostname** | ![hostname](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcphostname.PNG) |
| **Victim IP** | ![victim ip](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dhcpip.PNG) |

---

### NetBIOS Name Service (NBNS)
> Filter: `nbns`

![NBNS](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/nbns.PNG)

---

### SMB2
> Filter: `smb2 && ip.addr == 10.8.15.133`

![SMB2 traffic](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2search.PNG)

| | |
|---|---|
| **Account name** `plucero` | ![account name](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2accountname.PNG) |
| **Full name** Pierce Lucero | ![full name](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/smb2fullname.PNG) |

---

## 2. DNS Queries

> Filter: `dns` → `dns.qry.name contains "checkfedexexp"`

| Domain | Screenshot |
|---|---|
| `quote.checkfedexexp.com` | ![dns1](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dns1.PNG) |
| `business.checkfedexexp.com` | ![dns2](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dns2.PNG) |

---

## 3. Malware Delivery

### ZIP Lure — `quote.checkfedexexp.com`
> Filter: `http && ip.addr == 104.21.55.70`

![HTTP ZIP request](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpzip.PNG)
![HTTP ZIP stream](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpstream1.PNG)

---

### DLL Payload — `72.5.43.29` (via BITS)
> Filter: `http && ip.addr == 72.5.43.29`

![HTTP DLL request](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpdll.PNG)
![HTTP DLL stream](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/httpstream2.PNG)

---

## 4. Exported Objects

![Export objects list](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/exportobjects.PNG)

**ZIP file**
![ZIP object](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/zipobject.PNG)

**DLL file**
![DLL object](https://github.com/ndreuig/warmcookie-analysis/blob/main/screenshots/dllobject.PNG)
