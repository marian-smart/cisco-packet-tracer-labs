
Lab 4: Device Security – Hostnames and Enable Passwords

# Objective
- To configure router hostnames, set enable passwords, apply password encryption,understand the difference between 'enable password' and 'enable secret, and save the running configuration to the startup configuration.

# Devices Used
- Cisco Router (R1)
- Cisco Router (R2, if applicable)

# Step-by-Step – What I Did

1. I accessed the router CLI and entered privileged EXEC mode using command:
enable

2. I entered global configuration mode and changed the router hostname to R1 using commands:
configure terminal
hostname R1

3. I configured an unencrypted enable password CCNA using command: 
enable password CCNA

4. I exited back to user EXEC mode and tested the enable password using commands:
exit
enable

5. I viewed the running configuration to confirm the enable password was stored in plain text using command:
show running-config

6. I enabled password encryption to secure the current and all future passwords using command:
service password-encryption

7. I viewed the running configuration again to confirm the enable password was now encrypted using command:
show running-config

8. I configured a more secure, encrypted enable secret password Cisco using command:
enable secret Cisco

9. I exited to user EXEC mode and returned to privileged EXEC mode to test which password is required using commands:
exit
enable
	Note: The router prompted for the enable secret, confirming it overrides the enable password

10. I viewed the running configuration to identify encryption types- enable password → Type 7 encryption and enable secret → Type 5 encryption using command:
show running-config

11. I saved the running configuration to the startup configuration  using command:
copy running-config startup-config

# Result
- Router hostname successfully changed
- Enable password and enable secret configured and tested
- Password encryption applied correctly
- Verified that enable secret takes precedence over enable password
- Running configuration saved successfully

# Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

