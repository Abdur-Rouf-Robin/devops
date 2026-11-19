# DevOps

## chapter 1 Linux and Bash

- the shell = a program that runs commands. Bash is the usual one on a server
- a process we start in the shell is a child of the shell
- `pwd` prints the folder. `ls` lists it. `cd` moves
- a pipe `|` sends the output of one command into the next
- redirect `>` writes a file. `>>` appends
- permissions are read, write, execute, for owner, group, and others
- `chmod` changes them. a private key is not world-readable
- a unit file or PM2 keeps a process running after we log out. a command in an SSH session dies when we disconnect, unless we used a process manager
- we edit on the laptop and deploy. we do not hotfix production by typing into a live file and forgetting

```bash
ls -la
ps aux | grep node
tail -n 100 /var/log/nginx/error.log
```

- `tail` shows the end of a log. that is the first place a 502 sends us
- `grep` filters lines. the pipe is why `ps` and `grep` are one thought

- homework of chapter 1
```bash
# 1a  list files with their permissions
# 1b  the last 50 nginx error lines
# 1c  why a private key is not chmod 644
```

- example 1. shell around log and process for pc_12
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 21 /var/log/nginx/error.log
# look for pc_12 in the recent lines
```

- homework
```bash
# 1a  list permissions
# 1b  last lines of the nginx error log
# 1c  chmod 600 on a key, not 644
```

- example 2. shell around log and process for m_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 22 /var/log/nginx/error.log
# look for m_1 in the recent lines
```

- homework
```bash
# 2a  list permissions
# 2b  last lines of the nginx error log
# 2c  chmod 600 on a key, not 644
```

- example 3. shell around log and process for t_9
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 23 /var/log/nginx/error.log
# look for t_9 in the recent lines
```

- homework
```bash
# 3a  list permissions
# 3b  last lines of the nginx error log
# 3c  chmod 600 on a key, not 644
```

- example 4. shell around log and process for v_4
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 24 /var/log/nginx/error.log
# look for v_4 in the recent lines
```

- homework
```bash
# 4a  list permissions
# 4b  last lines of the nginx error log
# 4c  chmod 600 on a key, not 644
```

- example 5. shell around log and process for f_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 25 /var/log/nginx/error.log
# look for f_2 in the recent lines
```

- homework
```bash
# 5a  list permissions
# 5b  last lines of the nginx error log
# 5c  chmod 600 on a key, not 644
```

- example 6. shell around log and process for u_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 26 /var/log/nginx/error.log
# look for u_3 in the recent lines
```

- homework
```bash
# 6a  list permissions
# 6b  last lines of the nginx error log
# 6c  chmod 600 on a key, not 644
```

- example 7. shell around log and process for pay_8
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 27 /var/log/nginx/error.log
# look for pay_8 in the recent lines
```

- homework
```bash
# 7a  list permissions
# 7b  last lines of the nginx error log
# 7c  chmod 600 on a key, not 644
```

- example 8. shell around log and process for room_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 28 /var/log/nginx/error.log
# look for room_2 in the recent lines
```

- homework
```bash
# 8a  list permissions
# 8b  last lines of the nginx error log
# 8c  chmod 600 on a key, not 644
```

- example 9. shell around log and process for vs_7
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 29 /var/log/nginx/error.log
# look for vs_7 in the recent lines
```

- homework
```bash
# 9a  list permissions
# 9b  last lines of the nginx error log
# 9c  chmod 600 on a key, not 644
```

- example 10. shell around log and process for sc_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 30 /var/log/nginx/error.log
# look for sc_3 in the recent lines
```

- homework
```bash
# 10a  list permissions
# 10b  last lines of the nginx error log
# 10c  chmod 600 on a key, not 644
```

- example 11. shell around log and process for tm_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 31 /var/log/nginx/error.log
# look for tm_2 in the recent lines
```

- homework
```bash
# 11a  list permissions
# 11b  last lines of the nginx error log
# 11c  chmod 600 on a key, not 644
```

- example 12. shell around log and process for up_6
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 32 /var/log/nginx/error.log
# look for up_6 in the recent lines
```

- homework
```bash
# 12a  list permissions
# 12b  last lines of the nginx error log
# 12c  chmod 600 on a key, not 644
```

- example 13. shell around log and process for st_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 33 /var/log/nginx/error.log
# look for st_1 in the recent lines
```

- homework
```bash
# 13a  list permissions
# 13b  last lines of the nginx error log
# 13c  chmod 600 on a key, not 644
```

- example 14. shell around log and process for n_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 34 /var/log/nginx/error.log
# look for n_2 in the recent lines
```

- homework
```bash
# 14a  list permissions
# 14b  last lines of the nginx error log
# 14c  chmod 600 on a key, not 644
```

- example 15. shell around log and process for b_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 35 /var/log/nginx/error.log
# look for b_3 in the recent lines
```

- homework
```bash
# 15a  list permissions
# 15b  last lines of the nginx error log
# 15c  chmod 600 on a key, not 644
```

- example 16. shell around log and process for se_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 36 /var/log/nginx/error.log
# look for se_1 in the recent lines
```

- homework
```bash
# 16a  list permissions
# 16b  last lines of the nginx error log
# 16c  chmod 600 on a key, not 644
```

- example 17. shell around log and process for q_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 37 /var/log/nginx/error.log
# look for q_1 in the recent lines
```

- homework
```bash
# 17a  list permissions
# 17b  last lines of the nginx error log
# 17c  chmod 600 on a key, not 644
```

- example 18. shell around log and process for r_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 38 /var/log/nginx/error.log
# look for r_1 in the recent lines
```

- homework
```bash
# 18a  list permissions
# 18b  last lines of the nginx error log
# 18c  chmod 600 on a key, not 644
```

- example 19. shell around log and process for pc_12
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 39 /var/log/nginx/error.log
# look for pc_12 in the recent lines
```

- homework
```bash
# 19a  list permissions
# 19b  last lines of the nginx error log
# 19c  chmod 600 on a key, not 644
```

- example 20. shell around log and process for m_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 40 /var/log/nginx/error.log
# look for m_1 in the recent lines
```

- homework
```bash
# 20a  list permissions
# 20b  last lines of the nginx error log
# 20c  chmod 600 on a key, not 644
```

- example 21. shell around log and process for t_9
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 41 /var/log/nginx/error.log
# look for t_9 in the recent lines
```

- homework
```bash
# 21a  list permissions
# 21b  last lines of the nginx error log
# 21c  chmod 600 on a key, not 644
```

- example 22. shell around log and process for v_4
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 42 /var/log/nginx/error.log
# look for v_4 in the recent lines
```

- homework
```bash
# 22a  list permissions
# 22b  last lines of the nginx error log
# 22c  chmod 600 on a key, not 644
```

- example 23. shell around log and process for f_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 43 /var/log/nginx/error.log
# look for f_2 in the recent lines
```

- homework
```bash
# 23a  list permissions
# 23b  last lines of the nginx error log
# 23c  chmod 600 on a key, not 644
```

- example 24. shell around log and process for u_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 44 /var/log/nginx/error.log
# look for u_3 in the recent lines
```

- homework
```bash
# 24a  list permissions
# 24b  last lines of the nginx error log
# 24c  chmod 600 on a key, not 644
```

- example 25. shell around log and process for pay_8
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 45 /var/log/nginx/error.log
# look for pay_8 in the recent lines
```

- homework
```bash
# 25a  list permissions
# 25b  last lines of the nginx error log
# 25c  chmod 600 on a key, not 644
```

- example 26. shell around log and process for room_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 46 /var/log/nginx/error.log
# look for room_2 in the recent lines
```

- homework
```bash
# 26a  list permissions
# 26b  last lines of the nginx error log
# 26c  chmod 600 on a key, not 644
```

- example 27. shell around log and process for vs_7
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 47 /var/log/nginx/error.log
# look for vs_7 in the recent lines
```

- homework
```bash
# 27a  list permissions
# 27b  last lines of the nginx error log
# 27c  chmod 600 on a key, not 644
```

- example 28. shell around log and process for sc_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 48 /var/log/nginx/error.log
# look for sc_3 in the recent lines
```

- homework
```bash
# 28a  list permissions
# 28b  last lines of the nginx error log
# 28c  chmod 600 on a key, not 644
```

- example 29. shell around log and process for tm_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 49 /var/log/nginx/error.log
# look for tm_2 in the recent lines
```

- homework
```bash
# 29a  list permissions
# 29b  last lines of the nginx error log
# 29c  chmod 600 on a key, not 644
```

- example 30. shell around log and process for up_6
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 20 /var/log/nginx/error.log
# look for up_6 in the recent lines
```

- homework
```bash
# 30a  list permissions
# 30b  last lines of the nginx error log
# 30c  chmod 600 on a key, not 644
```

- example 31. shell around log and process for st_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 21 /var/log/nginx/error.log
# look for st_1 in the recent lines
```

- homework
```bash
# 31a  list permissions
# 31b  last lines of the nginx error log
# 31c  chmod 600 on a key, not 644
```

- example 32. shell around log and process for n_2
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 22 /var/log/nginx/error.log
# look for n_2 in the recent lines
```

- homework
```bash
# 32a  list permissions
# 32b  last lines of the nginx error log
# 32c  chmod 600 on a key, not 644
```

- example 33. shell around log and process for b_3
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 23 /var/log/nginx/error.log
# look for b_3 in the recent lines
```

- homework
```bash
# 33a  list permissions
# 33b  last lines of the nginx error log
# 33c  chmod 600 on a key, not 644
```

- example 34. shell around log and process for se_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 24 /var/log/nginx/error.log
# look for se_1 in the recent lines
```

- homework
```bash
# 34a  list permissions
# 34b  last lines of the nginx error log
# 34c  chmod 600 on a key, not 644
```

- example 35. shell around log and process for q_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 25 /var/log/nginx/error.log
# look for q_1 in the recent lines
```

- homework
```bash
# 35a  list permissions
# 35b  last lines of the nginx error log
# 35c  chmod 600 on a key, not 644
```

- example 36. shell around log and process for r_1
- pipe sends stdout to the next command
- permissions: a private key is not world-readable
- PM2 or a unit file keeps the process after SSH ends

```bash
pwd
ls -la
ps aux | grep node
tail -n 26 /var/log/nginx/error.log
# look for r_1 in the recent lines
```

- homework
```bash
# 36a  list permissions
# 36b  last lines of the nginx error log
# 36c  chmod 600 on a key, not 644
```

## chapter 2 Networking basics

- an interface has an address. the public one is how the internet reaches the box. a private one is how the box reaches the database on the same network
- a port is the number of the program. 22 SSH, 80 HTTP, 443 HTTPS, 5432 Postgres
- we do not publish 5432 to the world
- DNS turns the name into the address. the firewall decides if the port is open
- `curl` from the server tells us if the API is up without the browser
- inside Docker, localhost is the container. the database host is the service name

```bash
curl -I https://vms.arrobin.com
ss -lntp | head
```

- `-I` fetches headers. a 200 or a 301 is the front door answering
- `ss` shows who is listening. the Nest port should be local if nginx is the public door

- homework of chapter 2
```bash
# 2a  which port is public, 443 or 5432
# 2b  why curl to localhost from the API container does not reach Postgres
# 2c  what DNS answers, and what a firewall answers
```

- example 1. ports for the box that serves pc_12
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/port-calls/pc_12
ss -lntp | head
```

- homework
```bash
# 1a  public port for pc_12 is 443
# 1b  do not publish 5432
# 1c  DNS names the host. the firewall opens the port
```

