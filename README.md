# Kali Linux Firewall Configuration using UFW

## Project Description
Implementation of network security controls through firewall configuration on a Linux system. This project demonstrates practical application of host-based firewall management using UFW (Uncomplicated Firewall) to enforce secure network access policies.

## Technical Objectives
- Establish baseline firewall configuration
- Implement port-based access controls
- Verify rule effectiveness through testing
- Document security implementation

## System Configuration
- **Operating System**: Kali Linux (6.12.33+kali-amd64 kernel)
- **Security Tools**:
  - UFW v0.36.1
  - OpenSSH 8.9p1
  - Telnet


## Implementation Details
<img width="506" height="197" alt="Screenshot 2025-08-10 093403" src="https://github.com/user-attachments/assets/5250877f-d6f6-471f-9325-f86a2a893390" />

- check the ufw status
### Firewall Rule Configuration
```bash
# Initialize firewall
sudo ufw --force enable

# Configure access rules
sudo ufw allow 22/tcp   # allows SSH access
sudo ufw deny 23/tcp    # deny Telnet service

# Verify configuration
sudo ufw status numbered
```
## Conclusion        
This UFW firewall implementation on Kali Linux successfully enforced secure network access by blocking insecure Telnet (port 23) while permitting encrypted SSH connections (port 22). The configuration was validated through comprehensive testing, demonstrating proper rule enforcement.
