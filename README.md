# Enumeration
Enumeration Techniques

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

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:
![WhatsApp Image 2025-04-23 at 20 49 34_d0e2950b](https://github.com/user-attachments/assets/b9ac1984-9f37-4e14-ba9c-254383c05e3b)

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
![WhatsApp Image 2025-04-23 at 20 49 54_3b0cc68e](https://github.com/user-attachments/assets/5e98c9f8-defe-4684-b44d-71ddd9d83f7a)

Following searches for all the sites that is in the domain yahoo.com
![WhatsApp Image 2025-04-23 at 20 50 05_a72d11ee](https://github.com/user-attachments/assets/45d5f5bd-ed10-439c-8407-7967608c1e6f)

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
![WhatsApp Image 2025-04-23 at 20 51 44_c9e19cdd](https://github.com/user-attachments/assets/d3cf5572-7c94-41a4-a8aa-32fac9803d51)

Following searches for pdf file in the domain yahoo.com
![WhatsApp Image 2025-04-23 at 20 52 05_27067e88](https://github.com/user-attachments/assets/fc654134-2836-404f-ae1d-85bbe80a47f5)



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
![WhatsApp Image 2025-04-23 at 20 52 19_f546c461](https://github.com/user-attachments/assets/b218a05a-a74e-4472-ad83-c70614a6ca0a)



inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![WhatsApp Image 2025-04-23 at 20 52 32_9d5c1e68](https://github.com/user-attachments/assets/5c06469a-b36f-4dd3-b5c5-5bf493a7e707)

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:

![WhatsApp Image 2025-04-23 at 20 52 50_4db79a4f](https://github.com/user-attachments/assets/2008fae3-9970-4147-a178-0458383be56a)


![WhatsApp Image 2025-04-23 at 20 53 01_9a6ecca0](https://github.com/user-attachments/assets/d6846378-404b-465f-a98f-51fb9a4073cd)




##dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
![WhatsApp Image 2025-04-23 at 20 53 27_b196b4e0](https://github.com/user-attachments/assets/29e02f9d-e3a4-4a19-b66f-0d9b973a7272)


##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
![WhatsApp Image 2025-04-23 at 20 53 46_754152df](https://github.com/user-attachments/assets/c29e8050-4b69-40d5-a917-3a0f3c987f55)


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same
![WhatsApp Image 2025-04-23 at 20 54 11_c303fd57](https://github.com/user-attachments/assets/e47dfb63-1987-4943-85f9-d957c80411d0)
![WhatsApp Image 2025-04-23 at 20 54 20_ed64c645](https://github.com/user-attachments/assets/459b805d-e2b4-4005-96bb-60ee2a3c7be8)


#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ##Output
  ![WhatsApp Image 2025-04-23 at 20 54 44_f882b703](https://github.com/user-attachments/assets/843573be-a955-491d-8e37-cf5960d6b429)

  

## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
![WhatsApp Image 2025-04-23 at 20 55 12_850c36ac](https://github.com/user-attachments/assets/732e2a3a-d3bd-48fe-b6c9-7fbdad545abc)



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

