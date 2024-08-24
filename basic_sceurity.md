### **Step 1: Enter Privileged Exec Mode**
- `enable`: Enter privileged exec mode.
- `conf t`: Enter configuration terminal.
- `hostname <name>`: Change the hostname.

---

### **Step 2: Set Password in Plaintext**
- `enable password ccna`: Set the password in plaintext.
- Test the configuration by exiting twice (`exit`).

![[Screenshot 2024-08-24 at 4.36.19 PM.png]]

---

### **Step 3: View Password in Running Configuration**
- `show running-configuration`: View the password in the running configuration.

---

### **Step 4: Enable Password Encryption**
1. **Be in Privileged Exec Mode:**
   - `enable`
   
2. **Enter Configuration Terminal:**
   - `conf t`
   
3. **Enable Password Encryption:**
   - `service password-encryption`

4. **View the Running Configuration:**
   - Use `show running-config` from privileged exec mode (`sh run`).
   - Alternatively, in configuration terminal, use `do sh run`.
![[Screenshot 2024-08-24 at 4.40.18 PM.png]]


---

### **Step 5: Enable More Secure Encryption (MD5)**
- **Use MD5 Encryption:**
   - `enable secret Cisco`: Set a secure password using MD5 encryption.
- **Note:** If both `enable password` and `enable secret` are set, only `enable secret` becomes valid.
- **Reminder:** Be in global privileged exec mode to see the running configuration.

---
![[Screenshot 2024-08-24 at 4.41.14 PM.png]]
### **Step 6: Save Running Configuration to Startup**
You can save the running configuration to startup configuration using the following commands:
```bash
write
write memory
copy running-config startup-config
