### Fundamentos de la Comunicación
La comunicación puede variar según se necesite, para esto se utilizan métodos o XD. Los métodos de comunicación siempre tienen:

- Origen de Mensaje
- Destino
- Canal
### Protocolos de Comunicación
Son el conjunto de reglas a seguir para hacer posible una comunicación.
Depende del tipo de comunicación utilizaremos unos u otros.

### Requisitos de protocolo de red
Incluyen:
**Codificación** de los mensajes: La codificación es el proceso por el que la información se convierte para poder transmitirse.

**Formato** y **encapsulamiento**: formato/estructura que sigue; incluye el destinoy el origen.

**Tamaño del mensaje**: el mensaje se separa en varias tramas, deberemos saber el tamaño de estas.

**Sincronización del mensaje**: 
- **Control de Flujo**: controla la velocidad de transmisión.
- **Response Timeout**: en caso de no recibir respuesta, reenvia la request o cierra la transmisión.
- **Método de Acceso**: Determina el momento en el que cada host puede enviar.

**Opciones de entrega del mensaje**: a quién/quiénes llega, estos son **Unicast**, **Multicast** **Broadcast**.

### Codificación de los mensajes
La codificación es el proceso por el que la información se convierte para poder transmitirse.

---
## Protocolos
Para poder comunicar 2 nodos, deben seguir los mismos protocolos.

### Funciones de protocolos
- **Direccionamiento**: Identifica al emisor y al destinatario (Ethernet,IP).
- **Confiabilidad**: Garantiza que se entregue el mensaje (TCP).
- **Control de Flujo**: Asegura una velocidad eficiente (TCP).
- **Secuenciación**: Etiqueta cada segmento de datos, esto sirve para volver a ensamblar el mensaje (TCP).
- **Detección de Errores**: Detecta errores (IP,TCP)
- **Interfaz de la Aplicación**: Contiene información para la comunicación (HTTP)


### Interacción de protocolos
Al enviar información, se utilizan varios protocolos.
Por ejemplo, en un cliente que se conecta a un servidor web:
- **HTTP**: Regula la interacción entre el servidor y el cliente, define formato de solicitud y respuesta.
- **TCP**: Controla el flujo y administra las conversaciones, para así asegurar la entrega fiable de la información
- **IP**: Se encarga de la entrega de mensajes, lo utilizan los routers para el rennvío entre redes.
- **Ethernet**: Responsable de la centrega de mensajes en la LAN.

---
### TCP/IP
TCP/IP combina diferentes protocolos para la transmisión, dependiendo de como sea, utilizara uno u otro en cada capa.

(*"C." se refiere a capa*)
- **C. de Aplicación**: DNS, DHCP, SMTP, POP3, IMAP, FTP, HTTP.
- **C. de Transporte**: TCP, UDP.
- **C. Internet**: IP, NAT, ICMP, OSPF, BGP, EIGRP
- **C. Acceso a Red**: ARP, Ethernet, WLAN.

---
### Estándares abiertos
Se encargan de que dispositivos de diferentes fabricantes sean compatibles entre sí.

**IANA** e **ICANN**: asignan (venden) nombres y números (IPs y nombres de dominio).
**IEE**: estandarización de electrónica (Ethernet, WiFi, Bluetooth).
**EIA**: Cableado eléctrico, conectores y Racks 19"

---
### Modelo OSI
