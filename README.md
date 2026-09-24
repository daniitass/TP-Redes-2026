# TP-Redes-2026
Trabajo grupal ifts 18 - 2026 
# Integrantes 
## GRUPO D:
* Lezcano, Sergio.
* Roth Norberto Oscar
* Tassara Daniela
* Quintana, María Florencia

## Preguntas:

## 1. VLAN (Virtual Local Area Network)

Una **VLAN** o *LAN Virtual* permite crear redes lógicamente independientes sobre una misma infraestructura física. Requiere el uso de switches gestionables e idealmente routers compatibles para segmentar y administrar adecuadamente el tráfico.

### Ventajas principales
* **Seguridad:** Aísla el tráfico entre redes por defecto. Para permitir la comunicación entre diferentes VLANs, es necesario implementar un router o switch multicapa (Capas 3) mediante *inter-vlan routing*.
* **Segmentación y flexibilidad:** Permite agrupar equipos en distintas subredes fácilmente, asignando políticas específicas de comunicación y acceso a Internet.
* **Optimización de la red:** Contiene el tráfico de *broadcast* (difusión) en dominios más pequeños. Esto evita que las transmisiones masivas saturen la red global.
* **Reducción de costes:** Maximiza el rendimiento del ancho de banda y elimina la necesidad de adquirir hardware costoso adicional para dividir redes.
* **Gestión eficiente:** Facilita la administración a los equipos de TI al aplicar políticas unificadas a través de los switches, además de adaptar la red a requisitos geográficos o proyectos específicos.

### Desventajas
* **Complejidad de mantenimiento:** Requiere conocimientos avanzados tanto para su configuración como para su posterior administración.
* **Escalabilidad limitada:** Los switches tienen un límite máximo en la cantidad de VLANs que pueden soportar.
* **Carga en los equipos:** Gestionar múltiples VLANs en un mismo dispositivo puede ocasionar sobrecarga de procesamiento.
* **Riesgos de seguridad:** Una mala configuración puede hacer la red vulnerable a ataques como el *VLAN hopping*.
* **Incompatibilidad de hardware:** Todos los dispositivos de red deben admitir el estándar **802.1Q**, lo que puede exigir la renovación de equipos.

### Tipos de VLAN
* VLAN nativa
* Etiquetado VLAN 802.1Q
* VLAN basadas en puerto
* VLAN basadas en MAC
* VLAN etiquetadas
* VXLAN
* VLAN híbrida
* VLAN de gestión
* VLAN de control
* VLAN dedicada

---

## 2. VPN (Virtual Private Network)

Una **VPN** o *Red Privada Virtual* es una tecnología que establece una conexión a Internet segura y cifrada entre el dispositivo del usuario y una red privada o punto de conexión de confianza.

### Características fundamentales
* **Virtual:** No requiere cables o enlaces físicos dedicados.
* **Privada:** Oculta el tráfico y las actividades frente a terceros.
* **En red:** Conecta de forma coordinada múltiples dispositivos (como el cliente y el servidor VPN).

### Pilares tecnológicos
1. **Cifrado:** Transforma los datos en un formato ilegible (texto cifrado) mediante algoritmos criptográficos para proteger credenciales y datos confidenciales.
2. **Tunelización:** Encapsula los paquetes de datos cifrados para que viajen de forma aislada a través de redes públicas no seguras.
3. **Autenticación:** Valida que solo usuarios y dispositivos autorizados puedan conectarse al túnel y acceder a los recursos internos.

### Ventajas principales
* **Privacidad y anonimato:** Enmascara la dirección IP del usuario y evita el rastreo o la interceptación en redes públicas.
* **Acceso remoto seguro:** Permite a empleados, desarrolladores y estudiantes conectarse a sistemas corporativos o educativos desde cualquier lugar.
* **Integración con la nube:** Une de forma segura infraestructuras locales con plataformas en la nube (como Azure) mediante gateways dedicados.
* **Cumplimiento normativo:** Ayuda a cumplir los estándares de seguridad de protección de datos en tránsito.

### Casos de uso comunes
* **Trabajo remoto e híbrido:** Conexión segura a datos y aplicaciones internas sin exporlos a Internet.
* **Conectividad sitio a sitio:** Enlace entre sucursales u oficinas sin depender de líneas privadas dedicadas de alto costo.
* **Entornos multinube e híbridos:** Interconexión de recursos locales con múltiples proveedores de nube.
* **Entornos de desarrollo:** Acceso privado y cifrado a APIs, entornos de pruebas y servicios en la nube.
* **Ámbito educativo:** Acceso remoto de estudiantes a bases de datos, bibliotecas digitales y plataformas académicas.

---

## 3. SAN (Storage Area Network)

Una **SAN** es una red dedicada y de alta velocidad que conecta servidores con sistemas de almacenamiento compartido (matrices de discos, unidades SSD/HDD o bibliotecas de cintas) mediante hardware y software especializado (como *Fibre Channel*).

### Importancia
A diferencia del almacenamiento adjunto tradicional, permite superar los límites de capacidad local, optimizar la protección de datos, gestionar el acceso multiusuario de gran escala y ofrecer alto rendimiento para aplicaciones empresariales junto a esquemas NAS.

