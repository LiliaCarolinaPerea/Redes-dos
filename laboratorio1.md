2. 
a). ¿Cuál es la dirección de red y de broadcast de un host que tiene una ip 192.168?10.10/30?

La dirección de red y del broadcast de un host que tiene una ip 192.168.10.10/30 son los siguientes:
Dirección de red: 192.168.10.8
Dirección de broadcast: 192.168.10.11

B). ¿Qué información se puede inferir de un host con la dirección 169.254.255.200/26?

1.	Dirección IP del host: 169.254.255.200
2.	Máscara de subred: /26 (255.255.255.192 en notación decimal)
3.	Rango de direcciones IP utilizables en la subred: 169.254.255.193 a 169.254.255.254 (este rango excluye la dirección de red y la dirección de broadcast)
4.	Dirección de red: 169.254.255.192
5.	Dirección de broadcast: 169.254.255.255
6.	Cantidad de direcciones IP utilizables: 62 (debido a que /26 deja 6 bits para hosts, lo que da lugar a 2^6 - 2 = 62 direcciones utilizable después de descontar la dirección de red y la dirección de broadcast)
La característica clave aquí es la dirección IP 169.254. Esta es una dirección IP reservada que se utiliza en el protocolo de configuración automática de direcciones IP conocido como APIPA (Automatic Private IP Addressing). Esto significa que si un dispositivo no puede obtener una dirección IP de un servidor DHCP y tiene habilitada la función de APIPA, entonces seleccionará automáticamente una dirección IP de este rango. Esto suele ocurrir cuando un dispositivo no puede comunicarse con un servidor DHCP en la red. Por lo tanto, la dirección IP 169.254.255.200 sugiere que este host está configurado para usar APIPA debido a la incapacidad de obtener una dirección IP válida de un servidor DHCP.

c). ¿Cuantas sub-redes puede lograr con la máscara 172.16.0.0/22?.

Para determinar cuántas subredes se pueden lograr con la máscara de subred 172.16.0.0/22, primero necesitamos entender la cantidad de bits que se reservan para la porción de red y la porción de host. La notación "/22" indica que hay 22 bits en la porción de red y los 32 - 22 = 10 bits en la porción de host. La fórmula para calcular el número de subredes posibles es 2^n, donde "n" es el número de bits que se toman prestados de la porción de host para formar la porción de subred. En este caso, hay 10 bits en la porción de host que se pueden utilizar para crear subredes. Por lo tanto:
Número de subredes = 2^10 = 1024 subredes 
En resumen, con la máscara de subred 172.16.0.0/22, podemos lograr hasta 1024 subredes diferentes.

d). ¿Cuantos clientes puede tener la sub red 172.16.0.0/22?.

Para determinar cuántos clientes puede tener en total en la subred 172.16.0.0/22, primero debemos calcular la cantidad de direcciones IP utilizables en esa subred. La notación "/22" indica que hay 22 bits en la porción de red y 32 - 22 = 10 bits en la porción de host. Sin embargo, recordemos que de esas 10 direcciones IP de host posibles, dos de ellas están reservadas: una es para la dirección de red y otra para la dirección de broadcast. Por lo tanto, el cálculo sería: 
Número de direcciones IP utilizables = 2^(número de bits en la porción de host) - 2 Número de direcciones IP utilizables = 2^10 - 2 Número de direcciones IP utilizables = 1024 - 2 Número de direcciones IP utilizables = 1022 direcciones IP utilizables para clientes
Por lo tanto, en la subred 172.16.0.0/22, se puede tener hasta 1022 clientes con direcciones IP únicas.
e)	¿Qué clase y tipo de dirección es 10.10.10.0/24?.

La dirección IP 10.10.10.0/24 pertenece a la clase A de direcciones IP, y se trata de una dirección IP privada.
Para aclararles un poco lo de las clases:
•	Clase A: Rango de direcciones IP de 1.0.0.0 a 126.255.255.255
•	Clase B: Rango de direcciones IP de 128.0.0.0 a 191.255.255.255
•	Clase C: Rango de direcciones IP de 192.0.0.0 a 223.255.255.255
La dirección 10.10.10.0 se encuentra dentro del rango de direcciones reservadas para la Clase A (1.0.0.0 a 126.0.0.0). El "/24" indica que los primeros 24 bits de la dirección IP se utilizan para la porción de red, y los últimos 8 bits se utilizan para la porción de host. Además, la dirección 10.10.10.0/24 se encuentra en el rango de direcciones IP privadas. Las direcciones IP privadas son direcciones que se pueden utilizar en redes internas, y no se enrutan en Internet público. Esto significa que podemos usar la dirección IP 10.10.10.0/24 en una red privada sin preocuparte por conflictos con direcciones públicas en Internet. Por lo tanto la dirección IP 10.10.10.0/24 pertenece a la Clase A de direcciones IP y es una dirección IP privada


