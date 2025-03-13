# Домашнее задание к занятию «Уязвимости и атаки на информационные системы» - `Станик Александр`

### Задание 1
Были найдены следующие открытые порты со службами:

21/tcp    open  ftp         vsftpd 2.3.4 [ссылка на уязвимость](https://www.exploit-db.com/exploits/49757)  
22/tcp    open  ssh         OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)  
23/tcp    open  telnet      Linux telnetd  
25/tcp    open  smtp        Postfix smtpd [ссылка на уязвимость](https://www.exploit-db.com/exploits/48185)  
53/tcp    open  domain      ISC BIND 9.4.2 [ссылка на уязвимость](https://www.exploit-db.com/exploits/37721)  
80/tcp    open  http        Apache httpd 2.2.8 ((Ubuntu) DAV/2)  
111/tcp   open  rpcbind     2 (RPC #100000)  
139/tcp   open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: WORKGROUP) [ссылка на уязвимость](https://www.exploit-db.com/exploits/42060)  
445/tcp   open  netbios-ssn Samba smbd 3.0.20-Debian (workgroup: WORKGROUP) [ссылка на уязвимость](https://www.exploit-db.com/exploits/42060)  
512/tcp   open  exec        netkit-rsh rexecd  
513/tcp   open  login       OpenBSD or Solaris rlogind  
514/tcp   open  shell       Netkit rshd  
1099/tcp  open  java-rmi    GNU Classpath grmiregistry  
1524/tcp  open  bindshell   Metasploitable root shell  
2049/tcp  open  nfs         2-4 (RPC #100003)  
2121/tcp  open  ftp         ProFTPD 1.3.1  
3306/tcp  open  mysql       MySQL 5.0.51a-3ubuntu5  
3632/tcp  open  distccd     distccd v1 ((GNU) 4.2.4 (Ubuntu 4.2.4-1ubuntu4))  
5432/tcp  open  postgresql  PostgreSQL DB 8.3.0 - 8.3.7  
5900/tcp  open  vnc         VNC (protocol 3.3)  
6000/tcp  open  X11         (access denied)  
6667/tcp  open  irc         UnrealIRCd  
6697/tcp  open  irc         UnrealIRCd  
8009/tcp  open  ajp13       Apache Jserv (Protocol v1.3)  
8180/tcp  open  http        Apache Tomcat/Coyote JSP engine 1.1  
8787/tcp  open  drb         Ruby DRb RMI (Ruby 1.8; path /usr/lib/ruby/1.8/drb)  
35840/tcp open  nlockmgr    1-4 (RPC #100021)  
39140/tcp open  status      1 (RPC #100024)  
39302/tcp open  java-rmi    GNU Classpath grmiregistry  
57629/tcp open  mountd      1-3 (RPC #100005)  

### Задание 2
SYN — отправляет SYN-пакеты и анализирует ответы для определения открытых портов.  
FIN-сканирование отправляет FIN-пакеты (используемые для завершения соединения) и анализирует ответы. Этот метод полезен для обхода некоторых типов брандмауэров.  
Xmas-сканирование отправляет пакеты с установленными флагами FIN, PSH и URG (пакет "подсвечен", как рождественская ёлка). Этот метод также используется для обхода брандмауэров.  
UDP-сканирование используется для поиска открытых UDP-портов. UDP-порты часто используются для DNS, DHCP, SNMP и других протоколов.  


