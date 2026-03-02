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
