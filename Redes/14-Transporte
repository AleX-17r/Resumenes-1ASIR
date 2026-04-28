Es la responsable entre las comunicaciones de aplicación y Sesión
- Segmenta y rearma los datos, 
- agrega encabezado, 
- administra conversaciones
- segmenta y multiplexa para que no se intercalen las conversaciones

Utiliza TCP y UDP, dependiendo de la fiabilidad o velocidad que se requiera.

---
### TCP
Provee confiabilidad y control de flujo
Puede:
- Numerar y rastrear segmentos transmitidos desde aplicaciones específicas
- Confirmar que recibe los datos
- Retransmitir la información no reconocida
- Ordenar los datos
- Enviar datos a velocidad eficiente

---
### UDP
Nos permite enviar los datos muy rápido
- No es orientado a conexión
- No comprueba si los datos llegan

---
### Funcionamiento TCP
- Establece una sesión entre los dispositivos
- Garantiza que los datos llegan
- Proporciona la entrega en orden
- Controla el flujo de la transmisión

También sigue el estado de la sesión.
Registra la información que se envía y reconoce

---
### 3-Way Handshake
Verifica que el origen y destino puedan comunicarse
![[3wayhandshake.png]]
Para iniciar la comunicación
- El cliente solicita la comunicación (SYN), 
- el servidor la acepta devolviendo el SYN junto con un ACK 
- el cliente reconoce la sesión de comunicación.

Una vez finalizada la comunicación, se finaliza
- El cliente envía un FIN
- Servidor responde con un ACK y envía a continuación un FIN
- El cliente confirma con un ACK

----
### Reordenación de segmentos
Como no todos los segmentos llegan a la vez, TCP emite un orden de secuncia en el encabezado para así poder reordenarlos en el orden original.

---
### Pérdida y Retransmisión
Al transmitir la información, se crea una copia de cada segmento que se pone en una cola, cuando llega el ACK (con número de secuencia de su segmento) de que ha llegado lo borra, para así si no recibe el ACK poder retransmitir esos datos.

---
