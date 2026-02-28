### MAC/IP
Los dispositivos de una red tienen 2 direcciones: 
- **MAC**: dirección física de capa 2 (enlace), está en la tarjeta de red (NIC).
- IP: dirección lógica de capa 3 (red).
Cuando el mensaje pasa a una red remota, su dirección MAC pasa a ser la de su puerta de enlace.
(la interfaz del router por el que sale de la red que lleva al host).

---
### ARP
**Addres Resolution Protocol (ARP)**: es un protocolo que nos permite conocer la dirección MAC teniendo la IP, (tiene una lista de cada MAC con la IP que tiene asociada en la red).
- *Nota (fuera de examen): existe Reverse-ARP, que nos permite conocer la IP sabiendo la MAC.*
Para enviar una trama el host comprobará la MAC del destino, en caso de estar en otra red, la MAC será la de su Gateway.
- *Nota: si hubiera varios routers, se pondría la MAC del siguiente en cada salto*