- example 2. ports for the box that serves m_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/matches/m_1
ss -lntp | head
```

- homework
```bash
# 2a  public port for m_1 is 443
# 2b  do not publish 5432
# 2c  DNS names the host. the firewall opens the port
```

- example 3. ports for the box that serves t_9
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/tournaments/t_9
ss -lntp | head
```

- homework
```bash
# 3a  public port for t_9 is 443
# 3b  do not publish 5432
# 3c  DNS names the host. the firewall opens the port
```

- example 4. ports for the box that serves v_4
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/videos/v_4
ss -lntp | head
```

- homework
```bash
# 4a  public port for v_4 is 443
# 4b  do not publish 5432
# 4c  DNS names the host. the firewall opens the port
```

- example 5. ports for the box that serves f_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/facts/f_2
ss -lntp | head
```

- homework
```bash
# 5a  public port for f_2 is 443
# 5b  do not publish 5432
# 5c  DNS names the host. the firewall opens the port
```

- example 6. ports for the box that serves u_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/users/u_3
ss -lntp | head
```

- homework
```bash
# 6a  public port for u_3 is 443
# 6b  do not publish 5432
# 6c  DNS names the host. the firewall opens the port
```

- example 7. ports for the box that serves pay_8
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/payments/pay_8
ss -lntp | head
```

- homework
```bash
# 7a  public port for pay_8 is 443
# 7b  do not publish 5432
# 7c  DNS names the host. the firewall opens the port
```

- example 8. ports for the box that serves room_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/rooms/room_2
ss -lntp | head
```

- homework
```bash
# 8a  public port for room_2 is 443
# 8b  do not publish 5432
# 8c  DNS names the host. the firewall opens the port
```

- example 9. ports for the box that serves vs_7
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/vessels/vs_7
ss -lntp | head
```

- homework
```bash
# 9a  public port for vs_7 is 443
# 9b  do not publish 5432
# 9c  DNS names the host. the firewall opens the port
```

- example 10. ports for the box that serves sc_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/scores/sc_3
ss -lntp | head
```

- homework
```bash
# 10a  public port for sc_3 is 443
# 10b  do not publish 5432
# 10c  DNS names the host. the firewall opens the port
```

- example 11. ports for the box that serves tm_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/teams/tm_2
ss -lntp | head
```

- homework
```bash
# 11a  public port for tm_2 is 443
# 11b  do not publish 5432
# 11c  DNS names the host. the firewall opens the port
```

- example 12. ports for the box that serves up_6
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/uploads/up_6
ss -lntp | head
```

- homework
```bash
# 12a  public port for up_6 is 443
# 12b  do not publish 5432
# 12c  DNS names the host. the firewall opens the port
```

- example 13. ports for the box that serves st_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/standings/st_1
ss -lntp | head
```

- homework
```bash
# 13a  public port for st_1 is 443
# 13b  do not publish 5432
# 13c  DNS names the host. the firewall opens the port
```

- example 14. ports for the box that serves n_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/notices/n_2
ss -lntp | head
```

- homework
```bash
# 14a  public port for n_2 is 443
# 14b  do not publish 5432
# 14c  DNS names the host. the firewall opens the port
```

- example 15. ports for the box that serves b_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/brackets/b_3
ss -lntp | head
```

- homework
```bash
# 15a  public port for b_3 is 443
# 15b  do not publish 5432
# 15c  DNS names the host. the firewall opens the port
```

- example 16. ports for the box that serves se_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/sessions/se_1
ss -lntp | head
```

- homework
```bash
# 16a  public port for se_1 is 443
# 16b  do not publish 5432
# 16c  DNS names the host. the firewall opens the port
```

- example 17. ports for the box that serves q_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/queues/q_1
ss -lntp | head
```

- homework
```bash
# 17a  public port for q_1 is 443
# 17b  do not publish 5432
# 17c  DNS names the host. the firewall opens the port
```

- example 18. ports for the box that serves r_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/roles/r_1
ss -lntp | head
```

- homework
```bash
# 18a  public port for r_1 is 443
# 18b  do not publish 5432
# 18c  DNS names the host. the firewall opens the port
```

- example 19. ports for the box that serves pc_12
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/port-calls/pc_12
ss -lntp | head
```

- homework
```bash
# 19a  public port for pc_12 is 443
# 19b  do not publish 5432
# 19c  DNS names the host. the firewall opens the port
```

- example 20. ports for the box that serves m_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/matches/m_1
ss -lntp | head
```

- homework
```bash
# 20a  public port for m_1 is 443
# 20b  do not publish 5432
# 20c  DNS names the host. the firewall opens the port
```

- example 21. ports for the box that serves t_9
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/tournaments/t_9
ss -lntp | head
```

- homework
```bash
# 21a  public port for t_9 is 443
# 21b  do not publish 5432
# 21c  DNS names the host. the firewall opens the port
```

- example 22. ports for the box that serves v_4
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/videos/v_4
ss -lntp | head
```

- homework
```bash
# 22a  public port for v_4 is 443
# 22b  do not publish 5432
# 22c  DNS names the host. the firewall opens the port
```

- example 23. ports for the box that serves f_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/facts/f_2
ss -lntp | head
```

- homework
```bash
# 23a  public port for f_2 is 443
# 23b  do not publish 5432
# 23c  DNS names the host. the firewall opens the port
```

- example 24. ports for the box that serves u_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/users/u_3
ss -lntp | head
```

- homework
```bash
# 24a  public port for u_3 is 443
# 24b  do not publish 5432
# 24c  DNS names the host. the firewall opens the port
```

- example 25. ports for the box that serves pay_8
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/payments/pay_8
ss -lntp | head
```

- homework
```bash
# 25a  public port for pay_8 is 443
# 25b  do not publish 5432
# 25c  DNS names the host. the firewall opens the port
```

- example 26. ports for the box that serves room_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/rooms/room_2
ss -lntp | head
```

- homework
```bash
# 26a  public port for room_2 is 443
# 26b  do not publish 5432
# 26c  DNS names the host. the firewall opens the port
```

- example 27. ports for the box that serves vs_7
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/vessels/vs_7
ss -lntp | head
```

- homework
```bash
# 27a  public port for vs_7 is 443
# 27b  do not publish 5432
# 27c  DNS names the host. the firewall opens the port
```

- example 28. ports for the box that serves sc_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/scores/sc_3
ss -lntp | head
```

- homework
```bash
# 28a  public port for sc_3 is 443
# 28b  do not publish 5432
# 28c  DNS names the host. the firewall opens the port
```

- example 29. ports for the box that serves tm_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/teams/tm_2
ss -lntp | head
```

- homework
```bash
# 29a  public port for tm_2 is 443
# 29b  do not publish 5432
# 29c  DNS names the host. the firewall opens the port
```

- example 30. ports for the box that serves up_6
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/uploads/up_6
ss -lntp | head
```

- homework
```bash
# 30a  public port for up_6 is 443
# 30b  do not publish 5432
# 30c  DNS names the host. the firewall opens the port
```

- example 31. ports for the box that serves st_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/standings/st_1
ss -lntp | head
```

- homework
```bash
# 31a  public port for st_1 is 443
# 31b  do not publish 5432
# 31c  DNS names the host. the firewall opens the port
```

- example 32. ports for the box that serves n_2
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/notices/n_2
ss -lntp | head
```

- homework
```bash
# 32a  public port for n_2 is 443
# 32b  do not publish 5432
# 32c  DNS names the host. the firewall opens the port
```

- example 33. ports for the box that serves b_3
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/brackets/b_3
ss -lntp | head
```

- homework
```bash
# 33a  public port for b_3 is 443
# 33b  do not publish 5432
# 33c  DNS names the host. the firewall opens the port
```

- example 34. ports for the box that serves se_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/sessions/se_1
ss -lntp | head
```

- homework
```bash
# 34a  public port for se_1 is 443
# 34b  do not publish 5432
# 34c  DNS names the host. the firewall opens the port
```

- example 35. ports for the box that serves q_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/queues/q_1
ss -lntp | head
```

- homework
```bash
# 35a  public port for q_1 is 443
# 35b  do not publish 5432
# 35c  DNS names the host. the firewall opens the port
```

- example 36. ports for the box that serves r_1
- 443 is public. 5432 is not
- curl -I checks the front door
- inside the API container, localhost is not Postgres

```bash
curl -I https://example.com/roles/r_1
ss -lntp | head
```

- homework
```bash
# 36a  public port for r_1 is 443
# 36b  do not publish 5432
# 36c  DNS names the host. the firewall opens the port
```

## chapter 3 Git and GitHub

- a commit = a snapshot with a message and a parent
- a branch = a name for a commit we are building on
- `status` shows what changed. `diff` shows the lines
- `add` stages. `commit` records. `push` sends the branch
- a pull request is a branch we ask to merge. the conversation and the checks live there
- `main` is the branch we deploy. we do not rewrite its history after it is shared
- a merge commit joins two lines. a rebase replays our commits on top. we rebase only branches that are not shared
- `.gitignore` keeps `node_modules` and `.env` out of the repo

```bash
git status
git diff
git add backendFull.md
git commit -m "Describe the HTTP status codes with examples."
git push
```

- the message says why. the diff already says what
- a secret in a commit stays in the history. we do not commit `.env`

- homework of chapter 3
```bash
# 3a  the three commands from a changed file to a recorded commit
# 3b  what a pull request is for
# 3c  a file that must stay in .gitignore
```

- example 1. commit the note, not a secret, for change pc_12
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain port-calls pc_12 with another example."
git push
```

- homework
```bash
# 1a  three commands from a change to a commit
# 1b  a pull request is the branch we ask to merge
# 1c  .env for pc_12 is not committed
```

- example 2. commit the note, not a secret, for change m_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain matches m_1 with another example."
git push
```

- homework
```bash
# 2a  three commands from a change to a commit
# 2b  a pull request is the branch we ask to merge
# 2c  .env for m_1 is not committed
```

- example 3. commit the note, not a secret, for change t_9
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain tournaments t_9 with another example."
git push
```

- homework
```bash
# 3a  three commands from a change to a commit
# 3b  a pull request is the branch we ask to merge
# 3c  .env for t_9 is not committed
```

- example 4. commit the note, not a secret, for change v_4
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain videos v_4 with another example."
git push
```

- homework
```bash
# 4a  three commands from a change to a commit
# 4b  a pull request is the branch we ask to merge
# 4c  .env for v_4 is not committed
```

- example 5. commit the note, not a secret, for change f_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain facts f_2 with another example."
git push
```

- homework
```bash
# 5a  three commands from a change to a commit
# 5b  a pull request is the branch we ask to merge
# 5c  .env for f_2 is not committed
```

- example 6. commit the note, not a secret, for change u_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain users u_3 with another example."
git push
```

- homework
```bash
# 6a  three commands from a change to a commit
# 6b  a pull request is the branch we ask to merge
# 6c  .env for u_3 is not committed
```

- example 7. commit the note, not a secret, for change pay_8
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain payments pay_8 with another example."
git push
```

- homework
```bash
# 7a  three commands from a change to a commit
# 7b  a pull request is the branch we ask to merge
# 7c  .env for pay_8 is not committed
```

- example 8. commit the note, not a secret, for change room_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain rooms room_2 with another example."
git push
```

- homework
```bash
# 8a  three commands from a change to a commit
# 8b  a pull request is the branch we ask to merge
# 8c  .env for room_2 is not committed
```