### Ventajas principales
* **Disponibilidad mejorada:** El almacenamiento es independiente de las aplicaciones y accesible a través de múltiples rutas de conexión.
* **Rendimiento optimizado:** Descarga el procesamiento de almacenamiento de los servidores de aplicaciones hacia una red independiente.
* **Gestión centralizada y consolidada:** Simplifica la administración al unificar los medios de almacenamiento, permitiendo mayor escalabilidad y flexibilidad.
* **Recuperación ante desastres:** Facilita la creación de copias remotas de datos para protección contra ataques o fallos graves.

### Formas de interacción en la SAN
* **Servidor a Almacenamiento:** Acceso directo y simultáneo de múltiples servidores a los mismos recursos de almacenamiento.
* **Servidor a Servidor:** Comunicación directa de alta velocidad y baja latencia entre servidores.
* **Almacenamiento a Almacenamiento:** Mapeo, migración y respaldo de datos directamente entre dispositivos de almacenamiento sin saturar la CPU del servidor.

### Componentes principales
* **Servidores:** Plataformas que ejecutan las aplicaciones corporativas.
* **Sistemas de almacenamiento:** Discos (HDD/SSD/Flash) y bibliotecas de cintas.
* **Infraestructura de red:** Componentes de interconexión físicos (conmutadores, directores, enrutadores, Fibre Channel) y software de gestión centralizada.

---

## 4. Comparativa de Dispositivos de Red

### 1. Repetidor (Repeater)
* **Capa OSI:** Capa 1 (Física).
* **Función:** Captura y regenera/amplifica la señal (cableada o inalámbrica) para extender el alcance físico del segmento de red.
* **Características:** Cuenta generalmente con solo dos puertos. No inspecciona ni filtra el tráfico.

### 2. Hub (Concentrador)
* **Capa OSI:** Capa 1 (Física).
* **Función:** Actúa como punto de conexión central multiport para múltiples dispositivos dentro de una LAN.
* **Características:**
  * Reenvía los paquetes entrantes a todos sus puertos indiscriminadamente (difusión general).
  * Trabaja en modo *semidúplex*, compartiendo un único dominio de colisión entre todos los puertos, lo que puede provocar congestión.
  * Funciona internamente como un repetidor multipuerto básico.

### 3. Switch (Conmutador)
* **Capa OSI:** Capa 2 (Enlace de datos).
* **Función:** Conecta múltiples dispositivos en una red local (LAN) de forma inteligente.
* **Características:**
  * Utiliza **direcciones MAC** para enviar datos únicamente al dispositivo de destino específico.
  * Crea canales dedicados para cada conexión, eliminando los dominios de colisión y optimizando el rendimiento del tráfico interno.

### 4. Router (Enrutador)
* **Capa OSI:** Capa 3 (Red).
* **Función:** Interconecta diferentes redes independientes entre sí (por ejemplo, una LAN corporativa con Internet).
* **Características:**
  * Utiliza **direcciones IP** y tablas de enrutamiento para determinar la trayectoria óptima de los datos.
  * Permite la segmentación en subredes (*subnetting*), gestión de ancho de banda y priorización de tráfico.
  * Incorpora funciones avanzadas de seguridad como firewalls e inspección de tráfico.

---

### Resumen comparativo de dispositivos

| Dispositivo | Capa OSI | Identificación utilizada | Ámbito de trabajo | Manejo del tráfico |
| :--- | :--- | :--- | :--- | :--- |
| **Repetidor** | Capa 1 (Física) | Ninguna | Extensión de tramo | Regenera y amplifica la señal |
| **Hub** | Capa 1 (Física) | Ninguna | Red Local (LAN) | Difusión a todos los puertos (*Broadcast*) |
| **Switch** | Capa 2 (Enlace) | Dirección MAC | Red Local (LAN) | Reenvío directo al destino específico |
| **Router** | Capa 3 (Red) | Dirección IP | Entre redes distintas (LAN/WAN) | Enrutamiento estratégico de paquetes |

---

## 5. Protocolos de Comunicación

Un **protocolo de comunicación** es un conjunto estandarizado de reglas, pautas e instrucciones que rigen el intercambio de información entre sistemas informáticos.

### Tipos de protocolos
1. **Punto a punto:** Diseñados para transferir información directamente entre dos equipos. Gestionan el envío, recepción y retransmisión de mensajes hasta recibir un acuse de recibo (*ACK*).
2. **Comunicación entre redes:** Permiten la interacción de múltiples usuarios en una red local (LAN). Utilizan identificadores para cada terminal y coordinan el tráfico de forma organizada.
3. **De transmisión de paquetes:** Centran el control de la transmisión en los propios paquetes de datos y sus metadatos (en lugar de en los nodos). La información se fragmenta y viaja de manera independiente hasta el destino.
4. **TCP/IP:** Protocolo basado en la transmisión de paquetes. Divide la información en fragmentos independientes que eligen la ruta más eficiente según el estado de la red, garantizando estabilidad y velocidad.

---

## 6. TCP/IP vs. NetBIOS

### Modelo TCP/IP
Es la suite de protocolos estandarizada sobre la que se estructura Internet y la mayoría de las redes modernas. Divide los datos en paquetes, los transmite por rutas óptimas y los reensambla en el destino.

