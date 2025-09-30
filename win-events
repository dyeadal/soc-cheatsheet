# Window Event IDs

### 4624
🚩🚩🚩 Successful Logon 🚩🚩🚩

### 4625
Logon was unsuccessful

### 4634
User account password was changed

### 4674
User initiated logoff

### 4720
🚩🚩🚩Service Account Logon 🚩🚩🚩

### 4722
User account was created

### 4723
User account was enabled or disabled

### 4725 
User account deleted

### 4737
A security-enabled group was changed. 
A global security group that likely has admin access was changed and indicates privilege escalation through adding an account to a security group. Reach out to admins that user account was allowed to be added to a security group.

### 4765
SID History was added to an account.
Can signal potential credential compromise, privilege escalation, or other malicious activity. What to do !  Confirm with sysadmins if migration of domain account was scheduled or authorized.

### 4688 
🚩🚩🚩Event log cleared 🚩🚩🚩
Adversary likely trying to cover their tracks. It is important to perform log collection frequently as much as possible to track adversary movements and actions. 

### 4697
File was created

### 4698 
🚩🚩🚩Registry Key Creation🚩🚩🚩
Adverasies can create or modify registry keys to gain persistence

### 4732
Group Membership Changed

### 7045
🚩🚩🚩Process Creation. 🚩🚩🚩
Can be caused by PsExec, WMI, etc. 
Look for process name, parent process (this is _critical_), command-line arguments.

You can use this event ID to detect malware execution, suspicious scripts, and unauthorized software installations. PsExec is a common tool for lateral movement; WMI can be used maliciously.


### 2002
Sysmon event, network connection was created

### 2003 
Sysmon event, DNS query occurred