- example 9. commit the note, not a secret, for change vs_7
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain vessels vs_7 with another example."
git push
```

- homework
```bash
# 9a  three commands from a change to a commit
# 9b  a pull request is the branch we ask to merge
# 9c  .env for vs_7 is not committed
```

- example 10. commit the note, not a secret, for change sc_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain scores sc_3 with another example."
git push
```

- homework
```bash
# 10a  three commands from a change to a commit
# 10b  a pull request is the branch we ask to merge
# 10c  .env for sc_3 is not committed
```

- example 11. commit the note, not a secret, for change tm_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain teams tm_2 with another example."
git push
```

- homework
```bash
# 11a  three commands from a change to a commit
# 11b  a pull request is the branch we ask to merge
# 11c  .env for tm_2 is not committed
```

- example 12. commit the note, not a secret, for change up_6
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain uploads up_6 with another example."
git push
```

- homework
```bash
# 12a  three commands from a change to a commit
# 12b  a pull request is the branch we ask to merge
# 12c  .env for up_6 is not committed
```

- example 13. commit the note, not a secret, for change st_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain standings st_1 with another example."
git push
```

- homework
```bash
# 13a  three commands from a change to a commit
# 13b  a pull request is the branch we ask to merge
# 13c  .env for st_1 is not committed
```

- example 14. commit the note, not a secret, for change n_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain notices n_2 with another example."
git push
```

- homework
```bash
# 14a  three commands from a change to a commit
# 14b  a pull request is the branch we ask to merge
# 14c  .env for n_2 is not committed
```

- example 15. commit the note, not a secret, for change b_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain brackets b_3 with another example."
git push
```

- homework
```bash
# 15a  three commands from a change to a commit
# 15b  a pull request is the branch we ask to merge
# 15c  .env for b_3 is not committed
```

- example 16. commit the note, not a secret, for change se_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain sessions se_1 with another example."
git push
```

- homework
```bash
# 16a  three commands from a change to a commit
# 16b  a pull request is the branch we ask to merge
# 16c  .env for se_1 is not committed
```

- example 17. commit the note, not a secret, for change q_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain queues q_1 with another example."
git push
```

- homework
```bash
# 17a  three commands from a change to a commit
# 17b  a pull request is the branch we ask to merge
# 17c  .env for q_1 is not committed
```

- example 18. commit the note, not a secret, for change r_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain roles r_1 with another example."
git push
```

- homework
```bash
# 18a  three commands from a change to a commit
# 18b  a pull request is the branch we ask to merge
# 18c  .env for r_1 is not committed
```

- example 19. commit the note, not a secret, for change pc_12
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain port-calls pc_12 with another example."
git push
```

- homework
```bash
# 19a  three commands from a change to a commit
# 19b  a pull request is the branch we ask to merge
# 19c  .env for pc_12 is not committed
```

- example 20. commit the note, not a secret, for change m_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain matches m_1 with another example."
git push
```

- homework
```bash
# 20a  three commands from a change to a commit
# 20b  a pull request is the branch we ask to merge
# 20c  .env for m_1 is not committed
```

- example 21. commit the note, not a secret, for change t_9
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain tournaments t_9 with another example."
git push
```

- homework
```bash
# 21a  three commands from a change to a commit
# 21b  a pull request is the branch we ask to merge
# 21c  .env for t_9 is not committed
```

- example 22. commit the note, not a secret, for change v_4
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain videos v_4 with another example."
git push
```

- homework
```bash
# 22a  three commands from a change to a commit
# 22b  a pull request is the branch we ask to merge
# 22c  .env for v_4 is not committed
```

- example 23. commit the note, not a secret, for change f_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain facts f_2 with another example."
git push
```

- homework
```bash
# 23a  three commands from a change to a commit
# 23b  a pull request is the branch we ask to merge
# 23c  .env for f_2 is not committed
```

- example 24. commit the note, not a secret, for change u_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain users u_3 with another example."
git push
```

- homework
```bash
# 24a  three commands from a change to a commit
# 24b  a pull request is the branch we ask to merge
# 24c  .env for u_3 is not committed
```

- example 25. commit the note, not a secret, for change pay_8
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain payments pay_8 with another example."
git push
```

- homework
```bash
# 25a  three commands from a change to a commit
# 25b  a pull request is the branch we ask to merge
# 25c  .env for pay_8 is not committed
```

- example 26. commit the note, not a secret, for change room_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain rooms room_2 with another example."
git push
```

- homework
```bash
# 26a  three commands from a change to a commit
# 26b  a pull request is the branch we ask to merge
# 26c  .env for room_2 is not committed
```

- example 27. commit the note, not a secret, for change vs_7
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain vessels vs_7 with another example."
git push
```

- homework
```bash
# 27a  three commands from a change to a commit
# 27b  a pull request is the branch we ask to merge
# 27c  .env for vs_7 is not committed
```

- example 28. commit the note, not a secret, for change sc_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain scores sc_3 with another example."
git push
```

- homework
```bash
# 28a  three commands from a change to a commit
# 28b  a pull request is the branch we ask to merge
# 28c  .env for sc_3 is not committed
```

- example 29. commit the note, not a secret, for change tm_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain teams tm_2 with another example."
git push
```

- homework
```bash
# 29a  three commands from a change to a commit
# 29b  a pull request is the branch we ask to merge
# 29c  .env for tm_2 is not committed
```

- example 30. commit the note, not a secret, for change up_6
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain uploads up_6 with another example."
git push
```

- homework
```bash
# 30a  three commands from a change to a commit
# 30b  a pull request is the branch we ask to merge
# 30c  .env for up_6 is not committed
```

- example 31. commit the note, not a secret, for change st_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain standings st_1 with another example."
git push
```

- homework
```bash
# 31a  three commands from a change to a commit
# 31b  a pull request is the branch we ask to merge
# 31c  .env for st_1 is not committed
```

- example 32. commit the note, not a secret, for change n_2
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain notices n_2 with another example."
git push
```

- homework
```bash
# 32a  three commands from a change to a commit
# 32b  a pull request is the branch we ask to merge
# 32c  .env for n_2 is not committed
```

- example 33. commit the note, not a secret, for change b_3
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain brackets b_3 with another example."
git push
```

- homework
```bash
# 33a  three commands from a change to a commit
# 33b  a pull request is the branch we ask to merge
# 33c  .env for b_3 is not committed
```

- example 34. commit the note, not a secret, for change se_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain sessions se_1 with another example."
git push
```

- homework
```bash
# 34a  three commands from a change to a commit
# 34b  a pull request is the branch we ask to merge
# 34c  .env for se_1 is not committed
```

- example 35. commit the note, not a secret, for change q_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain queues q_1 with another example."
git push
```

- homework
```bash
# 35a  three commands from a change to a commit
# 35b  a pull request is the branch we ask to merge
# 35c  .env for q_1 is not committed
```

- example 36. commit the note, not a secret, for change r_1
- status, diff, add, commit, push
- main is not rewritten after it is shared
- .env stays ignored

```bash
git status
git diff
git add notes.md
git commit -m "Explain roles r_1 with another example."
git push
```

- homework
```bash
# 36a  three commands from a change to a commit
# 36b  a pull request is the branch we ask to merge
# 36c  .env for r_1 is not committed
```

## chapter 4 Docker

- an image = a packed filesystem and a start command
- a container = a running image. it has its own files and its own network namespace
- a Dockerfile builds the image in layers. a layer is cached when the lines above it did not change
- we copy the lockfile and install dependencies before we copy the source, so a code change does not reinstall every package
- the process in the container is PID 1. it should handle a stop signal and exit
- we do not run as root if the process does not need to
- localhost inside the container is the container

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
RUN npm run build
CMD ["node", "dist/main.js"]
```

- `npm ci` installs from the lockfile. it does not update it
- the image does not contain `.env`. we pass environment at run time

- homework of chapter 4
```dockerfile
# 4a  why package files are copied before the rest of the source
# 4b  what localhost means in this container
# 4c  where the database password comes from, if it is not in the image
```

- example 1. image layers for an API that serves pc_12
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# pc_12 is data, not a layer
```

- homework
```dockerfile
# 1a  why the lockfile is copied first
# 1b  localhost in this container is the container
# 1c  DATABASE_URL is passed in, not baked in, for port-calls
```

- example 2. image layers for an API that serves m_1
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# m_1 is data, not a layer
```

- homework
```dockerfile
# 2a  why the lockfile is copied first
# 2b  localhost in this container is the container
# 2c  DATABASE_URL is passed in, not baked in, for matches
```

- example 3. image layers for an API that serves t_9
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# t_9 is data, not a layer
```

- homework
```dockerfile
# 3a  why the lockfile is copied first
# 3b  localhost in this container is the container
# 3c  DATABASE_URL is passed in, not baked in, for tournaments
```

- example 4. image layers for an API that serves v_4
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# v_4 is data, not a layer
```

- homework
```dockerfile
# 4a  why the lockfile is copied first
# 4b  localhost in this container is the container
# 4c  DATABASE_URL is passed in, not baked in, for videos
```

- example 5. image layers for an API that serves f_2
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# f_2 is data, not a layer
```

- homework
```dockerfile
# 5a  why the lockfile is copied first
# 5b  localhost in this container is the container
# 5c  DATABASE_URL is passed in, not baked in, for facts
```

- example 6. image layers for an API that serves u_3
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# u_3 is data, not a layer
```

- homework
```dockerfile
# 6a  why the lockfile is copied first
# 6b  localhost in this container is the container
# 6c  DATABASE_URL is passed in, not baked in, for users
```

- example 7. image layers for an API that serves pay_8
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# pay_8 is data, not a layer
```

- homework
```dockerfile
# 7a  why the lockfile is copied first
# 7b  localhost in this container is the container
# 7c  DATABASE_URL is passed in, not baked in, for payments
```

- example 8. image layers for an API that serves room_2
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# room_2 is data, not a layer
```

- homework
```dockerfile
# 8a  why the lockfile is copied first
# 8b  localhost in this container is the container
# 8c  DATABASE_URL is passed in, not baked in, for rooms
```

- example 9. image layers for an API that serves vs_7
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# vs_7 is data, not a layer
```

- homework
```dockerfile
# 9a  why the lockfile is copied first
# 9b  localhost in this container is the container
# 9c  DATABASE_URL is passed in, not baked in, for vessels
```

- example 10. image layers for an API that serves sc_3
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# sc_3 is data, not a layer
```

- homework
```dockerfile
# 10a  why the lockfile is copied first
# 10b  localhost in this container is the container
# 10c  DATABASE_URL is passed in, not baked in, for scores
```

- example 11. image layers for an API that serves tm_2
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# tm_2 is data, not a layer
```

- homework
```dockerfile
# 11a  why the lockfile is copied first
# 11b  localhost in this container is the container
# 11c  DATABASE_URL is passed in, not baked in, for teams
```

- example 12. image layers for an API that serves up_6
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# up_6 is data, not a layer
```

- homework
```dockerfile
# 12a  why the lockfile is copied first
# 12b  localhost in this container is the container
# 12c  DATABASE_URL is passed in, not baked in, for uploads
```

- example 13. image layers for an API that serves st_1
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# st_1 is data, not a layer
```

- homework
```dockerfile
# 13a  why the lockfile is copied first
# 13b  localhost in this container is the container
# 13c  DATABASE_URL is passed in, not baked in, for standings
```

- example 14. image layers for an API that serves n_2
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# n_2 is data, not a layer
```

