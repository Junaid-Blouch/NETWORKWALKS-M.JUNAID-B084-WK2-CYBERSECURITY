# PM1 — Footprinting & Reconnaissance with Multiple Kali Tools

**Target:** networkwalks.com (authorized)
**Tools used:** whois, whatweb, nslookup, curl, wafw00f, dnsrecon

---

## Task 1: WHOIS Lookup

**Command:**
whois networkwalks.com
**Screenshot:**
👉 **<img width="1920" height="891" alt="Whois result SS" src="https://github.com/user-attachments/assets/c6bbbc35-e3f9-42bb-8d76-3a7cf01e9473" />
**

**Output:**
[Whois results.txt](https://github.com/user-attachments/files/34815512/Whois.results.txt)

──(junaid㉿junaidbloch)-[~]
└─$ whois networkwalks.com
   Domain Name: NETWORKWALKS.COM
   Registry Domain ID: 2452319255_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.godaddy.com
   Registrar URL: http://www.godaddy.com
   Updated Date: 2025-11-12T10:08:43Z
   Creation Date: 2019-11-06T22:51:46Z
   Registry Expiry Date: 2027-11-06T22:51:46Z
   Registrar: GoDaddy.com, LLC
   Registrar IANA ID: 146
   Registrar Abuse Contact Email: abuse@godaddy.com
   Registrar Abuse Contact Phone: 480-624-2505
   Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
   Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
   Name Server: NS6135.HOSTGATOR.COM
   Name Server: NS6136.HOSTGATOR.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-11-12T15:30:33Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

NOTICE: The expiration date displayed in this record is the date the
registrar's sponsorship of the domain name registration in the registry is
currently set to expire. This date does not necessarily reflect the expiration
date of the domain name registrant's agreement with the sponsoring
registrar.  Users may consult the sponsoring registrar's Whois database to
view the registrar's reported date of expiration for this registration.

TERMS OF USE: You are not authorized to access or query our Whois
database through the use of electronic processes that are high-volume and
automated except as reasonably necessary to register domain names or
modify existing registrations; the Data in VeriSign Global Registry
Services' ("VeriSign") Whois database is provided by VeriSign for
information purposes only, and to assist persons in obtaining information
about or related to a domain name registration record. VeriSign does not
guarantee its accuracy. By submitting a Whois query, you agree to abide
by the following terms of use: You agree that you may use this Data only
for lawful purposes and that under no circumstances will you use this Data
to: (1) allow, enable, or otherwise support the transmission of mass
unsolicited, commercial advertising or solicitations via e-mail, telephone,
or facsimile; or (2) enable high volume, automated, electronic processes
that apply to VeriSign (or its computer systems). The compilation,
repackaging, dissemination or other use of this Data is expressly
prohibited without the prior written consent of VeriSign. You agree not to
use electronic processes that are automated and high-volume to access or
query the Whois database except as reasonably necessary to register
domain names or modify existing registrations. VeriSign reserves the right
to restrict your access to the Whois database in its sole discretion to ensure
operational stability.  VeriSign may restrict or terminate your access to the
Whois database for failure to abide by these terms of use. VeriSign
reserves the right to modify these terms at any time.

The Registry database contains ONLY .COM, .NET, .EDU domains and
Registrars.
Domain Name: networkwalks.com
Registry Domain ID: 2452319255_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.godaddy.com
Registrar URL: https://www.godaddy.com
Updated Date: 2025-11-12T05:08:41Z
Creation Date: 2019-11-06T17:51:46Z
Registrar Registration Expiration Date: 2027-11-06T17:51:46Z
Registrar: GoDaddy.com, LLC
Registrar IANA ID: 146
Registrar Abuse Contact Email: abuse@godaddy.com
Registrar Abuse Contact Phone: +1.4806242505
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
Domain Status: clientRenewProhibited https://icann.org/epp#clientRenewProhibited
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Registry Registrant ID: Not Available From Registry
Registrant Name: Registration Private
Registrant Organization: Domains By Proxy, LLC
Registrant Street: DomainsByProxy.com
Registrant Street: 100 S. Mill Ave, Suite 1600
Registrant City: Tempe
Registrant State/Province: Arizona
Registrant Postal Code: 85281
Registrant Country: US
Registrant Phone: +1.4806242599
Registrant Phone Ext:
Registrant Fax: 
Registrant Fax Ext:
Registrant Email: https://www.godaddy.com/whois/results.aspx?domain=networkwalks.com&action=contactDomainOwner
Registry Tech ID: Not Available From Registry
Tech Name: Registration Private
Tech Organization: Domains By Proxy, LLC
Tech Street: DomainsByProxy.com
Tech Street: 100 S. Mill Ave, Suite 1600
Tech City: Tempe
Tech State/Province: Arizona
Tech Postal Code: 85281
Tech Country: US
Tech Phone: +1.4806242599
Tech Phone Ext:
Tech Fax: 
Tech Fax Ext:
Tech Email: https://www.godaddy.com/whois/results.aspx?domain=networkwalks.com&action=contactDomainOwner
Name Server: NS6135.HOSTGATOR.COM
Name Server: NS6136.HOSTGATOR.COM
Name Server: NS29.DOMAINCONTROL.COM
Name Server: NS30.DOMAINCONTROL.COM
DNSSEC: unsigned
URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
>>> Last update of WHOIS database: 2026-11-12T15:30:51Z <<<
For more information on Whois status codes, please visit https://icann.org/epp

TERMS OF USE: The data contained in this registrar's Whois database, while believed by the
registrar to be reliable, is provided "as is" with no guarantee or warranties regarding its
accuracy. This information is provided for the sole purpose of assisting you in obtaining
information about domain name registration records. Any use of this data for any other purpose
is expressly forbidden without the prior written permission of this registrar. By submitting
an inquiry, you agree to these terms and limitations of warranty. In particular, you agree not
to use this data to allow, enable, or otherwise support the dissemination or collection of this
data, in part or in its entirety, for any purpose, such as transmission by e-mail, telephone,
postal mail, facsimile or other means of mass unsolicited, commercial advertising or solicitations
of any kind, including spam. You further agree not to use this data to enable high volume, automated
or robotic electronic processes designed to collect or compile this data for any purpose, including
mining this data for your own personal or commercial purposes. Failure to comply with these terms
may result in termination of access to the Whois database. These terms may be subject to modification
at any time without notice.

**NOTICE** This WHOIS server is being retired. Please use our RDAP service instead.

                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ 

---

## Task 2: WhatWeb Fingerprinting

**Command:**
whatweb networkwalks.com
**Screenshot:**
👉 **<img width="1427" height="593" alt="whatweb result SS" src="https://github.com/user-attachments/assets/23109722-eb03-440c-8509-f0a950853745" />
**

**Output:**
[whatweb results.txt](https://github.com/user-attachments/files/34815571/whatweb.results.txt)
──(junaid㉿junaidbloch)-[~]
└─$ whatweb networkwalks.com
http://networkwalks.com [301 Moved Permanently] Apache, Cookies[__wpdm_client], Country[UNITED STATES][US], HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], RedirectLocation[https://networkwalks.com/], UncommonHeaders[permissions-policy,x-redirect-by,referrer-policy,x-endurance-cache-level,x-nginx-cache]
https://networkwalks.com [200 OK] Apache, Bootstrap[7.1.4], Cookies[__wpdm_client], Country[UNITED STATES][US], Email[info@networkwalks.com], Frame, Google-Tag-Manager, HTML5, HTTPServer[Apache], HttpOnly[__wpdm_client], IP[192.232.216.135], JQuery[3.7.1], MetaGenerator[WordPress 7.1.4,WordPress Download Manager 3.3.76], Open-Graph-Protocol[website], Script[4684NR-IPIB&amp;pidnVar2=50511&amp;prtVar2=7&amp;scvVar2=12,application/json,application/ld+json,module,speculationrules,text/javascript], Title[Networkwalks Academy], UncommonHeaders[permissions-policy,link,referrer-policy,x-endurance-cache-level,x-nginx-cache], WordPress[7.1.4]
https://networkwalks.com/ [200 OK] Apache, Bootstrap[7.1.4], Country[UNITED STATES][US], Email[info@networkwalks.com], Frame, Google-Tag-Manager, HTML5, HTTPServer[Apache], IP[192.232.216.135], JQuery[3.7.1], MetaGenerator[WordPress 7.1.4,WordPress Download Manager 3.3.76], Open-Graph-Protocol[website], Script[4684NR-IPIB&amp;pidnVar2=50511&amp;prtVar2=7&amp;scvVar2=12,application/json,application/ld+json,module,speculationrules,text/javascript], Title[Networkwalks Academy], UncommonHeaders[permissions-policy,link,referrer-policy,x-endurance-cache-level,x-nginx-cache], WordPress[7.1.4]
                                                                                                                                                      
┌──(junaid㉿junaidbloch)-[~]
└─$ 

---

## Task 3: Nslookup — DNS Resolution

**Command:**
nslookup networkwalks.com
**Screenshot:**
👉 **<img width="659" height="434" alt="nslookup result SS" src="https://github.com/user-attachments/assets/d0d49c45-e8a9-4403-bd52-ce19ac27d1ee" />
**

**Output:**
[nslookup results.txt](https://github.com/user-attachments/files/34815814/nslookup.results.txt)──(junaid㉿junaidbloch)-[~]
└─$ nslookup networkwalks.com
Server:		8.8.8.8
Address:	8.8.8.8#53

Non-authoritative answer:
Name:	networkwalks.com
Address: 192.232.216.135

                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ 

---

## Task 4: Curl — HTTP Response Headers

**Command:**
curl -I https://networkwalks.com

**Screenshot:**
👉 **<img width="659" height="434" alt="curl -I result SS" src="https://github.com/user-attachments/assets/17d67ddd-f873-49fb-afa0-c8d47c865e89" />
**

**Output:**
[curl -I results.txt](https://github.com/user-attachments/files/34815683/curl.-I.results.txt)

──(junaid㉿junaidbloch)-[~]
└─$ curl -I networkwalks.com         
HTTP/1.1 301 Moved Permanently
Date: Thu, 12 Nov 2026 16:01:30 GMT
Server: Apache
Permissions-Policy: private-state-token-redemption=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com"), private-state-token-issuance=(self "https://www.google.com" "https://www.gstatic.com" "https://recaptcha.net" "https://challenges.cloudflare.com" "https://hcaptcha.com")
Expires: Thu, 12 Nov 2026 17:01:31 GMT
Cache-Control: max-age=3600
X-Redirect-By: WordPress - Really Simple Security
Set-Cookie: __wpdm_client=37ea100203b6c774f8c5e5f4f1324d7d; path=/; domain=networkwalks.com; HttpOnly
Location: https://networkwalks.com/
Referrer-Policy: no-referrer-when-downgrade
X-Endurance-Cache-Level: 0
X-nginx-cache: WordPress
Content-Type: text/html; charset=UTF-8

                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ 

---

## Task 5: Wafw00f — WAF Detection

**Command:**
wafw00f networkwalks.com

**Screenshot:**
👉 **<img width="664" height="374" alt="wafw00f result SS" src="https://github.com/user-attachments/assets/f68dbb85-c212-4eab-b38a-df0f476afa22" />
**

**Output:**
[wafw00f results.txt](https://github.com/user-attachments/files/34815720/wafw00f.results.txt)

──(junaid㉿junaidbloch)-[~]
└─$ wafw00f networkwalks.com

                   ______
                  /      \
                 (  Woof! )
                  \  ____/                      )
                  ,,                           ) (_
             .-. -    _______                 ( |__|
            ()``; |==|_______)                .)|__|
            / ('        /|\                  (  |__|
        (  /  )        / | \                  . |__|
         \(_)_))      /  |  \                   |__|

                    ~ WAFW00F : v2.4.2 ~
    The Web Application Firewall Fingerprinting Toolkit
    
[*] Checking https://networkwalks.com
[+] The site https://networkwalks.com is behind ModSecurity (SpiderLabs) WAF.
[~] Number of requests: 2
                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ 

---

## Task 6: DNSRecon — DNS Enumeration

**Command:**
dnsrecon -d networkwalks.com

**Screenshot:**
👉 **<img width="1088" height="536" alt="dnsrecon -d result SS" src="https://github.com/user-attachments/assets/34528adb-b301-437f-a9c1-b984118a77fc" />
**

**Output:**
[dnsrecon -d results.txt](https://github.com/user-attachments/files/34815737/dnsrecon.-d.results.txt)


                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ dnsrecon -d networkwalks.com
2026-11-12T08:08:00.900271-0800 INFO Starting enumeration for domain: networkwalks.com
2026-11-12T08:08:00.902407-0800 INFO std: Performing General Enumeration against: networkwalks.com...
2026-11-12T08:08:01.689905-0800 ERROR No answer for DNSSEC query for networkwalks.com
2026-11-12T08:08:02.356232-0800 INFO 	 SOA ns6135.hostgator.com 50.87.144.87
2026-11-12T08:08:03.092207-0800 INFO 	 NS ns6135.hostgator.com 50.87.144.87
2026-11-12T08:08:03.673144-0800 INFO 	 Bind Version for 50.87.144.87 "9.16.23-RH"
2026-11-12T08:08:03.673958-0800 INFO 	 NS ns6136.hostgator.com 192.232.216.131
2026-11-12T08:08:04.254321-0800 INFO 	 Bind Version for 192.232.216.131 "9.16.23-RH"
2026-11-12T08:08:05.074785-0800 INFO 	 MX mail.networkwalks.com 192.232.216.135
2026-11-12T08:08:05.419647-0800 INFO 	 A networkwalks.com 192.232.216.135
2026-11-12T08:08:06.455571-0800 INFO 	 TXT networkwalks.com v=spf1 +a +mx +ip4:50.87.144.87 +include:websitewelcome.com ~all
2026-11-12T08:08:06.456608-0800 INFO 	 TXT networkwalks.com google-site-verification=rr04eRmqHoWY3XemnizDNVK4q75X-Ij-mjgEeg-UsYI
2026-11-12T08:08:07.314810-0800 INFO Enumerating SRV Records
2026-11-12T08:08:09.832900-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.9 443
2026-11-12T08:08:09.833147-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.14 443
2026-11-12T08:08:09.833299-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.15 443
2026-11-12T08:08:09.833530-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.11 443
2026-11-12T08:08:09.833590-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.14 443
2026-11-12T08:08:09.833645-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.11 443
2026-11-12T08:08:09.833685-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.204.9 443
2026-11-12T08:08:09.833797-0800 INFO 	 SRV _autodiscover._tcp.networkwalks.com cpanelemaildiscovery.cpanel.net 184.94.203.15 443
2026-11-12T08:08:12.291805-0800 INFO 8 Records Found
2026-11-12T08:08:12.292448-0800 INFO Completed enumeration for domain: networkwalks.com

                                                                                
┌──(junaid㉿junaidbloch)-[~]
└─$ 
