# Network Protocol Analysis
The primary involved protocol in the incident is the hypertext transfer protcol, or HTTP. The issue was
related to accessing a web server, so we know that the requests involve HTTP traffic. tcpdump also showed the usage of http
protocols. Finally, the malicious file is shown to be transported to client devices using HTTP protocol.

# Documentation, general timeline
Clients and customers contacted IP help desk reporting that they were redirected to a new web server and prompted to download file,
which since has left their devices running much slower. Our analysis team then used a virtual machine to access
the website without impacting the company's network. tcpdump was ran to capture traffic packets. The analysts investigating
were prompted to download a file, which redirected the analyst to a fake website.

The analyst then reported the incident and traffic rerouting to the senior cybersec on duty, who analyzed source code 
for both the website and malicious file. It was then determined that the attacker changed the source code to prompt the user
to download a malicious file. The owner of the website also stated that they were locked out of the account, so the team is under the
assumption that the malicious agent changed the administrative password.

# Recommendations For Security
- Disallow previous passwords from being used
- Limit # of password attempts before being locked out
- MFA
- Frequent Pasword Updates