#### Capas del modelo TCP/IP
1. **Acceso a la Red (Enlace):** Administra la infraestructura física y los controladores de red (cables Ethernet, Wi-Fi, tarjetas NIC) transformando los datos digitales en señales físicas.
2. **Internet (Red):** Gestiona la direccionamiento, el enrutamiento y el flujo del tráfico entre distintas redes, asegurando la entrega eficiente de los paquetes.
3. **Transporte:** Proporciona una conexión de datos fiable de extremo a extremo (mediante la fragmentación, verificación y acuse de recibo de los paquetes).
4. **Aplicación:** Conjunto de protocolos que ofrecen servicios de red directos al usuario o a los programas (correo electrónico, la web, almacenamiento en la nube).

### NetBIOS
Es una interfaz de software y conjunto de servicios de nivel de sesión desarrollado originalmente para pequeñas redes locales (LAN). Proporciona:
* **Servicio de nombres:** Identifica dispositivos con nombres legibles en lugar de direcciones numéricas.
* **Servicio de datagramas:** Permite el envío de mensajes simples sin conexión.
* **Servicio de sesión:** Establece y mantiene conexiones orientadas a sesión para compartir archivos e impresoras.

### Diferencia clave

| Característica | NetBIOS | TCP/IP |
| :--- | :--- | :--- |
| **Alcance** | Redes locales pequeñas (LAN) o entornos heredados. | Estándar global (LAN, WAN e Internet). |
| **Nivel** | Interfaz de software / Capa de sesión. | Conjunto de protocolos multicapa completo. |
| **Escalabilidad** | Limitada; dependiente de difusión local. | Alta; diseñado para enrutamiento entre redes masivas. |

---

## 7. Estructura de un Paquete TCP/IP y "Flags"

Un paquete de datos en la pila TCP/IP se compone de un **encabezado IP**, un **encabezado TCP** (o UDP) y la carga útil de datos (**Payload**).

### Componentes del Encabezado IP
* **Versión:** IPv4 o IPv6.
* **Longitud de cabecera:** Tamaño del encabezado para su correcta lectura.
* **Tipo de servicio (ToS/QoS):** Define la prioridad del paquete.
* **Identificación y Banderas:** Controlan la fragmentación y reensamblado de paquetes grandes.
* **Tiempo de Vida (TTL):** Límite de saltos para evitar que los paquetes circulen indefinidamente.
* **Protocolo:** Especifica el protocolo de la capa superior (ej. TCP o UDP).
* **Suma de comprobación:** Valida la integridad del encabezado IP.
* **Direcciones IP:** Especifican el origen y el destino.

### Componentes del Encabezado TCP
* **Puertos de Origen y Destino:** Identifican las aplicaciones emisoras y receptoras.
* **Número de secuencia y Acuse de recibo (ACK):** Mantienen el orden de los datos y confirman la recepción.
* **Longitud de la cabecera y Ventana:** Especifican el tamaño del encabezado y el control de flujo de datos.
* **Suma de verificación:** Comprueba la integridad del segmento TCP.
* **Flags (6 bits de control):** Indicadores que gestionan el estado y comportamiento de la conexión TCP:
  * **SYN:** Inicia una nueva conexión (*Handshake*).
  * **ACK:** Confirma la recepción válida de un paquete o número de secuencia.
  * **FIN:** Solicita la finalización ordenada de la conexión.
  * **RST:** Reinicia la conexión de manera abrupta ante un fallo o error.
  * **PSH:** Solicita la entrega inmediata de los datos a la aplicación sin esperar a llenar el búfer.
  * **URG:** Indica que el segmento contiene información urgente que debe procesarse prioritariamente.

---

## 8. Clasificación de Redes según su Geografía

| Red | Denominación | Alcance y Descripción |
| :--- | :--- | :--- |
| **PAN** | *Personal Area Network* | **Corto alcance (pocos metros):** Conecta dispositivos de uso personal (smartphones, periféricos) mediante Bluetooth, USB o Zigbee. |
| **LAN** | *Local Area Network* | **Espacio limitado (oficinas, casas, edificios):** Ofrece alta velocidad y baja latencia mediante conexiones cableadas (Ethernet) o locales. |
| **WLAN** | *Wireless LAN* | **Variante inalámbrica de la LAN:** Utiliza ondas de radio (Wi-Fi), proporcionando movilidad, agilidad de despliegue y escalabilidad. |
| **MAN** | *Metropolitan Area Network* | **Área metropolitana (ciudades, campus universitarios):** Interconecta múltiples LANs dentro de una misma zona geográfica densa. |
| **WAN** | *Wide Area Network* | **Extensiones masivas (países, continentes):** Une subredes dispersas a través de fibra óptica, satélites y microondas. El ejemplo principal es **Internet**. |
| **GAN** | *Global Area Network* | **Cobertura global:** Infraestructura transcontinental que combina satélites y redes internacionales para dar soporte a la conectividad móvil mundial. |
| **VPN** | *Virtual Private Network* | **Red Lógica / Arquitectura Cifrada:** No definida por distancia física, sino por construir un túnel privado, autenticado y cifrado sobre una red pública (como Internet). |

