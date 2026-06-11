# IT Support & Troubleshooting Knowledge Base

Welcome to my technical repository. This folder serves as a documentation center for common IT support issues, system administration tasks, and home lab configurations.
## Scenario 1: User Cannot Connect to the Internet (Windows 10/11)

When a user reports network connectivity issues, I follow these diagnostic steps:
1. **Check Physical Layer:** Verify the Ethernet cable is securely plugged in or Wi-Fi is toggled ON.
2. **IP Verification:** Open Command Prompt and run `ipconfig /all` to check for a valid IP address. If it starts with `169.254`, it's an APIPA address (the computer can't reach the DHCP server).
3. **Network Reset:** Run `ipconfig /release` followed by `ipconfig /renew` to pull a new IP.
4. **DNS Flush:** Run `ipconfig /flushdns` to clear corrupt web-browsing caches.
5. **Ping Test:** Run `ping 8.8.8.8` (Google's DNS) to check absolute internet connectivity.
   ## Mock Ticket: Password Reset & Account Lockout
* **User Issue:** Marketing coordinator locked out of Active Directory account after returning from vacation.
* **Action Taken:** Verified user identity via secondary authentication method. Opened Active Directory Users and Computers (ADUC), located the user object, unlocked the account, and checked the "User must change password at next logon" box.
* **Result:** User successfully logged in and created a new secure password. Ticket marked resolved.
