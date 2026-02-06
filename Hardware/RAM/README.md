**Nota**: las MT/s se sacan a apartir  de 
$MhzReales * 8 * multpiplicadorDDR$, 
en el caso de DDR sería
$100Mhz * 8b * 2mddr = 1600MT/s$

*mddr: Multiplicador DDR (2, 4, 8) según su versión; en DDR es 2*
*8b: 8 bytes, porque $bit * 8 = byte$*
*100Mhz: sería la cantidad de Mhz, dependerá del módulo, 100 es un ejemplo*

*Multiplicar la real por su mddr y por 8 es lo mismo que la efectiva por 8*
$200MhzEfectivos * 8 = 1600MT/s$
:P

---
**DDR** -> hace el doble, con lo que cada transerencia multiplica por 2, es decir $100MhzReales = 200 MhzEfectivos (MT/s)$
(real = normal, velocidad que te venden)
$MhzReal * 2 = MhzEfectivos$
La velocidad efectiva puede ser Mhz o MT/s; la capacidad Máxima de trans es MB/s

---
DDR2 -> permite el doble que DDR, con lo que tenemos 4 transferencias en cada ciclo.
100Mhz reales = 400Mhz efectivos
$Mhz * 4 = MhzEfectivos$

---
DDR3 -> el doble que DDR2 lmfao, 8 transferencias en cada ciclo.
$100Mhz reales *8 = 800MhzEfectivos$

---
DDR4 -> sigue multiplicando por 8, como DDR3, tiene otras mejoras.
`100MhzReales * 8 = 800MhzEfectivos`

---
DDR5 -> tiene un multiplicador de 8 (o 16, hay dudas sobre ello...).
$100MhzReales *8 = 8MhzEfectivos$

---
**Latencia**:
Se mide en CAS
$VelocidadEfectiva/CAS = Coeficiente$
a mayor coeficiente mejor
