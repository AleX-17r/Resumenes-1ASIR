### Máscara de red
Nos indica la parte de red en una drección IP.

pasando a binario la dirección IP y la máscara podemos sacar la dirección de red con una operación AND (los bits que tienen en común **ambos**).

010**1**
001**1** 
= 000**1**
- *Nota: (AND y Anding son lo mismo)*

Longitud de prefijo: hace referencia al número de bits que tenemos de parte de red

---
### Tipos
Se clasifican según:
- Públicas: IPs de Internet, las asigna un ISP
- Privadas: Las de la red Local
También:
- Estáticas: se configuran manualmente y se quedan ahsta que se cambie.
- Dinámica: se refresca cada cierto tiempo ([DHCP](https://github.com/AleX-17r/Resumenes-2SMR/tree/main/S-Red/DHCP))

**(Relleno que entra en examen)**
En el caso de las públicas las asigna el registro de Recursos de Números de Internet, en Europa es **RIPE NCC**.
El **RIR** asigna bloques de IP a los **ISP** (Proveedores).
Los **ISP** asignan las IPs a sus **usuarios**.

**(Más relleno)**
Hay diferentes clases según sus rangos
- **A**: 0.0.0.0 - 127.255.255.255
- **B**: 128.0.0.0 - 191.255.255.255
- **C**: 192.0.0.0 - 233.255.255.255
Hay otras especiales que son:
- **D**: 224.0.0.0 - 239.255.255.255 (Multicast)
- **E**: 240.0.0.0 - 255.255.255.255 (Investigación)

- *Nota: Cuando se creó el protocolo se decidieron estos rangos porque sobraban IPs, en la actualidad se usan subredes, con lo que esto no tiene demasiado sentido*

---
### NAT
Network Address Translation es un protocolo que traduce las direcciones de hosts a su IP pública apra salir a Internet, cuando vuelve la respuesta al cliente, vuelve a traducirla para que llegue al host.

---
### IPs reservadas
hay algunas IPs que están reservadas por la red y que **NO** se pueden usar en hosts
- **Red**: la IP de la red, tiene la parte de Host a 0s (por ejemplo 192.168.1.0)
- **Broadcast**: toda la parte de host a 1s (por ejemplo: 192.168.1.255)
- **Loopback**: son las que tiene cada dispositivo para referirse a sí mismo (127.0.0.1)
- **Enlace Local/APIPA**: son las que se configuran automáticamente si el host no tiene IP fija ni recibe por DHCP. (169.254.0.0/16)
Para uso privado están reservadas (RFC 1918):
- 10.0.0.0/8
- 172.16.0.0/16
- 192.168.0.0/24

- (*Nota: Es importante mantener una parte de red al menos similar para que no coincida una de nuestras IPs privada con una pública, pero a las máscaras no les daremos importancia*)

---
### Tipos de Transmisión
- **Unicast**: Un host envía un mensaje a otro.
- **Broadcast**: Envía a toda la red (menos a sí mismo).
- **Multicast**: Envía a un grupo de direcciones.

---
### Supernetting
Funciona igual que el subnetting, pero a la inversa, si por ejemplo tenemos 2 subredes seguidas /24, podemos juntarlas como una /23.
Mientras que Subnetting toma parte de host como parte de red, Supernetting toma parte de red como parte de host.
Esto nos sirve para resumir redes, tener más hosts dentro de la misma subred, y poco más.

**Problemas**
Si tenemos demasiados hosts dentro de la misma red, se saturará, sobretodo si los hosts empiezan a enviar Broadcasts como locos.

---
pg 34
