# SSH Brute Force Detection Lab (Linux)

## Objective
Simulate failed SSH login attempts on a local Linux environment and analyze authentication logs to detect brute-force activity.

## Environment
- Kali Linux (local VM)
- OpenSSH Server
- Systemd journal logs

## Tools Used
- journalctl
- grep
- SSH client

## Methodology

1. Started SSH service on local machine
2. Created test user account
3. Generated multiple failed login attempts via SSH
4. Collected authentication logs using journalctl
5. Analyzed failed login patterns

## Key Commands Used
- sudo systemctl status ssh
- ssh testuser@localhost
- sudo journalctl -u ssh
- sudo journalctl | grep "Failed"

## Findings
- Multiple authentication failures detected
- Logs captured timestamps and username attempts
- System successfully recorded brute-force behavior indicators

## SOC Relevance
This type of log analysis is commonly used in Security Operations Centers (SOC) to detect unauthorized access attempts.

## Skills Demonstrated
- Linux log analysis
- SSH authentication monitoring
- Threat detection basics
- SOC investigation workflow
