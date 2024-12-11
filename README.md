# **Managing-Multiple-Sessions-on-a-VPS-via-Terminal**

The number of users shown in the uptime or who command output on your VPS represents the number of active sessions connected to the system. Each user session can include SSH connections, VNC sessions, or other terminal-based logins. If you saw "for e.g 3 users," it means there are three active sessions.

**Here's how to reduce it to one:**

**1. Check Active Sessions**
Run the 'who' or 'w' command to list all active sessions:

```bash
who
```
or 
```bash
w
```
This will display all active users, their terminal sessions, and connection details.

**2. Identify Unwanted Sessions**
Check the output for sessions you don’t need. For example:

```yaml
user1   pts/0    2024-12-11 08:00 (192.168.1.10)
user1   pts/1    2024-12-11 08:05 (:1)
user1   pts/2    2024-12-11 08:10 (bvncviewer)
```

**3.Terminate Extra Sessions**
To terminate a session, use the 'pkill' or 'kill' command with the 'pts' or process ID (PID):
   • To kill a specific session:



