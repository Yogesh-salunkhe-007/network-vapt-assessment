# Findings

# Finding 1: Multiple Network Services Exposed

- Severity: Informational (observation, not a confirmed vulnerability)
- Affected host: 10.48.144.123
- Affected ports: 21, 22, 139, 445, 3128, 3333
- Assessment tool: Nmap 7.99

# Evidence

Nmap identified the following open TCP ports:

- 21/tcp: vsftpd 3.0.5
- 22/tcp: OpenSSH 8.2p1 Ubuntu 4ubuntu0.13
- 139/tcp: Samba smbd 4
- 445/tcp: Samba smbd 4
- 3128/tcp: Squid HTTP proxy 4.10
- 3333/tcp: Apache httpd 2.4.41 (Ubuntu)

The host was reported as up. The scan found
994 closed TCP ports in the default scan range.

# Risk

Exposed services increase the system's attack surface.
The actual risk depends on the intended use of each
service, network restrictions, configuration, and
whether exploitable vulnerabilities are present.

This scan alone does not establish that any service
is vulnerable or improperly configured.

# Recommendation

- Confirm that each service is required.
- Restrict access to administrative and file-sharing
  services to authorized systems.
- Review FTP authentication and whether encrypted
  file transfer is required.
- Review Samba permissions and access controls.
- Ensure the proxy cannot be abused by unauthorized users.
- Verify software support status and apply appropriate
  security updates after checking the installed packages.

# Validation

Host discovery and Nmap service-version detection
were completed.

Authentication, access controls, proxy restrictions,
software vulnerability status, and exploitability have
not been verified by the evidence collected so far.
