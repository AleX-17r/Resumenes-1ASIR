### Introducción
Puesto que IPv4 tiene 32bits, no daba para asignar demasiadas direcciones, para solucionar esto, salió IPv6, con 128bits.

Tienen 128bits, están en hexadecimal, se separan en 4 bits con : (XXX:XXX::)
- Nota: los Hextetos son grupos de 16bits o cuatro valores hexadecimales
Generalmente tienen muchos 0s, estos se pueden resumir quitándolos y poniendo " :: " en su lugar, sólo se puede hacer una vez en cada dirección, ya que rellenará con 0s hasta llegar a los 128 bits.

Los **hextetos** son grupos de 16bits o 4 valores hexadecimales

el formato es (ejemplo):
111a:222b:333c:444d:555e:666f:777a:888b /64


---
### Compatibilidad con IPv4
Puesto que son direcciones diferentes, existen herramientas (chapuzas) con las que compatibilizarlas.
- **Dual Stack**: simplemente usa a la vez IPv4 e IPv6.
- **Tunneling**: encapsula paquetes IPv6 en paquetes IPv4.
- **Translation**: NAT64 nos permite traducir direcciones.

---
### Resumir Direcciones
Las IPv6 se pueden resumir **quitando los 0s de la izquerda en cada hexteto**, o si está todo a 0s, podemos poner " :: ", esto significa que lo rellenará todo a 0s hasta llegar a los 128 bits, con lo que sólo puede estar una vez por dirección.

---
### Prefijo de Red
Las direcciones IPv6 se separan en 64 bits de:
- **prefijo**: la parte de red a la que pertenece
- **ID**: Identificador de Interfaz (parte de host)

- *Nota (ampliación): dentro del prefijo de red, los 16 bits finales son para el ID de subred*

---
### Tipos de Direccionamiento
Podemos clasificarlas según su Direccionamiento, es decir, dónde van.
- **Unicast**: el mensaje va a un dispositivo.
- **Multicast**: lo envía a varios dispositivos (se puede hacer para todos).
- **Anycast**: cunado hay varias con la misma dirección envía a la más cercana.

- *Nota (ampliación): Anycast no es orientado a conexión, ya que como eld estino puede cambiar, no podríamos mantener el estado de la comunicación.* 

Otra clasificación es según si son públicas o privadas
- **Global Unicast Address (GUA)**: son públicas y se enrutan en Internet, rango 2000::/3
- **Link Local Address (LLA)**: son las que tiene cada interfaz (loopback), fe80::/10
- **Unique Local Address (ULA)**: son las de la red local (privadas), se suele utilizar fd00::/8, su rango es fc00::/7 a fdff::/7
  Tienen 8 bits de prefijo (fd00) 40 para global, 16 para subred, y 64 para host
