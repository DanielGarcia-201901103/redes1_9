# Manual Técnico
---
### Configuración de las VPCs (una por cada área) en total 10.
> Para el calculo de las ip's se utilizaron los numeros finales de los 3 carnets: 7+3+8 = 18 y también los numeros de los niveles. Por lo que se tienen las siguientes direcciones ip.

- Para el nivel 1
    -   192.168.18.10
    -   192.168.18.11
    -   192.168.18.12
    -   192.168.18.13
    -   192.168.18.14
    -   192.168.18.15
    -   192.168.18.16
    -   192.168.18.17
    -   192.168.18.18
    -   192.168.18.19 
- Para el nivel 2
    -   192.168.18.20
    -   192.168.18.21
    -   192.168.18.22
    -   192.168.18.23
    -   192.168.18.24
    -   192.168.18.25
    -   192.168.18.26
    -   192.168.18.27
    -   192.168.18.28
    -   192.168.18.29
    -   192.168.18.211
    -   192.168.18.212 
- Para el nivel 3
    -   192.168.18.30
    -   192.168.18.31
    -   192.168.18.32
    -   192.168.18.33
    -   192.168.18.34

![Ip recursos humanos](./images/asignacionIp.png)

1. **Recursos Humanos - VPC con ip 192.168.18.12**
- nombrando VPC con ip

![Ip recursos humanos](./images/ip_rh.png)

- Configurando ip y mascara de subred.

![Configuración Ip rh](./images/ipconfigurar_rh.png)

2. **Gerencia y Secretaría - VPC con ip 192.168.18.19**
- nombrando VPC con ip

![Ip gerencia y secretaria](./images/ip_gerencia.png)

- Configurando ip y mascara de subred.

![Configuración ip gerencia](./images/ipconfigurar_gerencia.png)

3. **Administración - VPC con ip 192.168.18.18**
- nombrando VPC con ip

![Ip Administración](./images/ip_administracion.png)

- Configurando ip y mascara de subred.

![Configuración ip Administración](./images/ipconfigurar_administracion.png)

4. **Atención al cliente - VPC con ip 192.168.18.17**
- nombrando VPC con ip

![Ip atención al cliente](./images/ip_atencioncliente.png)

- Configurando ip y mascara de subred.

![Configuración ip atención al cliente](./images/ipconfigurar_atencioncliente.png)

5. **Oficina A - VPC con ip 192.168.18.22**
- nombrando VPC con ip

![Ip oficina A](./images/ip_oficinaA.png)

- Configurando ip y mascara de subred.

![Configuración ip Oficina A](./images/ipconfigurar_oficinaA.png)

6. **Oficina B - VPC con ip 192.168.18.29**
- nombrando VPC con ip

![Ip oficina B](./images/ip_oficinaB.png)

- Configurando ip y mascara de subred.

![Configuración ip Oficina B](./images/ipconfigurar_oficinaB.png)

7. **Oficina C - VPC con ip 192.168.18.24**
- nombrando VPC con ip

![Ip oficina C](./images/ip_oficinaC.png)

- Configurando ip y mascara de subred.

![Configuración ip Oficina C](./images/ipconfigurar_oficinaC.png)

8. **Ventas - VPC con ip 192.168.18.30**
- nombrando VPC con ip

![Ip ventas](./images/ip_ventas.png)

- Configurando ip y mascara de subred.

![Configuración ip ventas](./images/ipconfigurar_ventas.png)

9. **Recepción - VPC con ip 192.168.18.31**
- nombrando VPC con ip

![Ip recepción](./images/ip_recepcion.png)

- Configurando ip y mascara de subred.

![Configuración ip recepción](./images/ipconfigurar_recepcion.png)

10. **Ti - VPC con ip 192.168.18.32**
- nombrando VPC con ip

![Ip Ti](./images/ip_Ti.png)

- Configurando ip y mascara de subred.

![Configuración ip Ti](./images/ipconfigurar_Ti.png)


### Pings entre los hosts 🛜
### Realización del ping 1️⃣.
![Ping 1](./images/ping1.png)
### Realización del ping 2️⃣.
![Ping 2](./images/ping2.png)
### Realización del ping 3️⃣.
![Ping 3](./images/ping3.png)
### Realización del ping 4️⃣.
![Ping 4](./images/ping4.png)
### Realización del ping 5️⃣.
![Ping 5](./images/ping5.png)

### Demostración de la captura de un paquete ARP/ICMP (solo 1 en general), incluyendo captura de pantalla. 

A continuación se presenta el envío de un paquete de la VPC de administración (192.168.18.18) hacia la VPC perteneciente a la oficina C (192.168.18.23):

![Captura de paquetes](./images/Captura_de_paquetes.JPG)

Como se puede observar en la siguiente imagen, los se utilizarón los protocolos ICMP y ARP. El protocolo ICMP es un protocolo de red que su funcion es realizar envios de mensajes de control es este caso en la red entre oficinas, esto con el proposito de verificar si las VPC tienen conectividad entre si. El color del paquete se identifica con el color azul:

![Captura de paquetes 2](./images/Captura_de_paquetes6.JPG)

De la misma manera se utilizó el protocolo ARP que es utilizado para mapear direcciones IP a direcciones MAC que es esencial para la comunicación en la capa de enlace de datos, en pocas palaras estre protocolo se utiliza para traducir direcciones IP a direcciones MAC, que son necesarias en la capa de enlace de datos para enviar paquetes a traves de nuestra red. El color del paquete enviado es verde: 

![Captura de paquetes 3](./images/Captura_de_paquetes2.JPG)

Al ejecutar el simulador, se comienzan a enviar los paquetes y se puede observar el flujo de envío:

![Captura de paquetes 4](./images/Captura_de_paquetes3.JPG)


---
### Configuración de switches
Para la configuración de los switches se utilizaron los comandos 
```
enable
configure terminal
enable secret numerodeswitch "el comando enable secret fue utilizado para establecer una contraseña "
do write
do write memory
do copy running-config startup-config
exit
exit
```
# Configuración del Switch1
![cs1](./images/confswitch1.png)
# Configuración del Switch1 Parte 2
![cs12](./images/contraswitch1.png)
# Login del Switch1
![log1](./images/loginswitch1.png)
# Configuración del Switch2
![cs2](./images/confwitch2.png)
# Login del Switch2
![log2](./images/loginswitch2.png)
# Configuración del Switch3
![config3](./images/confwitch3.png)
# Login del Switch3
![s3](./images/logswitch3.png)
