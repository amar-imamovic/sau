# Hack The Box - Easy - Sau

## Enumeration

- Command ( Host ): sudo nmap 10.129.229.26 -sT -sV -sC -p- -O -oN nmap-initial-scan.txt

## Which is the highest open TCP port on the target machine?

- Answer: 55555

## What is the name of the open source software that the application on 55555 is "powered by"?

- Answer: request-baskets

## What is the version of request-baskets running on Sau?

- Answer: 1.2.1

## What is the 2023 CVE ID for a Server-Side Request Forgery (SSRF) in this version of request-baskets?

- Answer: CVE-2023-27163

## What is the name of the software that the application running on port 80 is "powered by"?

- Exploit: https://github.com/Khalidhaimur/exploit-request-baskets-1.2.1

- Answer: Maltrail

## There is an unauthenticated command injection vulnerability in MailTrail v0.53. What is the relative path on the webserver targeted by this exploit?

- Exploit: https://github.com/spookier/Maltrail-v0.53-Exploit

- Answer: /login

## What system user is the Mailtrack application running as on Sau?

- Answer: puma

## Submit the flag located in the puma user's home directory.

- Answer: f382977b4d14d47a5cc2d2f71d0d92b2

## What is the full path to the binary (without arguments) the puma user can run as root on Sau?

- Answer: /usr/bin/systemctl

## What is the full version string for the instance of systemd installed on Sau?

- Answer: systemd 245 (245.4-4ubuntu3.22)

## What is the 2023 CVE ID for a local privilege escalation vulnerability in this version of systemd?

- Answer: CVE-2023-26604

## Submit the flag located in the root user's home directory.

- Article: https://www.sentinelone.com/vulnerability-database/cve-2023-26604/

- Command ( TARGET ): sudo systemctl stauts trail.service

- Command ( TARGET ): !sh

- Answer: 02a3c9489471164dc953a9666edaa24d
