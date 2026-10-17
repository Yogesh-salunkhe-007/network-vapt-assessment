# Network VAPT Assessment Report

# 1. Executive Summary

A network reconnaissance and service-enumeration
assessment was performed against an authorized
training target.

The host was reachable, and six open TCP ports were
identified. The exposed services included FTP, SSH,
Samba, Squid HTTP proxy, and Apache HTTP server.

The collected Nmap output identifies accessible
services but does not independently confirm any
security vulnerability.

# 2. Scope

- Target: 10.48.144.123
- Assessment type: Network reconnaissance and service enumeration
- Operating environment: Kali Linux
- Scanner: Nmap 7.99
- Authorization: Authorized training lab only
- Restrictions: No testing outside the assigne scope

# 3. Methodology

1. Host discovery using Nmap.
2. TCP port scanning.
3. Service and version detection.
4. Review of saved Nmap output.
5. Documentation of observations and recommendations.

# 4. Results


ItemResultTaget Ip 10.48.144.123Host status               UpOpen TCP ports            6Closed TCP ports          994Identified services       FTP, SSH, Samba, Squid, ApacheConfirmed vulnerabilities0 confirmed by this scan       
# Service Inventory

PortPortPortServiceServiceServiceDetected versionDetected versionDetected version212121FTPFTPFTPvsftpd 3.0.5vsftpd 3.0.5vsftpd 3.0.5222222
# 5. Findings

# Observation 1: Multiple Network Services Exposed

- Severity: Informational
- Affected host: 10.48.144.123
- Affected ports: 21, 22, 139, 445, 3128, 3333

Evidence from Nmap shows that six TCP ports were open
and that service identification was successful.

Potential impact depends on the configuration,
accessibility, and security of each service.

Recommendations:
- Disable unnecessary services.
- Restrict access using firewall rules.
- Review FTP and SMB access controls.
- Ensure the HTTP proxy is restricted to authorized users.
- Review software support and security updates.

This observation is not proof that the host is vulnerable.

# 6. Limitations

The assessment used host discovery and service-version
detection. It did not establish whether the detected
services were exploitable.

No confirmed vulnerability should be inferred solely
from a port being open or a version string being reported.

The assessment is limited to the stated target and
the evidence collected during the recorded scans.

# 7. Remediation

1. Confirm the business need for each exposed service.
2. Restrict network access to required sources.
3. Review authentication and authorization settings.
4. Verify installed software versions on the target.
5. Check vendor security advisories before concluding
   that a vulnerability exists.
6. Retest any verified issue after remediation.

# 8. Conclusion

The assessment identified six open TCP ports on the
target. The results provide an initial service inventory
for further authorized security testing.

Additional validation is required to determine whether
any configuration weaknesses or known vulnerabilities
are present.




# 9. Evidence

- Recon/host-discovery.txt
- Evidence/service-scan.txt
- Evidence/network-assesment.nmap
- Evidence/network-assesment.gnmap
- Evidence/network-assesment.xml
- Findings/findings.md

