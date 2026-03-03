**modo config:** 
`Router(config)# hostname hostname`
**Modo Exec con privilegios y cifradod e contraseñas:**
`Router(config)# enable secret password`
**Contraseña a Exec de usuario:**
`Router(config)# line console 0`
`Router(config-line)# password password`
`Router(config-line)# login`
**login remoto:**
`Router(config)# line vty 0 4`
`Router(config-line)# password password`
`Router(config-line)# login`
`Router(config-line)# transport input {ssh | telnet}`
**Cifrar contraseñas:**
`Router(config)# service password encryption`
**Banner motd:**
`Router (config) # banner motd # mensaje #`
Copiar config a la nvram:
`Router# copy running-config startup-config`

---
### Interfaces
`Router (config) # interface g0/0/0` (el nombre de la interfaz a configurar)
**Añadir descripción:**
`Router (config-if) # description (...)` 

**Configurar IPv4:**
`Router (config-if) # ip address 192.168.0.254 255.255.255.0`
**Configurar IPv6:**
`Router (config-if) # ipv6 address FE80: :1/64`
**Levantar interfaz**:
`Router (config-if) # no shutdown`

Podemos ver **todas las interfaces** con:
- IPv4: `show interface brief`
- IPv6: `show ipv6 interface brief`
Si queremos ver **estadísticas de interfaces**, usaremos:
- todo: `show interfaces`
- IPv4: `show ip interface`
- IPv6: `show ipv6 interface`
Para ver el contenido de las **tablas de enrutamiento**, podemos usar:
- IPv4: `show ip route`
- IPv6: `show ipv6 route`
Para configurar un **Gateway**, usaremos:
- ip default-gateway 192.168.1.254


---