- homework
```dockerfile
# 14a  why the lockfile is copied first
# 14b  localhost in this container is the container
# 14c  DATABASE_URL is passed in, not baked in, for notices
```

- example 15. image layers for an API that serves b_3
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# b_3 is data, not a layer
```

- homework
```dockerfile
# 15a  why the lockfile is copied first
# 15b  localhost in this container is the container
# 15c  DATABASE_URL is passed in, not baked in, for brackets
```

- example 16. image layers for an API that serves se_1
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# se_1 is data, not a layer
```

- homework
```dockerfile
# 16a  why the lockfile is copied first
# 16b  localhost in this container is the container
# 16c  DATABASE_URL is passed in, not baked in, for sessions
```

- example 17. image layers for an API that serves q_1
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# q_1 is data, not a layer
```

- homework
```dockerfile
# 17a  why the lockfile is copied first
# 17b  localhost in this container is the container
# 17c  DATABASE_URL is passed in, not baked in, for queues
```

- example 18. image layers for an API that serves r_1
- copy the lockfile before the source so a code edit does not reinstall
- npm ci uses the lockfile
- the password is env at run time, not a line in the image

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
# r_1 is data, not a layer
```

- homework
```dockerfile
# 18a  why the lockfile is copied first
# 18b  localhost in this container is the container
# 18c  DATABASE_URL is passed in, not baked in, for roles
```

## chapter 5 Docker Compose

- Compose starts several containers and gives them a network
- the service name is the DNS name. the API reaches Postgres at `postgres`, not at localhost
- a volume keeps the database files when the container is replaced
- `depends_on` waits for the process to start. it does not wait for Postgres to accept connections. the app retries
- VMS and Bracket compose files include Redis. Anemi's does not need Redis

```yaml
services:
  api:
    build: .
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on:
      - postgres
  postgres:
    image: postgres:16
    volumes:
      - pgdata:/var/lib/postgresql/data
volumes:
  pgdata:
```

- the URL host is `postgres` because that is the service name
- the volume name `pgdata` is what survives `docker compose down` without `-v`

- homework of chapter 5
```yaml
# 5a  the host in DATABASE_URL, and why not localhost
# 5b  what we lose if we remove the volume
# 5c  which product's compose file has no Redis service
```

- example 1. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for pc_12 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row pc_12 lives in pgdata
```

- homework
```yaml
# 1a  host is postgres
# 1b  removing the volume drops pc_12
# 1c  Anemi compose has no Redis
```

- example 2. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for m_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row m_1 lives in pgdata
```

- homework
```yaml
# 2a  host is postgres
# 2b  removing the volume drops m_1
# 2c  Anemi compose has no Redis
```

- example 3. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for t_9 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row t_9 lives in pgdata
```

- homework
```yaml
# 3a  host is postgres
# 3b  removing the volume drops t_9
# 3c  Anemi compose has no Redis
```

- example 4. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for v_4 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row v_4 lives in pgdata
```

- homework
```yaml
# 4a  host is postgres
# 4b  removing the volume drops v_4
# 4c  Anemi compose has no Redis
```

- example 5. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for f_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row f_2 lives in pgdata
```

- homework
```yaml
# 5a  host is postgres
# 5b  removing the volume drops f_2
# 5c  Anemi compose has no Redis
```

- example 6. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for u_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row u_3 lives in pgdata
```

- homework
```yaml
# 6a  host is postgres
# 6b  removing the volume drops u_3
# 6c  Anemi compose has no Redis
```

- example 7. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for pay_8 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row pay_8 lives in pgdata
```

- homework
```yaml
# 7a  host is postgres
# 7b  removing the volume drops pay_8
# 7c  Anemi compose has no Redis
```

- example 8. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for room_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row room_2 lives in pgdata
```

- homework
```yaml
# 8a  host is postgres
# 8b  removing the volume drops room_2
# 8c  Anemi compose has no Redis
```

- example 9. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for vs_7 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row vs_7 lives in pgdata
```

- homework
```yaml
# 9a  host is postgres
# 9b  removing the volume drops vs_7
# 9c  Anemi compose has no Redis
```

- example 10. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for sc_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row sc_3 lives in pgdata
```

- homework
```yaml
# 10a  host is postgres
# 10b  removing the volume drops sc_3
# 10c  Anemi compose has no Redis
```

- example 11. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for tm_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row tm_2 lives in pgdata
```

- homework
```yaml
# 11a  host is postgres
# 11b  removing the volume drops tm_2
# 11c  Anemi compose has no Redis
```

- example 12. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for up_6 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row up_6 lives in pgdata
```

- homework
```yaml
# 12a  host is postgres
# 12b  removing the volume drops up_6
# 12c  Anemi compose has no Redis
```

- example 13. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for st_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row st_1 lives in pgdata
```

- homework
```yaml
# 13a  host is postgres
# 13b  removing the volume drops st_1
# 13c  Anemi compose has no Redis
```

- example 14. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for n_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row n_2 lives in pgdata
```

- homework
```yaml
# 14a  host is postgres
# 14b  removing the volume drops n_2
# 14c  Anemi compose has no Redis
```

- example 15. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for b_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row b_3 lives in pgdata
```

- homework
```yaml
# 15a  host is postgres
# 15b  removing the volume drops b_3
# 15c  Anemi compose has no Redis
```

- example 16. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for se_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row se_1 lives in pgdata
```

- homework
```yaml
# 16a  host is postgres
# 16b  removing the volume drops se_1
# 16c  Anemi compose has no Redis
```

- example 17. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for q_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row q_1 lives in pgdata
```

- homework
```yaml
# 17a  host is postgres
# 17b  removing the volume drops q_1
# 17c  Anemi compose has no Redis
```

- example 18. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for r_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row r_1 lives in pgdata
```

- homework
```yaml
# 18a  host is postgres
# 18b  removing the volume drops r_1
# 18c  Anemi compose has no Redis
```

- example 19. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for pc_12 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row pc_12 lives in pgdata
```

- homework
```yaml
# 19a  host is postgres
# 19b  removing the volume drops pc_12
# 19c  Anemi compose has no Redis
```

- example 20. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for m_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row m_1 lives in pgdata
```

- homework
```yaml
# 20a  host is postgres
# 20b  removing the volume drops m_1
# 20c  Anemi compose has no Redis
```

- example 21. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for t_9 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row t_9 lives in pgdata
```

- homework
```yaml
# 21a  host is postgres
# 21b  removing the volume drops t_9
# 21c  Anemi compose has no Redis
```

- example 22. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for v_4 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row v_4 lives in pgdata
```

- homework
```yaml
# 22a  host is postgres
# 22b  removing the volume drops v_4
# 22c  Anemi compose has no Redis
```

- example 23. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for f_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row f_2 lives in pgdata
```

- homework
```yaml
# 23a  host is postgres
# 23b  removing the volume drops f_2
# 23c  Anemi compose has no Redis
```

- example 24. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for u_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row u_3 lives in pgdata
```

- homework
```yaml
# 24a  host is postgres
# 24b  removing the volume drops u_3
# 24c  Anemi compose has no Redis
```

- example 25. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for pay_8 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row pay_8 lives in pgdata
```

- homework
```yaml
# 25a  host is postgres
# 25b  removing the volume drops pay_8
# 25c  Anemi compose has no Redis
```

- example 26. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for room_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row room_2 lives in pgdata
```

- homework
```yaml
# 26a  host is postgres
# 26b  removing the volume drops room_2
# 26c  Anemi compose has no Redis
```

- example 27. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for vs_7 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row vs_7 lives in pgdata
```

- homework
```yaml
# 27a  host is postgres
# 27b  removing the volume drops vs_7
# 27c  Anemi compose has no Redis
```

- example 28. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for sc_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row sc_3 lives in pgdata
```

- homework
```yaml
# 28a  host is postgres
# 28b  removing the volume drops sc_3
# 28c  Anemi compose has no Redis
```

- example 29. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for tm_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row tm_2 lives in pgdata
```

- homework
```yaml
# 29a  host is postgres
# 29b  removing the volume drops tm_2
# 29c  Anemi compose has no Redis
```

- example 30. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for up_6 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row up_6 lives in pgdata
```

- homework
```yaml
# 30a  host is postgres
# 30b  removing the volume drops up_6
# 30c  Anemi compose has no Redis
```

- example 31. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for st_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row st_1 lives in pgdata
```

- homework
```yaml
# 31a  host is postgres
# 31b  removing the volume drops st_1
# 31c  Anemi compose has no Redis
```

- example 32. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for n_2 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row n_2 lives in pgdata
```

- homework
```yaml
# 32a  host is postgres
# 32b  removing the volume drops n_2
# 32c  Anemi compose has no Redis
```

- example 33. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for b_3 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row b_3 lives in pgdata
```

- homework
```yaml
# 33a  host is postgres
# 33b  removing the volume drops b_3
# 33c  Anemi compose has no Redis
```

- example 34. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for se_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row se_1 lives in pgdata
```

- homework
```yaml
# 34a  host is postgres
# 34b  removing the volume drops se_1
# 34c  Anemi compose has no Redis
```

- example 35. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for q_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row q_1 lives in pgdata
```

- homework
```yaml
# 35a  host is postgres
# 35b  removing the volume drops q_1
# 35c  Anemi compose has no Redis
```

- example 36. Compose service names
- host in the URL is postgres, not localhost
- the volume keeps data for r_1 across a recreate
- depends_on does not wait until Postgres accepts connections
- Anemi's file does not need a Redis service

```yaml
services:
  api:
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on: [postgres]
  postgres:
    image: postgres:16
    volumes: ["pgdata:/var/lib/postgresql/data"]
volumes:
  pgdata: {}
# row r_1 lives in pgdata
```

- homework
```yaml
# 36a  host is postgres
# 36b  removing the volume drops r_1
# 36c  Anemi compose has no Redis
```

## chapter 6 Kubernetes and Helm

- we have not operated a Kubernetes cluster. the notes still name the parts
- a pod = one or more containers that share a network and are scheduled together
- a deployment = the desired number of pods, and how to replace them
- a service = a stable name and address in front of the pods
- an ingress = the HTTP front door, the role nginx plays for us today
- a configmap is configuration. a secret is a secret. both are mounted or injected as env
- Helm = a package of those YAML files, with values we fill in
- a chart is the package. a release is one install
- the idea we already use is the same: more than one process, a front door, env for config, a restart when it dies
- we do not draw pods on a diagram of the system we run today

```text
today: nginx -> node process managed by PM2 -> postgres
the kubernetes words: ingress -> service -> deployment -> pod
```

- a liveness probe restarts a stuck process. a readiness probe takes it out of the service until it can answer
- those map to "PM2 restarts it" and "nginx stops sending traffic to a dead upstream"

- homework of chapter 6
```text
# 6a  pod, deployment, service, in one line each
# 6b  the thing we run today that is closest to an ingress
# 6c  what we say if we are asked whether we operate a cluster
```

- example 1. words we can define, for a request pc_12
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
pc_12 is still a row in Postgres
```

- homework
```text
# 1a  one line each: pod, deployment, service
# 1b  our ingress today is nginx
# 1c  say we have not operated a cluster
```

- example 2. words we can define, for a request m_1
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
m_1 is still a row in Postgres
```

- homework
```text
# 2a  one line each: pod, deployment, service
# 2b  our ingress today is nginx
# 2c  say we have not operated a cluster
```

- example 3. words we can define, for a request t_9
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
t_9 is still a row in Postgres
```

