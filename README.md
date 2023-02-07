# f3bruary

locate .nse | xargs grep "categories" | grep -oP '".*?"' | sort -uq

Execution with privilege vs without:
Running as a normal user and not root it will be perform TCP Connect (complete handshake connection) based scan. 
If run the command with sudo at the front it will run as a TCP SYN scan (half handshake connection), this scan is more faster thank the first one.


nmap -p 80 216.20.21.33
Paquetes que envía nmap a un servidor publico con la sentencia anterior:
Paquetes:  | PING | SYN (443) | ACK (80) | Timestamp |
Si el servidor tiene bloqueados los paquetes ICMP (ping), o no tiene levantado algún servicio en el 80 o 443 es probable
