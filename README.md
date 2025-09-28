# firewall-setup

## Objective
Configure and test basic firewall rules to allow or block traffic.

## Tools
- Windows Defender Firewall with Advanced Security

## Steps
1. **List Current Rules**
   - Open `wf.msc` → Inbound Rules.
   - Screenshot: `1-rules.png`.

2. **Block Telnet (Port 23)**
   - Inbound Rules → New Rule → Port → TCP 23 → Block connection.
   - Named rule: `Block Telnet`.
   - Screenshot: `2-block-telnet.png`.

3. **Test the Rule**
   - In CMD:  
     ```cmd
     telnet localhost 23
     ```
   - Connection should fail.
   - Screenshot: `3-test-telnet.png`.

4. **Remove the Rule**
   - Delete the rule `Block Telnet`.
   - Screenshot: `4-remove-rule.png`.

## Configuration Export
See `firewall-rules.txt` for example output.

## Summary
- Firewall rules filter inbound/outbound traffic.  
- Example: blocked insecure Telnet (23) but kept normal traffic allowed.  
- This ensures better security by controlling network access.

## Screenshots
Located in `/windows/screenshots/`.
