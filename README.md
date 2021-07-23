# tpot

## Intro

T-Pot es una distribución de Linux basada en Debian (Ubuntu, Kali, etc.)

Esta distro está dedicada a ser un contenedor de todos los honeypots existentes, o al menos de los más conocidos.

#### ¿Y que son los honeypots?

Son básicamente señuelos. Sistemas "trampa" que están ahí para ser el blanco de atacantes y distraer o desviar la atención de los verdaderos activos de la organización, a la vez que recopilar información de los ataques.

T-pot incluye los siguientes honeypots:

Cada uno tiene un objetivo distinto, en cuanto a que levantan distintos servicios. Aunque también hay algunos que son similar o comunes.

```
adbhoney: android
ciscoasa
citrixhoneypot: citrix
conpot
cowrie
dicompot
dionaea
elasticpot: elasticsearch
glutton
heralding: ftp, telnet, ssh, http, https, pop3, pop3s, imap, imaps, smtp, vnc, postgresql
honeypy: python
honeysap
honeytrap: nmap
ipphoney: impresora ipp
mailoney: correo
medpot: Microsoft RDP (Remote Desktop Protocol)
rdpy
snare
tanner
```

T-pot tiene distintos tipos de instalación para seleccionar la que más nos interesa según el tipo de organización.

Yo he seleccionado "Collector" ya que contiene al menos "heralding".

T-pot además utiliza Elastic Search (Un motor de indexación de datos para realizar consultas de búsqueda más rápidas. Muchos servicios de internet lo utilizan para sus buscadores y así aligerar las consultas directas a las bases de datos). Entonces T-pot registra todos los ataques e intentos de intrusión en su base de datos y tira de Elastic Search para presentar los resultados en la interfaz gráfica (Kibana).

## Instalación Core

```
IP: 10.164.1.213
SSH: ssh -l tsec -p 64295 10.164.1.213
WEB: https://10.164.1.213:64297
ADMIN: https://10.164.1.213:64294
```

```
login: tsec
password: cangetin
```

```
web user: luis
password: m******
```

## Usuarios de prueba

```
luis
juan
bot
pepito
alumno
forense
manana
admin
root
adm
```

## Contraseñas de prueba

```
1234
mypass
Seguridad-1
contrasena
empleado
Cayenne
abc123
core
kiosko
cangetin
Tr@1n1ng
```

## Heralding honeypot

### ftp

Filezilla

or

from Kali

```
ftp

open 10.164.1.213
luis
1234
close

open 10.164.1.213
luis
mypass
close

open 10.164.1.213
juan
kiosko
close

open 10.164.1.213
bot
empleado
close
```

### telnet

from Kali

```
open 10.164.1.213

manana
abc123

luis
contrasena

forense
Tr@1n1ng
```

### ssh

```
ssh pepito@10.164.1.213
cangetin

ssh forense@10.164.1.213
kiosko

ssh bot@10.164.1.213
1234
```

### http

http://10.164.1.213

```
juan
Cayenne
```

http://10.164.1.213

```
manana
empleado
```

### https


https://10.164.1.213

```
admin
Tr@1n1ng
```

https://10.164.1.213

```
adm
abc123
```

### pop3, pop3s, imap, imaps, smtp

```
openssl s_client -connect 10.164.1.213:993 -crlf
? LOGIN juan Tr@1n1ng
? LOGIN luis kiosko
? LOGIN adm mypass
```

### vnc

VNC Viewer

```
10.164.1.213

core
cangetin
contrasena
```

### postgresql

from Kali

```
psql -h 10.164.1.213 -U manana
Cayenne

psql -h 10.164.1.213 -U pepito
empleado

psql -h 10.164.1.213 -U bot
1234

psql -h 10.164.1.213 -U luis
kiosko
```

## Enlaces

https://github.com/telekom-security/tpotce

https://www.elladodelmal.com/2017/07/t-pot-una-colmena-de-honeypots-para.html

https://blog.elhacker.net/2021/01/instalar-honeypot-t-pot-en-una-maquina-virtual-tpotce-cowrie-docker-dionea.html
