🎯 LINUX ADMIN INTERVIEW QUESTIONS (REAL)

1️⃣ What is the Linux file system?

👉 A tree-like structure starting from / where everything is treated as a file.

2️⃣ Difference between hard link & soft link?

Hard Link	--- Soft Link

Same inode ---	Different inode

Can’t cross FS ---	Can cross FS

File survives deletion ---	Link breaks

3️⃣ How do you find large files?

find / -size +1G

4️⃣ What does chmod 644 mean?

👉 Owner: read/write

👉 Group & others: read only

5️⃣ How do you check disk usage?

df -h

du -sh /*

6️⃣ How do you search text in logs?

grep -r "failed" /var/log

7️⃣ How do you take backup?

👉 tar, rsync, cron automation

8️⃣ What happens if / partition is full?

👉 System services fail, login issues, app crashes.

🧠 REAL-LIFE ADMIN SCENARIOS (VERY IMPORTANT)

🚨 Scenario 1: Disk Full

df -h

du -sh /*

find / -size +500M


✔ Delete old logs

✔ Compress files

✔ Restart service

🚨 Scenario 2: Permission Denied Error

ls -l file

chmod 755 file

chown user file

🚨 Scenario 3: Website Not Loading

systemctl status apache2

df -h

tail -f /var/log/apache2/error.log

🚨 Scenario 4: Accidentally Deleted File

👉 Restore from backup (tar / snapshot)
