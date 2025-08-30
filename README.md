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

<img width="1904" height="1074" alt="image" src="https://github.com/user-attachments/assets/04021d77-b47d-405c-abcf-a3d781f2e6f9" />



# INURL
<img width="1919" height="1088" alt="image" src="https://github.com/user-attachments/assets/a1d7ae16-67af-47e6-af85-c46edc42e394" />

# INTITLE
<img width="688" height="772" alt="intitle ex3" src="https://github.com/user-attachments/assets/bc95ab33-88c7-4f08-b3af-0fc34ed2acf8" />

# FILETYPE
<img width="687" height="762" alt="Screenshot 2025-08-25 203146" src="https://github.com/user-attachments/assets/78c104a4-f091-4a54-9654-7c8ecf4aa03e" />

# INTEXT
<img width="682" height="767" alt="intext ex 3" src="https://github.com/user-attachments/assets/63adadc2-1f1c-4fc4-85e9-e5b5d0c80b0a" />

# LINK
<img width="687" height="765" alt="link ex3" src="https://github.com/user-attachments/assets/bb0cd924-f604-4b09-af6b-9f53a1caf352" />

# CACHE
<img width="682" height="763" alt="cache ex3" src="https://github.com/user-attachments/assets/8e9222c7-7e63-433d-8da8-6f2e5259a1f3" />

# EXT
<img width="686" height="768" alt="ext ex3" src="https://github.com/user-attachments/assets/9b786d95-9d14-4015-8ccb-a72d6115c004" />

# DNS Enumeration
<img width="637" height="910" alt="Screenshot 2025-08-25 201434" src="https://github.com/user-attachments/assets/ec94ccaf-8750-457c-96ff-549001e88456" />

## DNS Recon
<img width="641" height="538" alt="Screenshot 2025-08-25 201550" src="https://github.com/user-attachments/assets/652769c5-bb4e-45bb-8f7e-e44ddba323be" />

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
<img width="703" height="821" alt="NS lookup exp 3" src="https://github.com/user-attachments/assets/8a318853-1550-47f5-9346-58debc54f552" />

# DIG
<img width="644" height="634" alt="Screenshot 2025-08-25 201643" src="https://github.com/user-attachments/assets/6e031a87-8aa2-4663-91ad-512ecff7f3bb" />

# HOST
<img width="639" height="448" alt="Screenshot 2025-08-25 201729" src="https://github.com/user-attachments/assets/17703ab1-2e29-4441-a98b-9e6a88332dc4" />

# DNSSENUM
<img width="641" height="745" alt="Screenshot 2025-08-25 201827" src="https://github.com/user-attachments/assets/3c799a74-4d6a-40f0-b861-9468f98cd2a5" />

# DNSRECON
<img width="639" height="834" alt="Screenshot 2025-08-25 201953" src="https://github.com/user-attachments/assets/c296e331-a2dc-437d-a097-55599e4fd3f6" />

# FIERCE
<img width="763" height="996" alt="fierce exp 3" src="https://github.com/user-attachments/assets/683ca218-93f0-49d8-9bfa-169d06cf2226" />

# HARVESTER
<img width="723" height="725" alt="Harvester exp 3" src="https://github.com/user-attachments/assets/be204124-6c7b-4dc7-a434-4d6c71cbccf9" />

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
<img width="658" height="471" alt="Screenshot 2025-08-25 204202" src="https://github.com/user-attachments/assets/7b5ee759-3c92-4ec1-a3fc-7e52ccb99aa4" />




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
