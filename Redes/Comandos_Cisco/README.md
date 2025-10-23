## Configurar login

**config term** -> entra a modo de configuración de la terminal.
**line console 0** -> entrar a la consola 0.
**password cisco** -> pone "cisco" como contraseña.
**login** -> habilita el acceso EXEC al usuario.
**end** -> para salir del modo de config.

## Configurar EXEC
**config term** -> configuración de la terminal
**enable secret class** -> "class" como contraseña cifrada para el modo EXEC
**exit** -> salir

## Encriptación de contraseñas
**config term** -> config de la terminal
**service password encryption** -> nos cifra las contraseñas

## Comprobar config
**show running-config** -> nos muestra la config actual
**banner motd 'hola'** -> crea un mensaje de aviso para iniciar sesión

## Configurar dirección IP
(enable + conf t)
**interface vlan 1** -> para configurar la interfaz
**ip address 192.168.1.1** -> para asignar IP a la interfaz
**no shutdown** -> para mantener la interfaz activa