---

## 9. Defina una red según su topología. Explicar distintas variantes** 

La topología de red define la estructura, forma o disposición (tanto física como lógica) en la que se organizan e interconectan los distintos nodos (computadoras, routers, switches) para transmitir datos dentro de una red. 

| Topología | Descripción | Ventaja | Desventaja |
| --- | --- | --- | --- |
| **Bus** | Todos los nodos se conectan a un único cable central continuo (denominado bus o backbone). Los datos viajan a lo largo del cable y cada dispositivo evalúa si el paquete va dirigido a él. | Es económica y sencilla de instalar en redes pequeñas. | Si el cable principal se rompe o falla, toda la red queda fuera de servicio. |
| **Estrella** | Todos los dispositivos están conectados individualmente a un nodo central concentrador, como un switch o un hub. Toda la información pasa obligatoriamente a través del equipo central antes de llegar a su destino. | Es fácil de administrar; si falla un cable o un equipo, el resto de la red sigue funcionando con normalidad. | Si el dispositivo central falla, toda la red se cae. Es la más utilizada en las redes LAN actuales. |
| **Anillo** | Los nodos se conectan en un circuito cerrado formando un anillo. La información viaja en una sola dirección (o en dos si es doble anillo), pasando de un nodo a otro hasta llegar al destinatario. | No presenta colisiones de paquetes de datos ya que el tráfico se gestiona mediante un pase de turno (token). | Si un solo nodo o enlace se interrumpe, se interrumpe la comunicación en toda la red. |
| **Malla** | Cada dispositivo está conectado directamente a uno o a varios nodos (malla parcial), o incluso a todos los demás nodos de la red (malla completa). | Altísima redundancia y tolerancia a fallos; si un enlace falla, los datos toman una ruta alternativa. | Es costosa y compleja de cablear y configurar. Muy usada en redes WAN y centros de datos. |
| **Árbol (o Jerárquica)** | Es una variación de la topología en estrella estructurada en niveles o jerarquías. Los nodos están conectados a switches secundarios que, a su vez, se conectan a un switch o router principal. | Facilita la expansión y escalabilidad de la red por departamentos o pisos. | Si falla un concentrador de nivel superior, todos los nodos dependientes de él pierden conexión. |
| **Híbrida (o Mixta)** | Combina dos o más topologías diferentes en una sola red (por ejemplo, una combinación de topología en estrella y topología en bus o malla). | Permite adaptar la red a las necesidades específicas de la infraestructura física del lugar. | Puede ser compleja de diseñar, mantener y solucionar fallos. |

<img src="https://uhu.es/antonio.barragan/files/archivos_usuarios/125/ethernet13.png" alt="topologia de redes" width="500">

https://www.cisco.com/c/en/us/support/docs/smb/routers/cisco-rv-series-routers/bis-network-topologies.html:**

---

## 10. Explicar el servicio de DHCP.**

El DHCP (Dynamic Host Configuration Protocol) es el servicio de red que se encarga de repartir el acceso a internet y a la red de forma automática. 

Cuando te conectás al Wi-Fi con el celular o la computadora, en vez de tener que configurar a mano la dirección IP, la máscara de red, la puerta de enlace y los servidores DNS, el servidor DHCP lo hace por vos en un par de segundos. Esto evita errores de configuración y logra que dos aparatos no terminen usando la misma IP al mismo tiempo. 

El proceso es simple y funciona en 4 pasos (conocidos como DORA): 

* **Discovery (Descubrimiento):** Tu dispositivo entra a la red y pregunta a todos los equipos: "¿Hay algún servidor DHCP disponible?".
* **Offer (Ofrecimiento):** El servidor DHCP responde: "Acá estoy, te puedo prestar esta dirección IP".
* **Request (Solicitud):** Tu dispositivo le dice: "Buenísimo, reservame esa IP".
* **Acknowledge (Confirmación):** El servidor responde: "Listo, ya es tuya" y te entrega la configuración completa.

Las direcciones IP no se entregan de forma permanente, sino en calidad de alquiler o préstamo por un tiempo determinado (por ejemplo, 8 horas o 24 horas).

* **Renovación:** Cuando se cumple aproximadamente el 50% del tiempo de concesión, el cliente le pide automáticamente al servidor extender el préstamo. Si el servidor responde, la concesión se renueva sin interrumpir la conexión.
* **Liberación:** Si el dispositivo se desconecta de la red o no renueva el alquiler al vencer el plazo, la IP vuelve al pool de direcciones disponibles para que el servidor pueda asignársela a otro equipo que se conecte más tarde. Esto es clave en redes públicas (como cafeterías o aeropuertos) con un flujo constante de usuarios.

https://datatracker.ietf.org/doc/html/rfc2131

---

## 11. Explicar el servicio de DNS.**

El servicio DNS (Domain Name System o Sistema de Nombres de Dominio) es básicamente la agenda telefónica de Internet. Su función principal es traducir los nombres de dominio que nosotros podemos recordar fácilmente, como google.com, a las direcciones IP numéricas que usan las computadoras y los routers para identificarse y comunicarse entre sí. Sin este servicio, tendríamos que memorizar largas cadenas de números para entrar a cualquier página web o usar cualquier servicio en red. 