## 3. [Caracterización de los adaptadores](#) ✔
|Parámetro||Valor|
|--|:--:|--:|
|Número de adaptadores Físicos|-->|3|
|Número de adaptadores Virtuales|-->|1|
|Tipo de Adaptador principal|-->|Wi-fi|
|Fabricante del Adaptador principal|-->|Realtek PCIe GbE Family Controller|
|Código MAC del fabricante|-->|6C-02-E0|
|MAC|-->|6C-02-E0-0D-2E-B1|

>Nota: Para obtener los parámetros de la red, usaremos los comandos [ipconfig][10], [ifconfig][8], [getmac][9].


## 4. [Caracterización de la red](#) ✔
|Parámetro|Valor|
|--|--:|
|__Subnet__|192.168.101.0/24|
|IPv4|192.168.101.74|
|Subnet Mask decimal|24|
|Subnet Mask octetos|255.255.255.0|
|Número de direcciones de Host|101|
|Rango de direcciones de Host|192.168.101.1-101|
|IP Broadcast|192.168.101.255|
|Server DHCP|192.168.101.254|
|Server DNS|8.8.8.8|

>Nota: Para obtener los parámetros de la red, usaremos el comando [ipconfig][10] o [ifconfig][8].


## 5. [Caracterización de la puerta de enlace](#) ✔
|Parámetro|Valor|
|--|--:|
|Número de Entradas en la tabla ARP |9|
|IPv4 Gateway|192.168.101.254|
|MAC Gateway|6C-02-E0-0D-2E-B1|
|ISP|COLOMBIA TELECOMUNICACIONES SA ESP|
|[IP Publica][5]|152.200.190.58|
|[Sistema Autónomo][6]|AS3816|


>Nota: Para obtener los parámetros de la red, usaremos el comando [arp][11] y algún servicio web/HTTP como [cual-es-mi-ip.net][5], [ipinfo.io][6] o [asrank.caida.org][9_1].


## 6. [Retardo de la red](#) ✔
|Servidor|IP|Tiempo promedio/ms|
|--|--|--|
|DNS Google|8.8.8.8|24ms|
|DNS Cloudflare|1.1.1.1|29ms|
|OpenDNS|208.67.222.222|69ms|
|Alternate DNS|76.76.19.19|18ms|
|DNS Quad9|9.9.9.9||27ms|
|AdGuard DNS|94.140.14.14|79ms|

>Nota: Para calcular el retardo de la red, usaremos el protocolo ICMP/[ping][12] con al menos 10 paquetes.


## 7. [Capacidad del canal](#) ✔
|Servidor|Ping/ms|Down/MB|Up/MB|
|--|:--:|--:|--:|
|[speed test][1]|39|96.4|69.2|
|[Netflix][2]|14|78|67|
|[Claro][3]|13|74|31|
|[nperf][4]|6.7|93.6|54.98|

>Nota: Para calcular el retardo de la red, usaremos el protocolo HTTP via servicio WEB.


## 8. [Distancia desde el host](#) ✔
|Servidor|Ping/ms|Numero de Saltos|
|--|:--:|--:|
|google.com|14|10|
|GMail.com|15|9|
|YouTube.com|14|10|
|dns.google|15|9|
|aws.amazon.com|154|17|
|portal.azure.com|13|11|
|login.live.com|88|22|
|Facebook.com|120|11|
|c.ns.WhatsApp.net|151|12|
|claro.com.co|151|12|
|platzi.com|122|11|
|rappi.com.co|184|30|

>Nota: Para calcular el retardo de la red, usaremos el comando ICMP/[tracert][13].

## 9. [Diagrama de Red](#) ✔
- Realice un diagrama topológico de la red que le ofrece conectividad a internet.
- Incluya todos los detalles de la red de area local a la que se encuentra conectado.
- Incluya los saltos conocidos incluyendo el equipo de borde de su ISP.

>Nota: Para conocer el tamaño y la topología de la red, usaremos la información previa y la pagina [ASRank][9_1].

## 10. [Preguntas de conocimiento](#) ✔
1. ¿Cuál es el retardo esperado para tu red según la tecnología contratada?
1. ¿Coincide el retardo medido con el esperado para tu red según la tecnología contratada? ¿Por qué?
1. ¿Por qué varia la capacidad del canal en las distintas pruebas realizadas?
1. ¿Cuál de los servicios DNS es mejor para configurar mi LAN?
1. ¿Como podría medir la disponibilidad de ni conexión a internet?



