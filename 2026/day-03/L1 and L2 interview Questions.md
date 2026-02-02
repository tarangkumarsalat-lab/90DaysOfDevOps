🐧 LINUX ADMIN INTERVIEW BIBLE (L1 + L2)
SECTION 1 – L1 Linux Admin (Basic / Junior)

Navigation & File System

Q	A

1. How do you check current directory?	pwd

2. How to list all files, including hidden?	ls -a

3. How to move between directories?	cd /path/to/dir

4. How to create a directory?	mkdir folder

5. How to create a file?	touch file.txt

6. How to delete files and folders?	rm file.txt, rm -r folder

7. How to copy/move files?	cp source dest, mv source dest

Permissions & Ownership

Q	A

8. How to view permissions?	ls -l

9. How to change permissions?	chmod 644 file

10. How to make a script executable?	chmod +x script.sh

11. How to change file owner?	chown user file

12. How to change group?	chgrp group file

User & Process Management
Q	A

13. How to add a user?	useradd username

14. How to set password?	passwd username

15. How to view running processes?	ps aux or top

16. How to kill a process?	kill -9 <pid>

17. How to check CPU & memory?	top, free -h

Disk & Storage

Q	A

18. Check disk usage?	df -h

19. Check folder size?	du -sh folder/

20. Find large files?	find / -size +100M

Search & Logs

Q	A

21. Search for file?	find / -name file.txt

22. Search text in file?	grep "error" file.txt

23. Monitor logs in real-time?	tail -f /var/log/syslog

24. Search recursively in directory?	grep -r "pattern" folder/

Archive & Backup

Q	A

25. Create a tar archive?	tar -cvf backup.tar folder/

26. Extract a tar file?	tar -xvf backup.tar

27. Compress with gzip?	gzip file, gunzip file.gz

Scenario Questions

Scenario	Answer Steps

Disk full	df -h, du -sh /*, delete old logs, compress files, restart service

Permission denied	ls -l, chmod 755 file, chown user file

File accidentally deleted	Restore from backup (tar / snapshot)

SECTION 2 – L2 Linux Admin (Intermediate / Senior)

Service & Process Management

Q	A
26. Check service status	systemctl status apache2

27. Restart service	systemctl restart apache2

28. View service logs	journalctl -u apache2

29. Kill hung process	`ps aux

30. Monitor CPU & memory per process	top, ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu

Networking

Q	A

31. Check IP configuration	ip addr show, ifconfig

32. Ping a host	ping 8.8.8.8

33. Trace route	traceroute google.com

34. Check listening ports	netstat -tulnp, ss -tulnp

35. Check process using port	lsof -i :80

Automation & Cron

Q	A

36. Edit cron jobs	crontab -e

37. Schedule daily backup at 2AM	0 2 * * * tar -czvf /backup/home.tar.gz /home

38. Check cron logs	/var/log/cron

Disk, Filesystem & Backup

Q	A

39. Check disk usage	df -h, du -sh /*

40. Resize filesystem	resize2fs /dev/sda1

41. Mount a filesystem	mount /dev/sdb1 /mnt

42. Backup files	tar -czvf backup.tar.gz /data

43. Restore backup	tar -xzvf backup.tar.gz -C /restore/path

Scenario-Based Questions

Scenario	Answer Steps

Apache not starting	systemctl status apache2, check logs, check ports, restart service

Full root partition	df -h, du -sh /*, delete temp files, resize partition or add storage

High CPU usage	top, ps aux --sort=-%cpu, identify process, restart service or kill

Network issue	Check ip addr, ping gateway, traceroute, check firewall rules

Advanced / Bonus

Q	A

44. Check open files by process	lsof -p <pid>

45. Check inode usage	df -i

46. Monitor logs for specific pattern	`tail -f /var/log/syslog

47. Setup user with sudo	useradd john, usermod -aG sudo john

48. Find recently modified files	find / -type f -mtime -1

49. Remove large temp files	find /tmp -type f -size +100M -delete

50. Check service dependencies	systemctl list-dependencies apache2

