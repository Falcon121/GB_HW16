Step 1: Google Dorking
Altoro Mutual wants to ensure that private information that is unavailable on their public website cannot be found by searching the web.


For example, Altoro Mutual does not mention their executive remembers on the website. Using Google, can you identify who the Chief Executive Officer?
Answer: Karl Fitzgerald 

How can this information be helpful to an attacker?
Answer: You can find out who is in chain of command and who to gather information from.


Step 2: DNS and Domain Discovery
The reconnaissance phase of a penetration test is possibly the most important phase of the engagement. Without a clear understanding of your client's assets, vulnerabilities can go unnoticed and later exploited.


Navigate to centralops.net.


Enter the IP address for demo.testfire.net into Domain Dossier and answer the following questions based on the results:


Where is the company located?
Answer: Sunnyvale, CA 

What is the NetRange IP address?
Answeer: 65.61.137.64 - 65.61.137.127

What is the company they use to store their infrastructure?
Answer: AKAM.NET

What is the IP address of the DNS server?
Answer: 65.61.137.117




Step 3: Shodan
Using Shodan and the information gathered from Google Dorking, find any other useful information that can be used in an attack.


Navigate to shodan.io.


Run a scan against the IP address of the DNS server for demo.testfire.net.

What open ports and running services did Shodan find?
Answer: 80 and 443 are open. Apache services are running. 
		



Step 4: Recon-ng
Altoro Mutual is also concerned about cross-site scripting attacks, which can cause havoc on their website. Verify whether or not Altoro Mutual is vulnerable to XSS by completing the following:

Install the Recon module xssed.
Set the source to demo.testfire.net.
Run the module.

Is Altoro Mutual vulnerable to XSS?
Answer: Yes 
Step 5: Zenmap
Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:


Use Zenmap to run a service scan against the Metasploitable machine.


Bonus: In the same command, output the results into a new text file named zenmapscan.txt.
Bonus Answer: nmap -oN/root/zenmapscan.txt 192.168.0.10
Answer 1: SMB Listens on port
Answer 2: Malicious actors may use these ports to perform NetBIOS attacks.
Answer 3: Disable the ports with firewall settings
