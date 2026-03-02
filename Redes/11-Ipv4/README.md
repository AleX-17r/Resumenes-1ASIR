### Máscara de red
Nos indica la parte de red en una drección IP.

pasando a binario la dirección IP y la máscara podemos sacar la dirección de red con una operación AND (los bits que tienen en común **ambos**).

010**1**
001**1** 
= 000**1**
- *Nota: (AND y Anding son lo mismo)*

Longitud de prefijo: hace referencia al número de bits que tenemos de parte de red

---
Se clasifican según:
- Públicas: IPs de Internet, las asigna un ISP
- Privadas: Las de la red Local
También:
- Estáticas: se configuran manualmente y se quedan ahsta que se cambie.
- Dinámica: se refresca cada cierto tiempo ([DHCP](https://github.com/AleX-17r/Resumenes-2SMR/tree/main/S-Red/DHCP))


