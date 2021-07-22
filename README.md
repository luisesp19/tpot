# tpot

## Enlaces

https://github.com/telekom-security/tpotce

https://www.elladodelmal.com/2017/07/t-pot-una-colmena-de-honeypots-para.html

https://blog.elhacker.net/2021/01/instalar-honeypot-t-pot-en-una-maquina-virtual-tpotce-cowrie-docker-dionea.html

## Credenciales

```
login: tsec
password: cangetin
```

```
web user: luis
password: m******
```

## Instalación nativa máquina Core

```
IP: 10.164.1.213
SSH: ssh -l tsec -p 64295 10.164.1.213
WEB: https://10.164.1.213:64297
ADMIN: https://10.164.1.213:64294
```

## Usuarios

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

## Contraseñas

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

## Heralding

### ftp

```
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

```
aaa
```

### postgresql

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

### others

```
socks5
```