- homework
```text
# 3a  one line each: pod, deployment, service
# 3b  our ingress today is nginx
# 3c  say we have not operated a cluster
```

- example 4. words we can define, for a request v_4
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
v_4 is still a row in Postgres
```

- homework
```text
# 4a  one line each: pod, deployment, service
# 4b  our ingress today is nginx
# 4c  say we have not operated a cluster
```

- example 5. words we can define, for a request f_2
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
f_2 is still a row in Postgres
```

- homework
```text
# 5a  one line each: pod, deployment, service
# 5b  our ingress today is nginx
# 5c  say we have not operated a cluster
```

- example 6. words we can define, for a request u_3
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
u_3 is still a row in Postgres
```

- homework
```text
# 6a  one line each: pod, deployment, service
# 6b  our ingress today is nginx
# 6c  say we have not operated a cluster
```

- example 7. words we can define, for a request pay_8
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
pay_8 is still a row in Postgres
```

- homework
```text
# 7a  one line each: pod, deployment, service
# 7b  our ingress today is nginx
# 7c  say we have not operated a cluster
```

- example 8. words we can define, for a request room_2
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
room_2 is still a row in Postgres
```

- homework
```text
# 8a  one line each: pod, deployment, service
# 8b  our ingress today is nginx
# 8c  say we have not operated a cluster
```

- example 9. words we can define, for a request vs_7
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
vs_7 is still a row in Postgres
```

- homework
```text
# 9a  one line each: pod, deployment, service
# 9b  our ingress today is nginx
# 9c  say we have not operated a cluster
```

- example 10. words we can define, for a request sc_3
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
sc_3 is still a row in Postgres
```

- homework
```text
# 10a  one line each: pod, deployment, service
# 10b  our ingress today is nginx
# 10c  say we have not operated a cluster
```

- example 11. words we can define, for a request tm_2
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
tm_2 is still a row in Postgres
```

- homework
```text
# 11a  one line each: pod, deployment, service
# 11b  our ingress today is nginx
# 11c  say we have not operated a cluster
```

- example 12. words we can define, for a request up_6
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
up_6 is still a row in Postgres
```

- homework
```text
# 12a  one line each: pod, deployment, service
# 12b  our ingress today is nginx
# 12c  say we have not operated a cluster
```

- example 13. words we can define, for a request st_1
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
st_1 is still a row in Postgres
```

- homework
```text
# 13a  one line each: pod, deployment, service
# 13b  our ingress today is nginx
# 13c  say we have not operated a cluster
```

- example 14. words we can define, for a request n_2
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
n_2 is still a row in Postgres
```

- homework
```text
# 14a  one line each: pod, deployment, service
# 14b  our ingress today is nginx
# 14c  say we have not operated a cluster
```

- example 15. words we can define, for a request b_3
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
b_3 is still a row in Postgres
```

- homework
```text
# 15a  one line each: pod, deployment, service
# 15b  our ingress today is nginx
# 15c  say we have not operated a cluster
```

- example 16. words we can define, for a request se_1
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
se_1 is still a row in Postgres
```

- homework
```text
# 16a  one line each: pod, deployment, service
# 16b  our ingress today is nginx
# 16c  say we have not operated a cluster
```

- example 17. words we can define, for a request q_1
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
q_1 is still a row in Postgres
```

- homework
```text
# 17a  one line each: pod, deployment, service
# 17b  our ingress today is nginx
# 17c  say we have not operated a cluster
```

- example 18. words we can define, for a request r_1
- we have not run a Kubernetes cluster
- pod, deployment, service, ingress
- today: nginx, PM2, Postgres
- a probe restarts or removes a process that does not answer

```text
today: nginx -> PM2 node -> postgres
words: ingress -> service -> deployment -> pod
r_1 is still a row in Postgres
```

- homework
```text
# 18a  one line each: pod, deployment, service
# 18b  our ingress today is nginx
# 18c  say we have not operated a cluster
```

## chapter 7 CI, GitHub Actions, and cloud

- CI = every push runs the tests. a red check is not merged
- CD = a green main can deploy. we still know which commit is on the server
- GitHub Actions is the runner we use. a workflow file in `.github/workflows` lists the steps
- a job checks out the repo, installs, and runs the test script
- a secret in the workflow comes from the repo settings, not from the file
- a cloud server is someone else's machine with an API. the nouns are compute, disk, network, and identity
- a VM is a computer. a managed database is Postgres we do not patch ourselves, and we still design backups
- a security group is a firewall. which ports, from where
- object storage is the blob store for video
- the bill follows CPU, disk, and egress
- we name the machine in front of us. we do not invent a list of AWS products we have not opened
- the picture's cloud line was under the play button. the ideas are the VM, the firewall, the disk, and the object store

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
```

- `npm test` is Vitest or node:test, whichever the repo uses
- the workflow does not print the database password

- homework of chapter 7
```yaml
# 7a  when this workflow runs
# 7b  the step that must fail the pull request if a test fails
# 7c  a cloud noun for "who may open port 443"
# 7d  why a public video without a cache shows up on a bill
```

- example 1. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change pc_12 is covered if the tests cover it
```

- homework
```yaml
# 1a  the workflow runs on a pull request
# 1b  a failed test blocks the merge
# 1c  a public video without a cache is an egress bill
# 1d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 2. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change m_1 is covered if the tests cover it
```

- homework
```yaml
# 2a  the workflow runs on a pull request
# 2b  a failed test blocks the merge
# 2c  a public video without a cache is an egress bill
# 2d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 3. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change t_9 is covered if the tests cover it
```

- homework
```yaml
# 3a  the workflow runs on a pull request
# 3b  a failed test blocks the merge
# 3c  a public video without a cache is an egress bill
# 3d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 4. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change v_4 is covered if the tests cover it
```

- homework
```yaml
# 4a  the workflow runs on a pull request
# 4b  a failed test blocks the merge
# 4c  a public video without a cache is an egress bill
# 4d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 5. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change f_2 is covered if the tests cover it
```

- homework
```yaml
# 5a  the workflow runs on a pull request
# 5b  a failed test blocks the merge
# 5c  a public video without a cache is an egress bill
# 5d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 6. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change u_3 is covered if the tests cover it
```

- homework
```yaml
# 6a  the workflow runs on a pull request
# 6b  a failed test blocks the merge
# 6c  a public video without a cache is an egress bill
# 6d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 7. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change pay_8 is covered if the tests cover it
```

- homework
```yaml
# 7a  the workflow runs on a pull request
# 7b  a failed test blocks the merge
# 7c  a public video without a cache is an egress bill
# 7d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 8. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change room_2 is covered if the tests cover it
```

- homework
```yaml
# 8a  the workflow runs on a pull request
# 8b  a failed test blocks the merge
# 8c  a public video without a cache is an egress bill
# 8d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 9. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change vs_7 is covered if the tests cover it
```

- homework
```yaml
# 9a  the workflow runs on a pull request
# 9b  a failed test blocks the merge
# 9c  a public video without a cache is an egress bill
# 9d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 10. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change sc_3 is covered if the tests cover it
```

- homework
```yaml
# 10a  the workflow runs on a pull request
# 10b  a failed test blocks the merge
# 10c  a public video without a cache is an egress bill
# 10d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 11. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change tm_2 is covered if the tests cover it
```

- homework
```yaml
# 11a  the workflow runs on a pull request
# 11b  a failed test blocks the merge
# 11c  a public video without a cache is an egress bill
# 11d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 12. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change up_6 is covered if the tests cover it
```

- homework
```yaml
# 12a  the workflow runs on a pull request
# 12b  a failed test blocks the merge
# 12c  a public video without a cache is an egress bill
# 12d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 13. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change st_1 is covered if the tests cover it
```

- homework
```yaml
# 13a  the workflow runs on a pull request
# 13b  a failed test blocks the merge
# 13c  a public video without a cache is an egress bill
# 13d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 14. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change n_2 is covered if the tests cover it
```

- homework
```yaml
# 14a  the workflow runs on a pull request
# 14b  a failed test blocks the merge
# 14c  a public video without a cache is an egress bill
# 14d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 15. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change b_3 is covered if the tests cover it
```

- homework
```yaml
# 15a  the workflow runs on a pull request
# 15b  a failed test blocks the merge
# 15c  a public video without a cache is an egress bill
# 15d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 16. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change se_1 is covered if the tests cover it
```

- homework
```yaml
# 16a  the workflow runs on a pull request
# 16b  a failed test blocks the merge
# 16c  a public video without a cache is an egress bill
# 16d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 17. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change q_1 is covered if the tests cover it
```

- homework
```yaml
# 17a  the workflow runs on a pull request
# 17b  a failed test blocks the merge
# 17c  a public video without a cache is an egress bill
# 17d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

- example 18. a workflow that tests before merge
- checkout, npm ci, npm test
- secrets come from settings, not the file
- a VM, a firewall, a disk, object storage
- name the machine we have. do not invent products we have not opened

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
# change r_1 is covered if the tests cover it
```

- homework
```yaml
# 18a  the workflow runs on a pull request
# 18b  a failed test blocks the merge
# 18c  a public video without a cache is an egress bill
# 18d  the cloud line on the picture is these nouns: VM, firewall, disk, object storage
```

## chapter 8 Terraform and Ansible

- Terraform = a file that describes infrastructure. we plan, then we apply
- the state file remembers what Terraform created. we do not edit the cloud by hand and also let Terraform own it, or they drift
- state often contains secrets. it is not a public file
- Ansible = SSH and a list of tasks that make a server match a description. install nginx, copy a unit file, restart
- Terraform is better at "create the VM and the disk". Ansible is better at "the packages and the config files on that VM"
- we may not have either in the current deploy. the deploy we have is Docker, nginx, PM2, and GitHub Actions
- the words still have to be precise

```hcl
resource "local_file" "example" {
  filename = "hello.txt"
  content  = "hello"
}
```

```yaml
- name: nginx is installed
  apt:
    name: nginx
    state: present
```

- `plan` shows the change. `apply` does it. we read the plan
- an Ansible task should be safe to run twice. install "present" is. a blind append to a file is not

- homework of chapter 8
```text
# 8a  what Terraform state remembers
# 8b  why we do not commit a state file full of secrets
# 8c  a task that is safe to run twice, and one that is not
# 8d  the deploy tools we have actually used
```

- example 1. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for pc_12
```

- homework
```text
# 1a  state is not a public file
# 1b  install nginx twice stays installed once
# 1c  tools we have used: Docker, nginx, PM2, Actions
```

- example 2. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for m_1
```

- homework
```text
# 2a  state is not a public file
# 2b  install nginx twice stays installed once
# 2c  tools we have used: Docker, nginx, PM2, Actions
```

- example 3. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for t_9
```

- homework
```text
# 3a  state is not a public file
# 3b  install nginx twice stays installed once
# 3c  tools we have used: Docker, nginx, PM2, Actions
```

- example 4. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for v_4
```

- homework
```text
# 4a  state is not a public file
# 4b  install nginx twice stays installed once
# 4c  tools we have used: Docker, nginx, PM2, Actions
```

- example 5. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for f_2
```

- homework
```text
# 5a  state is not a public file
# 5b  install nginx twice stays installed once
# 5c  tools we have used: Docker, nginx, PM2, Actions
```

- example 6. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for u_3
```

- homework
```text
# 6a  state is not a public file
# 6b  install nginx twice stays installed once
# 6c  tools we have used: Docker, nginx, PM2, Actions
```

