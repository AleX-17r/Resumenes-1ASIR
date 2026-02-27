## Subredes VLSM
Es un método de subredes de volumen **variable**, es decir mientras que con el tamaño fijo, tenemos todas las subredes del mismo tamaño, con esta podemos sacar de diferentes tamaños, lo que nos permite aprovechar mejor las IPs.

Por **ejemplo**:
en **FLSM** scamos de /24 dos /25; 
**VLSM** nos permite sacar una /25 y dos /26, un total de 3 subredes

**Tamaño Fijo:**
192.168.1.0/24
---|--->==192.168.1.0/25==
---|--->==192.168.1.128/25==
**Tamaño Variable**
192.168.1.0/24
---|--->==192.168.1.0/25==
---|--->192.168.1.128/25
------------|---->==192.168.128/26==
------------|---->==192.168.192/26==
Con el tamaño variable hemos sacado 2 subredes /26 de la subred /25
⚠️**Importante**: debemos tener en cuenta que tomar un bit de la parte de host, significa que el rango de hosts pasará a ser la mitad, y viceversa⚠️