El sistema funciona de forma distribuida y jerárquica para no colapsar. Cuando escribo una dirección web en el navegador, mi computadora primero revisa su propia memoria caché o le pregunta al servidor DNS de mi proveedor de internet. Si ese servidor no tiene la IP guardada, inicia una búsqueda por capas: le pregunta a un servidor Raíz, este lo deriva al servidor de la extensión del dominio (como .com o .ar), y este último lo manda al servidor autoritativo del sitio, que es el que finalmente tiene la IP exacta. Una vez que obtiene esa dirección IP, me la devuelve, mi equipo la guarda temporalmente en la caché para no tener que buscarla de nuevo más tarde, y el navegador abre la página. 

https://www.cloudflare.com/learning/dns/what-is-dns/

---

## 12. Explicar las tecnologías Wireless, y sus estándares.**

Las tecnologías wireless o inalámbricas son aquellas que permiten la comunicación y la transferencia de datos entre dispositivos sin necesidad de un medio físico como un cable, utilizando para ello ondas electromagnéticas (radiofrecuencia o infrarrojos). Estas tecnologías abarcan desde conexiones de muy corto alcance para periféricos personales, pasando por redes locales, hasta enlaces de gran cobertura para telefonía e internet móvil. 

Los estándares de las redes inalámbricas más comunes están regulados principalmente por el instituto IEEE bajo la familia 802.11, conocida popularmente como Wi-Fi. A lo largo de los años, estos estándares han ido evolucionando para ofrecer mayor velocidad, capacidad de dispositivos conectados y menor interferencia, utilizando las bandas de frecuencia de 2.4 GHz, 5 GHz y recientemente 6 GHz: 

* **IEEE 802.11b / 802.11g:** Operan en la frecuencia de 2.4 GHz. Alcanzan velocidades teóricas de 11 Mbps y 54 Mbps respectivamente. Fueron las bases del Wi-Fi masivo, aunque sufren de bastantes interferencias por compartir frecuencia con otros electrodomésticos. 
* **IEEE 802.11n (Wi-Fi 4):** Introdujo el uso de doble banda (2.4 GHz y 5 GHz) y la tecnología MIMO (múltiples antenas), logrando velocidades de hasta 600 Mbps. 
* **IEEE 802.11ac (Wi-Fi 5):** Funciona exclusivamente en la banda de 5 GHz, ofreciendo mayor ancho de banda y velocidades superiores a 1 Gbps, reduciendo la saturación. 
* **IEEE 802.11ax (Wi-Fi 6 / 6E):** Diseñado para entornos densos con muchos dispositivos conectados. Mejora la eficiencia energética, aumenta la velocidad y reduce la latencia. La versión 6E suma el uso de la banda de 6 GHz. 
* **IEEE 802.11be (Wi-Fi 7):** La generación más reciente, orientada a aplicaciones de altísima velocidad y bajísima latencia (como streaming en 8K o realidad virtual), superando los 30 Gbps teóricos.

Además de Wi-Fi, existen otros estándares inalámbricos importantes según su alcance y aplicación: IEEE 802.15.1 (Bluetooth) para redes personales de corto alcance (PAN) y bajo consumo; IEEE 802.15.4 (Zigbee / Z-Wave) utilizado principalmente para domótica y dispositivos IoT; e IEEE 802.16 (WiMAX) diseñado para redes de área metropolitana inalámbricas de gran cobertura.  

https://standards.ieee.org/ieee/802.11/7028/

---

## 13. ¿Qué es un Proxy?**

Un Proxy (o servidor proxy) es un equipo o programa informático que actúa como intermediario entre un cliente (por ejemplo, mi computadora o navegador) y el servidor de destino al que quiero acceder en Internet. Cuando tengo configurado un proxy, en lugar de conectarme directamente a una página web, mi dispositivo le envía la solicitud al proxy, y este la procesa, la reenvía al sitio web de destino, recibe la respuesta y finalmente me la transmite de vuelta. 
Este intermediario se utiliza principalmente por tres motivos: seguridad, control y rendimiento. En primer lugar, ayuda a proteger la privacidad de la red interna porque oculta la dirección IP real del cliente y la reemplaza por la del propio proxy. En segundo lugar, se usa mucho en entornos corporativos o escolares para filtrar y bloquear el acceso a ciertas páginas web no permitidas (como redes sociales o juegos). Por último, mejora el rendimiento y la velocidad de navegación mediante el almacenamiento en caché; es decir, guarda una copia de los sitios web más visitados para entregarlos más rápido cuando varios usuarios piden la misma información, ahorrando así ancho de banda.

https://developer.mozilla.org/es/docs/Web/HTTP/Proxy_servers_and_tunneling 

---

## 14. Explicar el protocolo Spanning tree.**