- example 7. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for pay_8
```

- homework
```text
# 7a  state is not a public file
# 7b  install nginx twice stays installed once
# 7c  tools we have used: Docker, nginx, PM2, Actions
```

- example 8. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for room_2
```

- homework
```text
# 8a  state is not a public file
# 8b  install nginx twice stays installed once
# 8c  tools we have used: Docker, nginx, PM2, Actions
```

- example 9. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for vs_7
```

- homework
```text
# 9a  state is not a public file
# 9b  install nginx twice stays installed once
# 9c  tools we have used: Docker, nginx, PM2, Actions
```

- example 10. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for sc_3
```

- homework
```text
# 10a  state is not a public file
# 10b  install nginx twice stays installed once
# 10c  tools we have used: Docker, nginx, PM2, Actions
```

- example 11. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for tm_2
```

- homework
```text
# 11a  state is not a public file
# 11b  install nginx twice stays installed once
# 11c  tools we have used: Docker, nginx, PM2, Actions
```

- example 12. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for up_6
```

- homework
```text
# 12a  state is not a public file
# 12b  install nginx twice stays installed once
# 12c  tools we have used: Docker, nginx, PM2, Actions
```

- example 13. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for st_1
```

- homework
```text
# 13a  state is not a public file
# 13b  install nginx twice stays installed once
# 13c  tools we have used: Docker, nginx, PM2, Actions
```

- example 14. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for n_2
```

- homework
```text
# 14a  state is not a public file
# 14b  install nginx twice stays installed once
# 14c  tools we have used: Docker, nginx, PM2, Actions
```

- example 15. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for b_3
```

- homework
```text
# 15a  state is not a public file
# 15b  install nginx twice stays installed once
# 15c  tools we have used: Docker, nginx, PM2, Actions
```

- example 16. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for se_1
```

- homework
```text
# 16a  state is not a public file
# 16b  install nginx twice stays installed once
# 16c  tools we have used: Docker, nginx, PM2, Actions
```

- example 17. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for q_1
```

- homework
```text
# 17a  state is not a public file
# 17b  install nginx twice stays installed once
# 17c  tools we have used: Docker, nginx, PM2, Actions
```

- example 18. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for r_1
```

- homework
```text
# 18a  state is not a public file
# 18b  install nginx twice stays installed once
# 18c  tools we have used: Docker, nginx, PM2, Actions
```

- example 19. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for pc_12
```

- homework
```text
# 19a  state is not a public file
# 19b  install nginx twice stays installed once
# 19c  tools we have used: Docker, nginx, PM2, Actions
```

- example 20. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for m_1
```

- homework
```text
# 20a  state is not a public file
# 20b  install nginx twice stays installed once
# 20c  tools we have used: Docker, nginx, PM2, Actions
```

- example 21. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for t_9
```

- homework
```text
# 21a  state is not a public file
# 21b  install nginx twice stays installed once
# 21c  tools we have used: Docker, nginx, PM2, Actions
```

- example 22. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for v_4
```

- homework
```text
# 22a  state is not a public file
# 22b  install nginx twice stays installed once
# 22c  tools we have used: Docker, nginx, PM2, Actions
```

- example 23. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for f_2
```

- homework
```text
# 23a  state is not a public file
# 23b  install nginx twice stays installed once
# 23c  tools we have used: Docker, nginx, PM2, Actions
```

- example 24. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for u_3
```

- homework
```text
# 24a  state is not a public file
# 24b  install nginx twice stays installed once
# 24c  tools we have used: Docker, nginx, PM2, Actions
```

- example 25. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for pay_8
```

- homework
```text
# 25a  state is not a public file
# 25b  install nginx twice stays installed once
# 25c  tools we have used: Docker, nginx, PM2, Actions
```

- example 26. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for room_2
```

- homework
```text
# 26a  state is not a public file
# 26b  install nginx twice stays installed once
# 26c  tools we have used: Docker, nginx, PM2, Actions
```

- example 27. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for vs_7
```

- homework
```text
# 27a  state is not a public file
# 27b  install nginx twice stays installed once
# 27c  tools we have used: Docker, nginx, PM2, Actions
```

- example 28. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for sc_3
```

- homework
```text
# 28a  state is not a public file
# 28b  install nginx twice stays installed once
# 28c  tools we have used: Docker, nginx, PM2, Actions
```

- example 29. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for tm_2
```

- homework
```text
# 29a  state is not a public file
# 29b  install nginx twice stays installed once
# 29c  tools we have used: Docker, nginx, PM2, Actions
```

- example 30. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for up_6
```

- homework
```text
# 30a  state is not a public file
# 30b  install nginx twice stays installed once
# 30c  tools we have used: Docker, nginx, PM2, Actions
```

- example 31. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for st_1
```

- homework
```text
# 31a  state is not a public file
# 31b  install nginx twice stays installed once
# 31c  tools we have used: Docker, nginx, PM2, Actions
```

- example 32. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for n_2
```

- homework
```text
# 32a  state is not a public file
# 32b  install nginx twice stays installed once
# 32c  tools we have used: Docker, nginx, PM2, Actions
```

- example 33. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for b_3
```

- homework
```text
# 33a  state is not a public file
# 33b  install nginx twice stays installed once
# 33c  tools we have used: Docker, nginx, PM2, Actions
```

- example 34. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for se_1
```

- homework
```text
# 34a  state is not a public file
# 34b  install nginx twice stays installed once
# 34c  tools we have used: Docker, nginx, PM2, Actions
```

- example 35. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for q_1
```

- homework
```text
# 35a  state is not a public file
# 35b  install nginx twice stays installed once
# 35c  tools we have used: Docker, nginx, PM2, Actions
```

- example 36. plan versus a task we can run twice
- Terraform state remembers created objects and can hold secrets
- Ansible "present" is safe twice. a blind append is not
- the deploy we run is Docker, nginx, PM2, GitHub Actions

```text
terraform plan   # read it before apply
ansible: nginx state present
do not commit state for r_1
```

- homework
```text
# 36a  state is not a public file
# 36b  install nginx twice stays installed once
# 36c  tools we have used: Docker, nginx, PM2, Actions
```

## chapter 9 nginx and load balancers

- nginx is the front door. TLS, the static build, and `/api` proxied to Nest
- Caddy can do the same with automatic certificates. Anemi's notes include Caddy
- a load balancer spreads connections across healthy upstreams
- one upstream is still a front door. two upstreams are a balancer
- `proxy_pass` is the hop to Node
- we send the original host and the client IP if the app needs them
- WebSocket needs the upgrade headers
- a 502 means nginx could not get a valid answer from upstream

```nginx
server {
  listen 443 ssl;
  location /api/ {
    proxy_pass http://127.0.0.1:3000;
    proxy_set_header Host $host;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
  }
  location / {
    root /var/www/app;
    try_files $uri /index.html;
  }
}
```

- `try_files` sends unknown paths to the single-page app
- the API location is a proxy. the page location is files
- least-connections versus round robin matters when some requests are long sockets and some are quick reads

- homework of chapter 9
```nginx
# 9a  which location is files, which is the API
# 9b  what a 502 points at
# 9c  the headers a WebSocket upgrade needs
```

- example 1. nginx location for port-calls
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for pc_12

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 1a  files versus proxy
# 1b  502 points at the upstream of pc_12
# 1c  Upgrade and Connection for the socket
```

- example 2. nginx location for matches
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for m_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 2a  files versus proxy
# 2b  502 points at the upstream of m_1
# 2c  Upgrade and Connection for the socket
```

- example 3. nginx location for tournaments
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for t_9

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 3a  files versus proxy
# 3b  502 points at the upstream of t_9
# 3c  Upgrade and Connection for the socket
```

- example 4. nginx location for videos
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for v_4

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 4a  files versus proxy
# 4b  502 points at the upstream of v_4
# 4c  Upgrade and Connection for the socket
```

- example 5. nginx location for facts
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for f_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 5a  files versus proxy
# 5b  502 points at the upstream of f_2
# 5c  Upgrade and Connection for the socket
```

- example 6. nginx location for users
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for u_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 6a  files versus proxy
# 6b  502 points at the upstream of u_3
# 6c  Upgrade and Connection for the socket
```

- example 7. nginx location for payments
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for pay_8

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 7a  files versus proxy
# 7b  502 points at the upstream of pay_8
# 7c  Upgrade and Connection for the socket
```

- example 8. nginx location for rooms
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for room_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 8a  files versus proxy
# 8b  502 points at the upstream of room_2
# 8c  Upgrade and Connection for the socket
```

- example 9. nginx location for vessels
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for vs_7

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 9a  files versus proxy
# 9b  502 points at the upstream of vs_7
# 9c  Upgrade and Connection for the socket
```

- example 10. nginx location for scores
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for sc_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 10a  files versus proxy
# 10b  502 points at the upstream of sc_3
# 10c  Upgrade and Connection for the socket
```

- example 11. nginx location for teams
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for tm_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 11a  files versus proxy
# 11b  502 points at the upstream of tm_2
# 11c  Upgrade and Connection for the socket
```

- example 12. nginx location for uploads
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for up_6

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 12a  files versus proxy
# 12b  502 points at the upstream of up_6
# 12c  Upgrade and Connection for the socket
```

- example 13. nginx location for standings
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for st_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 13a  files versus proxy
# 13b  502 points at the upstream of st_1
# 13c  Upgrade and Connection for the socket
```

- example 14. nginx location for notices
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for n_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 14a  files versus proxy
# 14b  502 points at the upstream of n_2
# 14c  Upgrade and Connection for the socket
```

- example 15. nginx location for brackets
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for b_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 15a  files versus proxy
# 15b  502 points at the upstream of b_3
# 15c  Upgrade and Connection for the socket
```

- example 16. nginx location for sessions
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for se_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 16a  files versus proxy
# 16b  502 points at the upstream of se_1
# 16c  Upgrade and Connection for the socket
```

- example 17. nginx location for queues
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for q_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 17a  files versus proxy
# 17b  502 points at the upstream of q_1
# 17c  Upgrade and Connection for the socket
```

- example 18. nginx location for roles
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for r_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 18a  files versus proxy
# 18b  502 points at the upstream of r_1
# 18c  Upgrade and Connection for the socket
```

- example 19. nginx location for port-calls
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for pc_12

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 19a  files versus proxy
# 19b  502 points at the upstream of pc_12
# 19c  Upgrade and Connection for the socket
```

- example 20. nginx location for matches
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for m_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 20a  files versus proxy
# 20b  502 points at the upstream of m_1
# 20c  Upgrade and Connection for the socket
```

- example 21. nginx location for tournaments
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for t_9

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 21a  files versus proxy
# 21b  502 points at the upstream of t_9
# 21c  Upgrade and Connection for the socket
```

- example 22. nginx location for videos
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for v_4

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 22a  files versus proxy
# 22b  502 points at the upstream of v_4
# 22c  Upgrade and Connection for the socket
```

- example 23. nginx location for facts
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for f_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 23a  files versus proxy
# 23b  502 points at the upstream of f_2
# 23c  Upgrade and Connection for the socket
```

- example 24. nginx location for users
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for u_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 24a  files versus proxy
# 24b  502 points at the upstream of u_3
# 24c  Upgrade and Connection for the socket
```

- example 25. nginx location for payments
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for pay_8

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 25a  files versus proxy
# 25b  502 points at the upstream of pay_8
# 25c  Upgrade and Connection for the socket
```

