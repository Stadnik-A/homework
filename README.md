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
Для более удобного и краткого ответа я использовал фильтры на конкретные порты в Wireshark.  
SYN — отправляет SYN-пакеты и анализирует ответы для определения открытых портов.  
![image](https://github.com/user-attachments/assets/e43bbcc8-7715-403e-a5e3-c2ecc2fe9331)  
В Wireshark видны SYN-пакеты от Nmap и ответы SYN-ACK от сервера на открытые порты.  
![image](https://github.com/user-attachments/assets/c1423fb0-58b8-417f-af9f-24d3c5ae203f)  

FIN — отправляет FIN-пакеты (используемые для завершения соединения) и анализирует ответы. Этот метод полезен для обхода некоторых типов брандмауэров.  
![image](https://github.com/user-attachments/assets/6400c0a5-ee75-4bdc-b9b7-4f0468527a72)  
В Wireshark dидны FIN-пакеты от Nmap, ответы RST от сервера на закрытые порты и отсутствие ответа на открытые порты.  
![image](https://github.com/user-attachments/assets/61f1a65a-3cc5-4ca6-8a74-787a610259b8)  

Xmas — отправляет пакеты с установленными флагами FIN, PSH и URG. Этот метод также используется для обхода брандмауэров.  
![image](https://github.com/user-attachments/assets/4f0e85fc-8164-408f-8509-da344b4f625d)  
В Wireshark видны пакеты с флагами FIN, PSH и URG, а также ответы RST от сервера на закрытые порты, и отсутствие ответа на открытые порты.  
![image](https://github.com/user-attachments/assets/a8c827d5-5209-4bf1-8804-20b05d09e197)  

UDP — используется для поиска открытых UDP-портов. UDP-порты часто используются для DNS, DHCP, SNMP и других протоколов.  
![image](https://github.com/user-attachments/assets/4b9a734d-9e20-4223-ace8-6c0f7fcb43fe)  
В Wireshark видны UDP-пакеты от Nmap, ответы ICMP "Port Unreachable" на закрытые порты и отсутствие ответа или UDP-ответы на открытые порты.  
![image](https://github.com/user-attachments/assets/e6a5fcc7-24ed-4a64-adf8-d50ba37b9891)  