El protocolo Spanning Tree (STP, por sus siglas en inglés Spanning Tree Protocol y estandarizado como IEEE 802.1D) es un protocolo de red de capa 2 (enlace de datos) que sirve para prevenir bucles o bucles infinitos en redes de conmutación (LANs) que cuentan con enlaces redundantes. Cuando conectamos varios switches entre sí con múltiples cables para tener respaldo ante cualquier falla, si no se usa STP, las tramas de difusión (broadcast) quedan circulando indefinidamente entre los dispositivos. Esto genera una tormenta de broadcast que satura los enlaces y colapsa la red en pocos segundos. 
Para solucionar esto, el protocolo Spanning Tree analiza la topología física de la red y calcula una ruta lógica sin bucles. Lo hace eligiendo un switch principal llamado Puente Raíz (Root Bridge) y determinando cuáles son los caminos más cortos hacia él. Después, deja activos solo los puertos necesarios para la comunicación principal y bloquea automáticamente de forma lógica aquellos puertos sobrantes. Si en algún momento uno de los cables o switches activos falla, STP detecta el corte y desbloquea el puerto que estaba de respaldo para restaurar la conectividad automáticamente sin interrumpir el funcionamiento de la red. 

https://standards.ieee.org/ieee/802.1D/3387/ 

---

## 15. Explicar el protocolo de comunicaciones OSPF.**

OSPF (Open Shortest Path First o Primero el Camino Más Corto) es un protocolo de enrutamiento dinámico de tipo estado de enlace (link-state), utilizado en redes IP de interior (IGP) para determinar de forma automática la ruta más eficiente por la que deben viajar los paquetes de datos entre distintos routers dentro de una misma red corporativa o de un sistema autónomo. 
A diferencia de protocolos más simples que solo cuentan la cantidad de saltos (routers por los que pasa el paquete), OSPF analiza la topología completa de la red y calcula la mejor ruta basándose en el costo, el cual se determina a partir del ancho de banda disponible en los enlaces. Para lograr esto, cada router genera y comparte mensajes llamados LSA (Link-State Advertisements) para informar a sus vecinos sobre el estado de sus conexiones. Con toda esa información, cada router construye un mapa completo de la red y utiliza el algoritmo Dijkstra (SPF) para calcular el camino más corto hacia cada destino. Además, OSPF organiza la red en áreas (siendo el Área 0 el backbone o núcleo obligatorio) para jerarquizar el tráfico, reducir el consumo de memoria en los routers y mantener la red estable y escalable.
https://datatracker.ietf.org/doc/html/rfc2328 

---

## 16. Explicar el protocolo ARP.**

El protocolo ARP (Address Resolution Protocol o Protocolo de Resolución de Direcciones) es un protocolo de red clave que trabaja en el nivel de enlace de datos y de red, cuya función principal es asociar una dirección IP conocida (dirección lógica) con su correspondiente dirección MAC (dirección física de la placa de red) dentro de una misma red local. Dado que los paquetes en una red Ethernet local no se entregan usando direcciones IP sino mediante las direcciones MAC impresas en el hardware de las tarjetas de red, se necesita a ARP para hacer esa traducción antes de enviar cualquier dato. 
El funcionamiento de ARP es muy directo. Cuando un dispositivo (como mi computadora) quiere enviarle datos a otro equipo en la misma red local pero solo conoce su dirección IP, envía una solicitud ARP en modo difusión (broadcast) a toda la red preguntando: "¿Quién tiene esta dirección IP y cuál es su dirección MAC?". Todos los equipos de la red reciben la pregunta, pero únicamente el dispositivo que posee esa IP responde de forma individual (unicast) enviando su dirección MAC física. Una vez que mi equipo recibe esa respuesta, guarda la asociación entre la IP y la MAC en una tabla temporal llamada memoria caché ARP. De esta forma, para los siguientes envíos no necesita volver a consultar a la red, lo que optimiza el tráfico y acelera la comunicación. 

https://datatracker.ietf.org/doc/html/rfc826 

---

## 17. ¿Qué es un Firewall?
Un firewall (o cortafuegos) es un sistema de seguridad de red que monitorea, filtra y controla el tráfico de datos entrante y saliente basándose en reglas preestablecidas para bloquear accesos no autorizados. 
Por ejemplo una empresa puede configurar un firewall para permitir que los usuarios naveguen por Internet, pero bloquear conexiones externas no autorizadas hacia las computadoras de su red interna. 

