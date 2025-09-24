## Conversión entre diferentes Unidades
Existen dierentes unidades según la cantidad que queramos medir.
El dato más pequeño existente es el bit, la información se guarda en bytes (8 bits).
En casos en los que tenemos grandes volúmenes de información, se utilizan otras unidades, como por ejemplo el KB (1000/1024 Bytes).

![:P](images/Screenshot_20250527_081822.png)

Existen 2 Unidades de Medida para estos casos, estos son:
-  **Binario**: utilizado internamente por ordenadores, cada nivel (KB -> MB) son 1024
-  **Internacional**: más fácil de calcular para humanos, cada nivel son 1000

⚠️ Deberemos saber con qué sistema estamos trabajando para saber si multiplicar/dividir por 1000 o por 1024. 
Recuerda: un **Gibibyte** hace referencia a que es en Binario, un Gabyte será en decimal⚠️

![:P](images/Screenshot_20250527_081822.png)

---
## Conversión entre Binario y Decimal

El binario se basa en potencias de 2.
Podemos saber cuál sería el número en decimal a partir de la posición de los números **1**, por ejemplo en la siguiente imagen vemos que tenemos **1**s en la posición de **64** y de **16**, esto significa que nuestro número en decimal será **64+16=80**
![[Pasted image 20250923135759.png]]
Para convertir de decimal a binario, podemos hacer utilizar el mismo método, por ejemplo:
Si tenemos el 90:
La forma más rápida será restando en los números de la tabla, si este es mayor a  nuestro número, pondremos un 0 y pasaremos al siguiente, si es menor, se lo restaremos, y pondremos un 1 en su posición.

![:P](images/Screenshot_20250527_081822.png)

(128 > 90, con lo que ponemos un 0; 64 < 90, con lo que lo restaremos, nos quedamos con 26, ponemos un 1 en esta posición y probamos con el siguiente).

⚠️Dado que el sistema Binario se basa en potencias de 2, nuestra tabla siempre será de 1, 2, 4 , 8, 16, 32, 64, 128, 256, 512, 1024,...⚠️

---

