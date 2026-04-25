# Incident Report — SSH Brute Force Attempt

## 1. Summary
A series of failed SSH login attempts were detected 
originating from IP address 185.199.110.153, 
indicating a potential brute force attack.

## 2. Timeline
- 2024-01-12 14:32 — First failed login attempt
- 2024-01-12 14:33 — 25 consecutive attempts
- 2024-01-12 14:34 — Alert triggered by the SIEM

## 3. Evidence
- System log entry:
Jan 12 14:33:12 server sshd[2451]:
Failed password for root from 185.199.110.153
port 54321 ssh2
- Total number of attempts: 57  
- Source: IP 185.199.110.153 (geolocation: Russia)

## 4. Analysis
The repeated failed login attempts within a short 
period are consistent with automated brute force activity. 
The attacker appears to be attempting to gain 
unauthorized access to the root account.

## 5. Actions Taken
- Blocked the source IP address on the firewall
- Notified the Level 2 (N2) security team
- Recommendation: enable SSH key-based authentication
- and disable password authentication

## 6. Conclusion
Low-severity security incident successfully mitigated. 
No impact on system integrity or availability.