**Fuente:** [Fortinet - ¿Qué es un firewall?](https://www.fortinet.com/lat/resources/cyberglossary/firewall)

---

## 18. ¿Qué es una DMZ?

Una **DMZ (Zona Desmilitarizada)** es un término que proviene del concepto militar de "zona desmilitarizada", una zona de separación entre partes enfrentadas. En redes informáticas se utiliza de forma similar para definir una zona intermedia entre una red interna confiable e Internet, ayudando a proteger la red interna.

Por ejemplo, una empresa puede colocar su servidor web en una DMZ. Los usuarios de Internet pueden acceder al servidor web, pero **no directamente a las computadoras de la red interna**.

**Fuente:** [NIST - Demilitarized Zone](https://csrc.nist.gov/glossary/term/demilitarized_zone)

---

## 19. ¿Qué es un Gateway?

Un **Gateway (puerta de enlace)** es un dispositivo o punto de una red que permite la **comunicación con otra red**. En una red doméstica, normalmente el router cumple la función de gateway y permite que los dispositivos de la red local puedan comunicarse con Internet.

Cisco también señala que un gateway puede conectar redes diferentes y, cuando es necesario, traducir protocolos entre ellas.

Por ejemplo, una notebook con IP `192.168.1.20` puede tener como gateway predeterminado el router `192.168.1.1`. Cuando necesita acceder a Internet, envía hacia ese gateway el tráfico destinado fuera de su red local.

**Fuente:** [Cisco - What Is a Network Gateway?](https://www.cisco.com/site/us/en/learn/topics/networking/what-is-a-network-gateway.html)

---

## 20. Según Microsoft, ¿qué significa NBL?

**Nota:** La sigla correspondiente a la tecnología descrita es NLB (Network Load Balancing), no NBL.

**NLB (Network Load Balancing)** significa **Equilibrio de carga de red**. Es una tecnología de Windows Server que permite **distribuir el tráfico de red entre varios servidores**, agrupándolos en un clúster virtual.

Esto ayuda a mejorar la disponibilidad y el rendimiento de servicios como servidores web, FTP, proxy o VPN.

Por ejemplo, si una aplicación web funciona en tres servidores, NLB puede repartir las solicitudes de los usuarios entre esos servidores, evitando que todo el trabajo recaiga sobre uno solo. Si uno queda fuera de servicio, la carga puede redistribuirse entre los restantes.

**Fuente:** [Microsoft Learn - Network Load Balancing](https://learn.microsoft.com/es-es/windows-server/networking/technologies/network-load-balancing)

---

## 21. Tipos de enlace: MPLS, LAN to LAN, microondas y VSAT

### a. Explique cada uno de estos tipos de enlace

**MPLS (Multiprotocol Label Switching):** tecnología utilizada por proveedores para conectar distintas sedes de una organización mediante una red privada. Permite priorizar determinados tipos de tráfico mediante QoS, por ejemplo, dando prioridad a voz o aplicaciones críticas.

**LAN to LAN:** conexión que permite unir dos redes LAN ubicadas en lugares diferentes, haciendo que puedan comunicarse entre sí. El proveedor generalmente ofrece el enlace como un servicio punto a punto.

**Microondas:** enlace inalámbrico que utiliza ondas de radio para comunicar dos puntos. Normalmente requiere línea de vista entre las antenas. Puede ofrecer buena velocidad sin necesidad de realizar cableado entre ambos lugares.

**VSAT (Very Small Aperture Terminal):** comunicación mediante satélite utilizando pequeñas antenas terrestres. Su principal ventaja es poder llegar a lugares remotos donde no existe infraestructura terrestre. Como desventaja, suele tener mayor latencia, especialmente cuando utiliza satélites geoestacionarios.

### b. Agregue dos tipos de enlaces no mencionados anteriormente

**Fibra óptica:** transmite información mediante pulsos de luz. Permite velocidades y capacidades muy altas, baja latencia y grandes distancias. Es una de las mejores alternativas cuando existe infraestructura disponible.

**4G/5G:** utiliza redes móviles para proporcionar conectividad de datos. Es fácil y rápido de implementar donde existe cobertura y puede ser utilizado como enlace principal o de respaldo.

### c. Ranking de enlaces

El siguiente ranking es **orientativo**, porque el resultado real depende del proveedor, ubicación, ancho de banda contratado, SLA, infraestructura existente y otros factores.

Se utiliza una escala del **1 al 6, siendo 1 la mejor posición** para cada criterio.

| Criterio | 1 (mejor) | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|---|
| Más económico | 4G/5G | Microondas | LAN to LAN | Fibra | MPLS | VSAT |
| Performance | Fibra | LAN to LAN | MPLS | Microondas | 4G/5G | VSAT |
| Mayor capacidad | Fibra | LAN to LAN | MPLS | Microondas | 4G/5G | VSAT |
| Configuración de restricciones / QoS | MPLS | LAN to LAN | Fibra | Microondas | 4G/5G | VSAT |
| Mayor distancia | VSAT | MPLS | Fibra | 4G/5G | Microondas | LAN to LAN |
| Menor esfuerzo de configuración | 4G/5G | VSAT | LAN to LAN | Fibra | MPLS | Microondas |

### d. Elección del tipo de enlace según el escenario

**1. Conectividad de varios call centers con un data center central.**

Elegiría **MPLS** porque permite conectar múltiples sedes y aplicar QoS para priorizar tráfico sensible a latencia, como VoIP. En un call center esto es especialmente importante para mantener la calidad de las llamadas.

**2. Conectar los datos de los pozos petroleros durante 15 minutos por día.**

Elegiría **VSAT** porque los pozos pueden encontrarse en lugares remotos sin fibra, cableado o cobertura celular. Si solamente se necesita transmitir datos durante un período corto del día, la mayor latencia del satélite puede ser aceptable.

**3. Comunicar dos edificios enfrentados en la misma calle.**

Elegiría un enlace de **microondas punto a punto** porque la corta distancia y la posibilidad de tener línea de vista entre ambos edificios permiten establecer un enlace inalámbrico de buena capacidad sin tener que instalar un cable atravesando la calle.

**Fuentes:**

- [Cisco - Conceptos de redes y MPLS](https://www.cisco.com/c/es_mx/support/docs/multiprotocol-label-switching-mpls/mpls/4649-mpls-faq-4649.html)
- [Cloudflare - ¿Qué es la capa de red?](https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-network-layer/)

---

## 22. Describir la tecnología LTE

**LTE (Long Term Evolution)** es una tecnología de banda ancha móvil que permite transmitir datos a alta velocidad mediante una red celular. Es la tecnología que se convirtió en la base de gran parte de las redes conocidas comercialmente como **4G**.

Por ejemplo, cuando un celular muestra `4G` o `LTE`, normalmente está utilizando una red LTE del operador para navegar por Internet, enviar datos o utilizar diferentes servicios.

**Fuentes:**

- [IEEE - Long Term Evolution (LTE)](https://technav.ieee.org/topic/lte/)
- [3GPP - Organización responsable de las especificaciones de LTE](https://www.3gpp.org/article/OFDM)

---

## 23. Explique la solución de Microsoft Teams

**Microsoft Teams** es una plataforma de comunicación y colaboración de Microsoft. Permite que personas de una empresa, institución o grupo puedan **chatear, realizar videollamadas y reuniones, compartir archivos y trabajar en equipo desde un mismo lugar**.

Una alternativa **Open Source** es Mattermost, que puede instalarse en servidores propios, dando a la organización mayor control sobre sus datos.

Otra alternativa comercial es Slack, que también busca facilitar la comunicación y el trabajo colaborativo.

Por ejemplo, un equipo de trabajo puede crear un grupo en Teams, conversar mediante chat, compartir documentos y realizar una videollamada para discutir un proyecto sin salir de la misma plataforma.

**Fuentes:**

- [Microsoft - ¿Qué es Microsoft Teams?](https://support.microsoft.com/es-es/teams/platform/what-is-microsoft-teams)
- [Mattermost - Plataforma de colaboración](https://mattermost.com/)
- [Slack - Plataforma de comunicación y colaboración](https://slack.com/)

---

## 24. ¿Qué significa aplicar calidad en un enlace MPLS?

Aplicar **calidad en un enlace MPLS** significa utilizar mecanismos de **Calidad de Servicio (QoS)** para **dar prioridad a determinados tipos de tráfico** sobre otros.

Por ejemplo, se puede dar mayor prioridad a llamadas de voz o videoconferencias que a una descarga de archivos, para mantener una buena comunicación cuando la red está congestionada.

**Fuente:** [Cisco - MPLS Quality of Service (QoS)](https://www.cisco.com/c/en/us/td/docs/routers/ios-xe/mpls/mpls/m-mp-qos-xe.html)

---


**33. Experiencia en Redes:**
### Sergio Lezcano: 

No tengo experiencia. 

### Norberto Oscar Roth:

Mi experiencia con redes es principalmente práctica, adquirida a lo largo de los años por la necesidad de conectar equipos y resolver problemas de conectividad. Algunos ejemplos:

- En PC antiguas, cuando las placas de red no venían integradas, tuve que averiguar qué placa necesitaba, conseguirla e instalarla. Como vivía en City Bell (La Plata), a veces tenía que buscar componentes específicos en lugares como Galería Jardín o en ferreterias cercanas para evitar viajar.

- Aprendí de manera práctica sobre cables de red, coaxiales, fichas y conectores, consultando también a amigos que se dedicaban a reparación de PC. Según el caso, compraba los componentes necesarios o directamente cables ya armados.

- Realicé configuraciones básicas de routers y redes hogareñas con distintos proveedores, como Fibertel y Telefónica, además de conectar equipos mediante Ethernet y Wi-Fi.

- Trabajé en un "Ciber" con varias PC conectadas en red para juegos. Participaba en la conexión de los equipos y utilizábamos un software centralizado para administrar las PC y controlar el tiempo de uso de cada usuario.

- En el Ministerio de Agricultura, Ganadería y Pesca trabajé dentro de una red privada del Estado Nacional. Para desarrollar y publicar proyectos debía configurar las conexiones necesarias para acceder a los distintos ambientes (desarrollo/test y producción) y ejecutar las aplicaciones en servidores propios del Ministerio.
En ese mismo trabajo, cuando trabajaba de forma remota una vez por semana, accedía a la red privada mediante FortiClient. También, cuando la conexión Wi-Fi de la oficina era muy lenta, utilizaba un adaptador USB-Ethernet (RJ45) para conectar la notebook directamente a la red cableada.

- Actualmente utilizo y configuro principalmente redes Wi-Fi y conexiones Bluetooth entre notebooks, celulares, auriculares, smartwatch, Smart TV, Apple TV y decodificadores de Flow.
Para ampliar la cobertura Wi-Fi de mi casa sin realizar cableado, utilizo un extensor de rango TP-Link TL-WA850RE como repetidor de señal.
También utilizo aplicaciones del celular como controles remotos para distintos dispositivos y realizo casting de contenido hacia Smart TV. Además tengo experiencia vinculando dispositivos como AirTag y otros equipos inteligentes mediante Bluetooth o Wi-Fi.

### María Florencia Quintana: 

No tengo ninguna experiencia previa en redes. Lo único que se de redes es la teoría de clase y algunos protocolos que vimos en la materia de Backend.





