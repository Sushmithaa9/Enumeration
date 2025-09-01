# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

| Operator    | Description                        | Example Usage           |
| ----------- | ---------------------------------- | ----------------------- |
| `site:`     | Search within a specific domain    | `site:example.com`      |
| `inurl:`    | Search in URL                      | `inurl:admin`           |
| `intitle:`  | Search in page title               | `intitle:"index of"`    |
| `filetype:` | Search by file type                | `filetype:pdf`          |
| `intext:`   | Search inside page text            | `intext:"confidential"` |
| `link:`     | Pages that link to a specific site | `link:example.com`      |
| `cache:`    | View cached version of a site      | `cache:example.com`     |
| `ext:`      | Same as filetype                   | `ext:xls`               |

 ## Architecture 
 ```
+----------------------+
|   Attacker / Hacker  |
|   (Browser & Google) |
+----------+-----------+
           |
           | Google Dork Queries
           v
+---------------------------+
|       Google Search       |
+---------------------------+
           |
           | Indexed Public Content
           v
+---------------------------+
|   Target Websites / Data  |
| - Leaked files            |
| - Open directories        |
| - Sensitive info          |
+---------------------------+

```

# Output:
# SITE:

<img width="1906" height="1120" alt="image" src="https://github.com/user-attachments/assets/3708a9cb-88fc-4ea2-9d6c-4cd61d0bdfcb" />



# INURL
<img width="1919" height="1130" alt="image" src="https://github.com/user-attachments/assets/9dd15e30-8ac6-4237-94a0-7d38c0b4aa64" />


# INTITLE
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/5e6922c3-b4f8-4aef-b9e7-cfefbf06f1e3" />



# FILETYPE
<img width="1875" height="980" alt="image" src="https://github.com/user-attachments/assets/d2f2f50a-fe15-4892-9a60-a6b5e9b0c0b8" />


# INTEXT
 <img width="1919" height="972" alt="image" src="https://github.com/user-attachments/assets/9390f464-6fa5-454f-907d-c5c887880101" />


# LINK
<img width="1919" height="1131" alt="image" src="https://github.com/user-attachments/assets/4dbfbe53-3259-46ea-a176-82fd98ae9d56" />


# CACHE
<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/1edaa46e-0eda-4cc8-bce9-8671782a6595" />


# EXT
<img width="1906" height="1134" alt="image" src="https://github.com/user-attachments/assets/9f9f80a4-bae4-45fb-beae-2c067b13f1ea" />

# DNS Enumeration
<img width="833" height="384" alt="image" src="https://github.com/user-attachments/assets/e0ecf916-f8da-46c7-8590-f352f4696d90" />

## DNS Recon
<img width="809" height="381" alt="image" src="https://github.com/user-attachments/assets/56554fe6-3944-4653-afe1-4545b66b69fd" />

| Record Type | Meaning                        | Example Output                   |
| ----------- | ------------------------------ | -------------------------------- |
| A           | Host to IPv4 address           | `example.com -> 93.184.216.34`   |
| AAAA        | Host to IPv6 address           | `example.com -> ::1`             |
| MX          | Mail server info               | `mail.example.com`               |
| NS          | Name servers                   | `ns1.example.com`                |
| TXT         | Misc data (SPF, verifications) | `v=spf1 include:_spf.google.com` |
| CNAME       | Canonical names (aliases)      | `www -> example.com`             |

## Common Tools Used (Kali Linux)

| Tool           | Description                                | Usage Example                           |
| -------------- | ------------------------------------------ | --------------------------------------- |
| `nslookup`     | DNS lookup tool (simple queries)           | `nslookup example.com`                  |
| `dig`          | DNS lookup utility (detailed)              | `dig example.com any`                   |
| `host`         | Simple DNS querying tool                   | `host example.com`                      |
| `dnsenum`      | Perl script to enumerate DNS info          | `dnsenum example.com`                   |
| `fierce`       | DNS scanner to locate non-contiguous IPs   | `fierce -dns example.com`               |
| `dnsrecon`     | Powerful DNS enumeration script            | `dnsrecon -d example.com -a`            |
| `theHarvester` | Subdomain enumeration using search engines | `theHarvester -d example.com -b google` |


## OUTPUT:
# NSLOOKUP
<img width="621" height="387" alt="image" src="https://github.com/user-attachments/assets/8c298b16-6f19-43a8-981a-5c86f50fe3bd" />


# DIG
<img width="632" height="346" alt="image" src="https://github.com/user-attachments/assets/9fc41d30-f761-45d6-825b-b0e32717716d" />

# HOST
<img width="679" height="381" alt="image" src="https://github.com/user-attachments/assets/12e87167-084a-41b9-906d-4d657e11ccd3" />

# DNSSENUM
<img width="846" height="386" alt="image" src="https://github.com/user-attachments/assets/21a5b99e-64bc-40d0-8fab-b028c399b583" />

# DNSRECON
<img width="648" height="348" alt="image" src="https://github.com/user-attachments/assets/4cda7ea6-e440-4771-87ce-0b63599df984" />

# FIERCE
<img width="864" height="226" alt="image" src="https://github.com/user-attachments/assets/c87099fc-ac34-497a-9c42-711dc9aefe1f" />

# HARVESTER
<img width="839" height="372" alt="image" src="https://github.com/user-attachments/assets/f948d370-7a14-4e54-8e01-b4a5e86f0050" />


## Architecture Diagram 
```
+-------------------+        +------------------+       +------------------+
|                   |        |                  |       |                  |
|   Attacker (You)  +------->|   Target Server   +<----->+    DNS Server    |
| Kali Linux / Parrot|       | (Mail / DNS Host) |       |  (Authoritative) |
+---------+---------+        +---------+--------+       +---------+--------+
          |                            ^                          ^
          |                            |                          |
          |                            |                          |
          |           +-----------------------------+            |
          |           |      Information Tools      |            |
          |           |-----------------------------|            |
          |           | smtp-user-enum              |            |
          |           | nmap --script smtp-enum-*   |            |
          |           | dnsenum                     |<-----------+
          |           +-----------------------------+
          |
          v
+-----------------------------+
|   Output/Report             |
|  - Usernames Found          |
|  - MX Records / Zones       |
|  - Subdomains / IPs         |
+-----------------------------+

```

## dnsenum
**Purpose:** A multithreaded Perl script to enumerate information from DNS servers.

**Use case:** Performs DNS zone transfers, brute force subdomains, and gather host IPs.

```
dnsenum example.com
```

## Output:
<img width="833" height="384" alt="image" src="https://github.com/user-attachments/assets/8e394786-96cb-44f9-9166-48fad22bc431" />




## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
<img width="680" height="370" alt="Screenshot 2025-08-25 202131" src="https://github.com/user-attachments/assets/e4c7471f-0524-4c3c-85f0-80ef250ebb1b" />



## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:
<img width="681" height="137" alt="Screenshot 2025-08-25 202159" src="https://github.com/user-attachments/assets/bc1327b9-914d-47f7-b4df-c5c81c96d293" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