- example 26. nginx location for rooms
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for room_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 26a  files versus proxy
# 26b  502 points at the upstream of room_2
# 26c  Upgrade and Connection for the socket
```

- example 27. nginx location for vessels
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for vs_7

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 27a  files versus proxy
# 27b  502 points at the upstream of vs_7
# 27c  Upgrade and Connection for the socket
```

- example 28. nginx location for scores
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for sc_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 28a  files versus proxy
# 28b  502 points at the upstream of sc_3
# 28c  Upgrade and Connection for the socket
```

- example 29. nginx location for teams
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for tm_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 29a  files versus proxy
# 29b  502 points at the upstream of tm_2
# 29c  Upgrade and Connection for the socket
```

- example 30. nginx location for uploads
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for up_6

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 30a  files versus proxy
# 30b  502 points at the upstream of up_6
# 30c  Upgrade and Connection for the socket
```

- example 31. nginx location for standings
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for st_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 31a  files versus proxy
# 31b  502 points at the upstream of st_1
# 31c  Upgrade and Connection for the socket
```

- example 32. nginx location for notices
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for n_2

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 32a  files versus proxy
# 32b  502 points at the upstream of n_2
# 32c  Upgrade and Connection for the socket
```

- example 33. nginx location for brackets
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for b_3

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 33a  files versus proxy
# 33b  502 points at the upstream of b_3
# 33c  Upgrade and Connection for the socket
```

- example 34. nginx location for sessions
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for se_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 34a  files versus proxy
# 34b  502 points at the upstream of se_1
# 34c  Upgrade and Connection for the socket
```

- example 35. nginx location for queues
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for q_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 35a  files versus proxy
# 35b  502 points at the upstream of q_1
# 35c  Upgrade and Connection for the socket
```

- example 36. nginx location for roles
- /api proxies. / is files
- upgrade headers for a socket
- 502 means the upstream did not answer for r_1

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
location / {
  try_files $uri /index.html;
}
```

- homework
```nginx
# 36a  files versus proxy
# 36b  502 points at the upstream of r_1
# 36c  Upgrade and Connection for the socket
```

## chapter 10 Prometheus, Grafana, and ELK

- Prometheus scrapes a metrics URL on an interval
- a counter only goes up. requests total. a gauge can go down. queue depth, memory
- a histogram is for duration. we can ask for a percentile later
- Grafana draws the Prometheus data
- a useful board is HTTP duration and queue depth, not a chart nobody opens
- ELK = Elasticsearch, Logstash or an agent, and Kibana. logs go in, we search them
- we may ship logs to a file and to Sentry for exceptions. ELK is the search stack when the files are not enough
- a log line has a request id. it does not have a password or a token
- Sentry is the exception with a release id. Prometheus is the number over time. they answer different questions

```text
http_requests_total{route="/port-calls",status="500"}
queue_depth{name="laytime"}
```

- a 500 rate and a rising queue depth are the two pictures that page someone
- a log without a request id cannot be tied to the metric spike

- homework of chapter 10
```text
# 10a  counter or gauge: queue depth
# 10b  counter or gauge: requests total
# 10c  what Sentry has that Prometheus does not
# 10d  two fields that never go in the log line
```

- example 1. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for pc_12 has a request id and not a token

```text
http_requests_total{route="/port-calls",status="500"}
queue_depth{name="laytime"}
log requestId and pc_12
do not log the refresh token
```

- homework
```text
# 1a  queue depth is a gauge
# 1b  requests total is a counter
# 1c  Sentry names the release. Prometheus does not replace that
```

- example 2. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for m_1 has a request id and not a token

```text
http_requests_total{route="/matches",status="500"}
queue_depth{name="laytime"}
log requestId and m_1
do not log the refresh token
```

- homework
```text
# 2a  queue depth is a gauge
# 2b  requests total is a counter
# 2c  Sentry names the release. Prometheus does not replace that
```

- example 3. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for t_9 has a request id and not a token

```text
http_requests_total{route="/tournaments",status="500"}
queue_depth{name="laytime"}
log requestId and t_9
do not log the refresh token
```

- homework
```text
# 3a  queue depth is a gauge
# 3b  requests total is a counter
# 3c  Sentry names the release. Prometheus does not replace that
```

- example 4. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for v_4 has a request id and not a token

```text
http_requests_total{route="/videos",status="500"}
queue_depth{name="laytime"}
log requestId and v_4
do not log the refresh token
```

- homework
```text
# 4a  queue depth is a gauge
# 4b  requests total is a counter
# 4c  Sentry names the release. Prometheus does not replace that
```

- example 5. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for f_2 has a request id and not a token

```text
http_requests_total{route="/facts",status="500"}
queue_depth{name="laytime"}
log requestId and f_2
do not log the refresh token
```

- homework
```text
# 5a  queue depth is a gauge
# 5b  requests total is a counter
# 5c  Sentry names the release. Prometheus does not replace that
```

- example 6. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for u_3 has a request id and not a token

```text
http_requests_total{route="/users",status="500"}
queue_depth{name="laytime"}
log requestId and u_3
do not log the refresh token
```

- homework
```text
# 6a  queue depth is a gauge
# 6b  requests total is a counter
# 6c  Sentry names the release. Prometheus does not replace that
```

- example 7. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for pay_8 has a request id and not a token

```text
http_requests_total{route="/payments",status="500"}
queue_depth{name="laytime"}
log requestId and pay_8
do not log the refresh token
```

- homework
```text
# 7a  queue depth is a gauge
# 7b  requests total is a counter
# 7c  Sentry names the release. Prometheus does not replace that
```

- example 8. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for room_2 has a request id and not a token

```text
http_requests_total{route="/rooms",status="500"}
queue_depth{name="laytime"}
log requestId and room_2
do not log the refresh token
```

- homework
```text
# 8a  queue depth is a gauge
# 8b  requests total is a counter
# 8c  Sentry names the release. Prometheus does not replace that
```

- example 9. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for vs_7 has a request id and not a token

```text
http_requests_total{route="/vessels",status="500"}
queue_depth{name="laytime"}
log requestId and vs_7
do not log the refresh token
```

- homework
```text
# 9a  queue depth is a gauge
# 9b  requests total is a counter
# 9c  Sentry names the release. Prometheus does not replace that
```

- example 10. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for sc_3 has a request id and not a token

```text
http_requests_total{route="/scores",status="500"}
queue_depth{name="laytime"}
log requestId and sc_3
do not log the refresh token
```

- homework
```text
# 10a  queue depth is a gauge
# 10b  requests total is a counter
# 10c  Sentry names the release. Prometheus does not replace that
```

- example 11. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for tm_2 has a request id and not a token

```text
http_requests_total{route="/teams",status="500"}
queue_depth{name="laytime"}
log requestId and tm_2
do not log the refresh token
```

- homework
```text
# 11a  queue depth is a gauge
# 11b  requests total is a counter
# 11c  Sentry names the release. Prometheus does not replace that
```

- example 12. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for up_6 has a request id and not a token

```text
http_requests_total{route="/uploads",status="500"}
queue_depth{name="laytime"}
log requestId and up_6
do not log the refresh token
```

- homework
```text
# 12a  queue depth is a gauge
# 12b  requests total is a counter
# 12c  Sentry names the release. Prometheus does not replace that
```

- example 13. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for st_1 has a request id and not a token

```text
http_requests_total{route="/standings",status="500"}
queue_depth{name="laytime"}
log requestId and st_1
do not log the refresh token
```

- homework
```text
# 13a  queue depth is a gauge
# 13b  requests total is a counter
# 13c  Sentry names the release. Prometheus does not replace that
```

- example 14. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for n_2 has a request id and not a token

```text
http_requests_total{route="/notices",status="500"}
queue_depth{name="laytime"}
log requestId and n_2
do not log the refresh token
```

- homework
```text
# 14a  queue depth is a gauge
# 14b  requests total is a counter
# 14c  Sentry names the release. Prometheus does not replace that
```

- example 15. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for b_3 has a request id and not a token

```text
http_requests_total{route="/brackets",status="500"}
queue_depth{name="laytime"}
log requestId and b_3
do not log the refresh token
```

- homework
```text
# 15a  queue depth is a gauge
# 15b  requests total is a counter
# 15c  Sentry names the release. Prometheus does not replace that
```

- example 16. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for se_1 has a request id and not a token

```text
http_requests_total{route="/sessions",status="500"}
queue_depth{name="laytime"}
log requestId and se_1
do not log the refresh token
```

- homework
```text
# 16a  queue depth is a gauge
# 16b  requests total is a counter
# 16c  Sentry names the release. Prometheus does not replace that
```

- example 17. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for q_1 has a request id and not a token

```text
http_requests_total{route="/queues",status="500"}
queue_depth{name="laytime"}
log requestId and q_1
do not log the refresh token
```

- homework
```text
# 17a  queue depth is a gauge
# 17b  requests total is a counter
# 17c  Sentry names the release. Prometheus does not replace that
```

- example 18. one counter and one gauge
- requests only go up. queue depth goes up and down
- Grafana draws them. Sentry holds the exception and the release
- the log line for r_1 has a request id and not a token

```text
http_requests_total{route="/roles",status="500"}
queue_depth{name="laytime"}
log requestId and r_1
do not log the refresh token
```

- homework
```text
# 18a  queue depth is a gauge
# 18b  requests total is a counter
# 18c  Sentry names the release. Prometheus does not replace that
```

## chapter 11 Blue-green, autoscaling, and secrets

- blue-green = two copies of the app. one is live. we deploy the other, test it, then move the front door
- if the new copy is bad, the front door moves back
- a database migration has to work on both copies during the switch, or we migrate in a way the old code still understands
- rolling deploy = replace one process at a time. PM2 and a second upstream can do a small version of this
- autoscaling = add or remove machines from a metric. CPU, request count, queue depth
- scale the thing that is busy. API CPU is not a reason to add Postgres replicas by magic
- a scale-in that kills a worker mid-job needs the job to be retryable
- a secret = a password, a token, a key. it lives in the environment or a secret store, not in git
- the app reads `process.env`. the file `.env` is local and ignored
- rotate a secret by adding the new one, deploying, then removing the old one. a JWT signing key needs a moment where both verify

```text
blue: live, old release
green: new release, not in the upstream yet
test green
point nginx at green
keep blue until the graphs look normal
```

- we have shipped nginx, PM2, Docker, and GitHub Actions. blue-green is the pattern. a second upstream is the small version
- autoscaling on queue depth fits the laytime worker. autoscaling the API does not fix a slow query

- homework of chapter 11
```text
# 11a  what has to be true of a migration during blue-green
# 11b  a metric that should add a worker, not an API process
# 11c  where a database password lives, and where it does not
# 11d  why a signing-key rotation has an overlap
```

- example 1. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands pc_12
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 1a  both copies tolerate the migration
# 1b  queue depth adds a worker
# 1c  a signing key overlap lets old tokens verify during rotation
```

- example 2. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands m_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 2a  both copies tolerate the migration
# 2b  queue depth adds a worker
# 2c  a signing key overlap lets old tokens verify during rotation
```

- example 3. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands t_9
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 3a  both copies tolerate the migration
# 3b  queue depth adds a worker
# 3c  a signing key overlap lets old tokens verify during rotation
```

- example 4. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands v_4
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 4a  both copies tolerate the migration
# 4b  queue depth adds a worker
# 4c  a signing key overlap lets old tokens verify during rotation
```

- example 5. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands f_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 5a  both copies tolerate the migration
# 5b  queue depth adds a worker
# 5c  a signing key overlap lets old tokens verify during rotation
```

- example 6. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands u_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 6a  both copies tolerate the migration
# 6b  queue depth adds a worker
# 6c  a signing key overlap lets old tokens verify during rotation
```

- example 7. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands pay_8
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 7a  both copies tolerate the migration
# 7b  queue depth adds a worker
# 7c  a signing key overlap lets old tokens verify during rotation
```

- example 8. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands room_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 8a  both copies tolerate the migration
# 8b  queue depth adds a worker
# 8c  a signing key overlap lets old tokens verify during rotation
```

- example 9. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands vs_7
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 9a  both copies tolerate the migration
# 9b  queue depth adds a worker
# 9c  a signing key overlap lets old tokens verify during rotation
```

- example 10. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands sc_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 10a  both copies tolerate the migration
# 10b  queue depth adds a worker
# 10c  a signing key overlap lets old tokens verify during rotation
```

- example 11. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands tm_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 11a  both copies tolerate the migration
# 11b  queue depth adds a worker
# 11c  a signing key overlap lets old tokens verify during rotation
```

- example 12. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands up_6
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 12a  both copies tolerate the migration
# 12b  queue depth adds a worker
# 12c  a signing key overlap lets old tokens verify during rotation
```

- example 13. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands st_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 13a  both copies tolerate the migration
# 13b  queue depth adds a worker
# 13c  a signing key overlap lets old tokens verify during rotation
```

- example 14. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands n_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 14a  both copies tolerate the migration
# 14b  queue depth adds a worker
# 14c  a signing key overlap lets old tokens verify during rotation
```

- example 15. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands b_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 15a  both copies tolerate the migration
# 15b  queue depth adds a worker
# 15c  a signing key overlap lets old tokens verify during rotation
```

- example 16. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands se_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 16a  both copies tolerate the migration
# 16b  queue depth adds a worker
# 16c  a signing key overlap lets old tokens verify during rotation
```

- example 17. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands q_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 17a  both copies tolerate the migration
# 17b  queue depth adds a worker
# 17c  a signing key overlap lets old tokens verify during rotation
```

- example 18. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands r_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 18a  both copies tolerate the migration
# 18b  queue depth adds a worker
# 18c  a signing key overlap lets old tokens verify during rotation
```

- example 19. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands pc_12
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 19a  both copies tolerate the migration
# 19b  queue depth adds a worker
# 19c  a signing key overlap lets old tokens verify during rotation
```

- example 20. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands m_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 20a  both copies tolerate the migration
# 20b  queue depth adds a worker
# 20c  a signing key overlap lets old tokens verify during rotation
```

- example 21. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands t_9
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 21a  both copies tolerate the migration
# 21b  queue depth adds a worker
# 21c  a signing key overlap lets old tokens verify during rotation
```

- example 22. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands v_4
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 22a  both copies tolerate the migration
# 22b  queue depth adds a worker
# 22c  a signing key overlap lets old tokens verify during rotation
```

- example 23. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands f_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 23a  both copies tolerate the migration
# 23b  queue depth adds a worker
# 23c  a signing key overlap lets old tokens verify during rotation
```

- example 24. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands u_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 24a  both copies tolerate the migration
# 24b  queue depth adds a worker
# 24c  a signing key overlap lets old tokens verify during rotation
```

- example 25. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands pay_8
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 25a  both copies tolerate the migration
# 25b  queue depth adds a worker
# 25c  a signing key overlap lets old tokens verify during rotation
```

- example 26. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands room_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 26a  both copies tolerate the migration
# 26b  queue depth adds a worker
# 26c  a signing key overlap lets old tokens verify during rotation
```

- example 27. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands vs_7
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 27a  both copies tolerate the migration
# 27b  queue depth adds a worker
# 27c  a signing key overlap lets old tokens verify during rotation
```

- example 28. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands sc_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 28a  both copies tolerate the migration
# 28b  queue depth adds a worker
# 28c  a signing key overlap lets old tokens verify during rotation
```

- example 29. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands tm_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 29a  both copies tolerate the migration
# 29b  queue depth adds a worker
# 29c  a signing key overlap lets old tokens verify during rotation
```

- example 30. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands up_6
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 30a  both copies tolerate the migration
# 30b  queue depth adds a worker
# 30c  a signing key overlap lets old tokens verify during rotation
```

- example 31. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands st_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 31a  both copies tolerate the migration
# 31b  queue depth adds a worker
# 31c  a signing key overlap lets old tokens verify during rotation
```

- example 32. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands n_2
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 32a  both copies tolerate the migration
# 32b  queue depth adds a worker
# 32c  a signing key overlap lets old tokens verify during rotation
```

- example 33. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands b_3
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 33a  both copies tolerate the migration
# 33b  queue depth adds a worker
# 33c  a signing key overlap lets old tokens verify during rotation
```

- example 34. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands se_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 34a  both copies tolerate the migration
# 34b  queue depth adds a worker
# 34c  a signing key overlap lets old tokens verify during rotation
```

- example 35. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands q_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 35a  both copies tolerate the migration
# 35b  queue depth adds a worker
# 35c  a signing key overlap lets old tokens verify during rotation
```

- example 36. two copies, then secrets
- blue is live. green is the new build. the door moves after a check
- a migration must still make sense to the old copy during the move
- scale a worker on queue depth, not because a query is slow
- the password is in the environment. rotation overlaps verify keys

```text
blue live
green has the build that understands r_1
test green
point nginx at green
secret from env, not from git
```

- homework
```text
# 36a  both copies tolerate the migration
# 36b  queue depth adds a worker
# 36c  a signing key overlap lets old tokens verify during rotation
```

## chapter 12 A deploy we can walk

- a pull request runs GitHub Actions
- merge to main builds an image or a Node build
- the server pulls it. PM2 reloads the process
- nginx keeps the public port
- Postgres stays up. we run a migration as its own step, before the new code expects the column
- Sentry gets the release id so an exception names the deploy
- Anemi's box may be Caddy instead of nginx. the hop is the same idea

```text
pull request -> tests
main -> build
server -> migrate -> reload process -> watch errors and latency
```

- rollback is the previous image and, if the migration was backward compatible, the previous process
- a migration that deletes a column is not in the same minute as the code that stops writing it. stop writing first, deploy, then delete

- homework of chapter 12
```text
# 12a  the order: migrate, or reload, and why
# 12b  what we watch for ten minutes after
# 12c  the tools in this path we have actually run
# 12d  Anemi's front door if it is not nginx
```

- example 1. order for a release that includes pc_12
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for port-calls
Caddy can be the door on Anemi
```

- homework
```text
# 1a  migrate before the new code expects the column
# 1b  watch latency and errors after pc_12 is deployed
# 1c  do not drop a column in the same minute the old code still writes it
```

- example 2. order for a release that includes m_1
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for matches
Caddy can be the door on Anemi
```

- homework
```text
# 2a  migrate before the new code expects the column
# 2b  watch latency and errors after m_1 is deployed
# 2c  do not drop a column in the same minute the old code still writes it
```

- example 3. order for a release that includes t_9
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for tournaments
Caddy can be the door on Anemi
```

- homework
```text
# 3a  migrate before the new code expects the column
# 3b  watch latency and errors after t_9 is deployed
# 3c  do not drop a column in the same minute the old code still writes it
```

- example 4. order for a release that includes v_4
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for videos
Caddy can be the door on Anemi
```

- homework
```text
# 4a  migrate before the new code expects the column
# 4b  watch latency and errors after v_4 is deployed
# 4c  do not drop a column in the same minute the old code still writes it
```

- example 5. order for a release that includes f_2
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for facts
Caddy can be the door on Anemi
```

- homework
```text
# 5a  migrate before the new code expects the column
# 5b  watch latency and errors after f_2 is deployed
# 5c  do not drop a column in the same minute the old code still writes it
```

- example 6. order for a release that includes u_3
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for users
Caddy can be the door on Anemi
```

- homework
```text
# 6a  migrate before the new code expects the column
# 6b  watch latency and errors after u_3 is deployed
# 6c  do not drop a column in the same minute the old code still writes it
```

- example 7. order for a release that includes pay_8
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for payments
Caddy can be the door on Anemi
```

- homework
```text
# 7a  migrate before the new code expects the column
# 7b  watch latency and errors after pay_8 is deployed
# 7c  do not drop a column in the same minute the old code still writes it
```

- example 8. order for a release that includes room_2
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for rooms
Caddy can be the door on Anemi
```

- homework
```text
# 8a  migrate before the new code expects the column
# 8b  watch latency and errors after room_2 is deployed
# 8c  do not drop a column in the same minute the old code still writes it
```

- example 9. order for a release that includes vs_7
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for vessels
Caddy can be the door on Anemi
```

- homework
```text
# 9a  migrate before the new code expects the column
# 9b  watch latency and errors after vs_7 is deployed
# 9c  do not drop a column in the same minute the old code still writes it
```

- example 10. order for a release that includes sc_3
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for scores
Caddy can be the door on Anemi
```

- homework
```text
# 10a  migrate before the new code expects the column
# 10b  watch latency and errors after sc_3 is deployed
# 10c  do not drop a column in the same minute the old code still writes it
```

- example 11. order for a release that includes tm_2
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for teams
Caddy can be the door on Anemi
```

- homework
```text
# 11a  migrate before the new code expects the column
# 11b  watch latency and errors after tm_2 is deployed
# 11c  do not drop a column in the same minute the old code still writes it
```

- example 12. order for a release that includes up_6
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for uploads
Caddy can be the door on Anemi
```

- homework
```text
# 12a  migrate before the new code expects the column
# 12b  watch latency and errors after up_6 is deployed
# 12c  do not drop a column in the same minute the old code still writes it
```

- example 13. order for a release that includes st_1
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for standings
Caddy can be the door on Anemi
```

- homework
```text
# 13a  migrate before the new code expects the column
# 13b  watch latency and errors after st_1 is deployed
# 13c  do not drop a column in the same minute the old code still writes it
```

- example 14. order for a release that includes n_2
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for notices
Caddy can be the door on Anemi
```

- homework
```text
# 14a  migrate before the new code expects the column
# 14b  watch latency and errors after n_2 is deployed
# 14c  do not drop a column in the same minute the old code still writes it
```

- example 15. order for a release that includes b_3
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for brackets
Caddy can be the door on Anemi
```

- homework
```text
# 15a  migrate before the new code expects the column
# 15b  watch latency and errors after b_3 is deployed
# 15c  do not drop a column in the same minute the old code still writes it
```

- example 16. order for a release that includes se_1
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for sessions
Caddy can be the door on Anemi
```

- homework
```text
# 16a  migrate before the new code expects the column
# 16b  watch latency and errors after se_1 is deployed
# 16c  do not drop a column in the same minute the old code still writes it
```

- example 17. order for a release that includes q_1
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for queues
Caddy can be the door on Anemi
```

- homework
```text
# 17a  migrate before the new code expects the column
# 17b  watch latency and errors after q_1 is deployed
# 17c  do not drop a column in the same minute the old code still writes it
```

- example 18. order for a release that includes r_1
- tests, build, migrate, reload, watch
- stop writing a column before you drop it
- rollback is the previous build if the migration was compatible

```text
pull request tests
main build
migrate
reload PM2
watch errors for roles
Caddy can be the door on Anemi
```

- homework
```text
# 18a  migrate before the new code expects the column
# 18b  watch latency and errors after r_1 is deployed
# 18c  do not drop a column in the same minute the old code still writes it
```
