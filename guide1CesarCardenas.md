# Study Guide: Chapter 1 - Computer Networks: A Systems Approach

## Introduction
Welcome to the study guide for Chapter 1 of the textbook "Computer Networks: A Systems Approach" by Larry Peterson and Bruce Davie. This guide will help you understand the fundamental concepts of computer networks and provide you with questions and exercises to reinforce your understanding. Let's get started!

### Required reading
Sections: 1.1, 1.2, 1.3 and 1.5 

## 1. Building a Scalable Network
- What are the key considerations when building a scalable network?

Para construir una red escalable debemos tener en cuenta varios factores,entre estos encontramos la capacidad de expansión para acomodar un mayor número de equipos, el uso de recursos, la facilidad de administración y la capacidad para tener y conservar un rendimiento adecuado a medida que la red crece.

- Explain the concept of network scalability and why it is important.

La escalabilidad de redes se refiere a la capacidad de la red para crecer y adaptarse a las demandas cambiantes sin empeorar su rendimiento. Esto es importante porque permite ajustar la red a medida que las necesidades cambian o aumentan, evitando costos inecesario o que se pudieron preveer.

- Provide examples of different applications that require a scalable network.

Algunos de los ejemplos de aplicaciones que requieren redes escalables incluyen servicios en la nube, redes sociales, aplicaciones de streaming de video y empresas en crecimiento que necesitan agregar más usuarios y dispositivos a su red.

- Why does a network need to be cost-effective, fair, and have robust connectivity?

Una red debe ser costeable para evitar gastos grandes innecesarios, justa para que todos los usuarios tengan acceso equitativo a los recursos de la red y por ultimo tener conectividad robusta para garantizar la disponibilidad del servicios.

- Discuss the challenges involved in designing a network that can support various applications.

Se puede hablar de las diferentes necesidades de aplicaciones y las cuales requieren diferentes niveles de ancho de banda, latencia y calidad de servicio. Esto implica el tráfico, la priorización de datos y la asignación eficiente de recursos.


## 2. Computer Network Architecture
- Define computer network architecture in terms of layers and protocols

La arquitectura de redes de computadoras se basa en division de las funciones de la red en algo llamado capas. Cada una de estas capas se ocupa de una parte específica entre la comunicación de datos y utilizacion de protocolos para el intercambio de información. Algunos ejemplos de arquitecturas de capas puede ser el modelo OSI y el modelo TCP/IP.

- Why are layers and protocols important?

Las capas y los protocolos son importantes porque proporcionan una estructura organizada para el diseño de redes y garantizan la interoperabilidad entre los dispositivos y los diversos sistemas existentes.

- What is encapsulation, multiplexing and demultiplexing?

Encapsulation: Es el proceso de empaquetar datos en una estructura específica que incluye información de control y encabezados, que permite que los datos viajen a través de la red.
Multiplexing: Es la técnica de combinar múltiples flujos de datos en un solo canal de comunicación para que la transmisión sea eficiente.
Demultiplexing: Es el proceso inverso de multiplexing, donde se separan los flujos de datos combinados para dirigirlos a las capas y aplicaciones especificas.

- Discuss the role of each layer in the OSI and Internet protocol stack.

En el modelo OSI, cada capa tiene una función específica en el proceso de comunicación. En el modelo TCP/IP, las capas se agrupan en cuatro niveles: Aplicación, Transporte, Internet y Enlace de Datos. Cada capa tiene una función clara, como la capa de aplicación para aplicaciones de usuario, la capa de transporte para controlar la comunicación extremo a extremo, la capa de internet para enrutamiento y la capa de enlace de datos para la transmisión de datos físicos.

- Provide examples of protocols used at each layer of the TCP/IP protocol stack.

Entre los ejemplos de protocolos en el modelo TCP/IP incluyen HTTP y FTP en la capa de Aplicación, TCP y UDP en la capa de Transporte, IP en la capa de Internet y Ethernet en la capa de Enlace de Datos.


## 3. Performance
- Why is important to keep track of the performance of a network?

Es importante monitorear el rendimiento de la red para garantizar que cumpla con los requisitos de calidad de servicio, identificar problemas y cuellos de botella, y tomar medidas proactivas para mantener un rendimiento óptimo.

- What are the main metrics we use to measure network performance?

Las métricas comunes para medir el rendimiento de la red incluyen el ancho de banda, la latencia, la pérdida de paquetes, la disponibilidad, la utilización de recursos y la calidad de servicio (QoS).

- Give some examples of the challenges of using different metrics in high speed networks


En redes de alta velocidad, es más difícil medir con precisión la latencia debido a la velocidad de los paquetes, y la pérdida de paquetes puede tener un impacto más significativo en la calidad del servicio. Además, la gestión de recursos y la escalabilidad son desafíos críticos en redes de alta velocidad para mantener un rendimiento consistente.


## Exercises
1. Calculate the total time required to transfer a 1000-KB file in the following cases, assuming an RTT of 50 ms, a packet size of 1 KB data, and an initial 2 × RTT of “handshaking” before data is sent:

    a. The bandwidth is 1.5 Mbps, and data packets can be sent continuously.
    
    1000 kb = 8,192 bits
    tp=5.46 ms
    tprop= 1/2 RTT
    T=(2.5*50)+1000*5.46
    T=5.58 seg

    b. The bandwidth is 1.5 Mbps, but after we finish sending each data packet we must wait one RTT before sending the next.
    
    T=5.58+99.9
    T=105.48 seg
    
    c. The bandwidth is “infinite,” meaning that we take transmit time to be zero, and up to 20 packets can be sent per RTT.
    
    1000/20 = 50
    necesitamos 1/2 RTT
    T=51.5(50)
    T=2.57 seg
    
    
2. For each of the following operations on a remote file server, discuss whether they are more likely to be delay sensitive or bandwidth sensitive:

    a. Open a file.
    
    Esta es mas sensible a los retrasos ya que hace una conexión con el servidor de archivos remoto y verificar los permisos del usuario

    b. Read the contents of a file.
    
    Esta puede ser ambos dependiendo del archivo y la velocidad de la red, por ejemplo si el archivo es grande este sera mas sensible al ancho de banda
    
    c. List the contents of a directory.
    
    Esta es mas sensible a los retrasos ya que hace una conexion con el servido por los datos.
    
    d. Display the attributes of a file.
    
    Esta es mas sensible a los retrasos ya que hace una conexión con el servidor por los datos que se necesitan rapidamente.
    
    
3. Suppose a host has a 1-MB file that is to be sent to another host. The file takes 1 second of CPU time to compress 50% or 2 seconds to compress 60%.

    a. Calculate the bandwidth at which each compression option takes the same total compression + transmission time.
    
    Tiempo total (TT) = Tiempo de compresión (CT) + Tiempo de transmisión 
    TT = RTT + (1 / Ancho de banda) x Tamaño de transferencia
    Para una compresión del 50%
    Tamaño de transferencia = 0.5 MB
    Tiempo de compresión = 1 seg
    TT = RTT + (1 / Ancho de banda) x 0.5 MB
    TT = RTT + (0.50 MB / Ancho de banda)
    TT = TC + RTT + (0.5 MB /Ancho de banda)
    TT = 1 seg + RTT + (0.5 MB / Ancho de banda)
    Para una compresión del 60%
    Tamaño de transferencia = 0.4 MB
    Tiempo de compresión = 2 seg
    TT = RTT + (1 / Ancho de banda) x 0.4 MB
    TT = RTT + (0.40 MB / Ancho de banda)
    TT = TC + RTT + (0.5 MB /Ancho de banda)
    TT = 2 seg + RTT + (0.4 MB / Ancho de banda)
    Cálculo de ancho de banda 
    Para este cálculo se necesita usar las ecuaciones anteriores e igualarlas y calcular el ancho de banda: 
    1 seg + (0.5 MB / ancho de banda) = 2 seg + (0.4 MB / ancho de banda)
    (0.5 MB / ancho de banda) - (0.40 MB / ancho de banda) = 2 seg - 1seg
    0.1 MB / ancho de banda = 1 seg
    Ancho de banda = 0.1 MB/s 

    
    b. Explain why latency does not affect your answer
    La latencia no afecta la respuesta porque no está relacionada con el ancho de banda o la velocidad de transferencia de datos, más bien se refiere al retraso entre el envío y la recepción de datos.

4. . Discuss the relative performance needs of the following applications in terms of average bandwidth, peak bandwidth, latency, jitter, and loss tolerance:
    
    a. File server.
    
    Servidor de archivos: Las necesidades de rendimiento de un servidor de archivos dependen del número de usuarios que acceden a él y del tamaño de los archivos que se transfieren. 
    Requiere
    •Alto ancho de banda promedio para transferir archivos grandes rápida y eficientemente. 
    •Baja latencia para garantizar que los usuarios puedan acceder a los archivos rápidamente. 

    
    
    b. Print server.
    
    Servidor de impresión: Las necesidades de rendimiento de un servidor de impresión dependen del número de usuarios que acceden a él y del tamaño de los trabajos de impresión que se envían a él. 
    Requiere
    •Bajo ancho de banda promedio porque los trabajos de impresión suelen ser pequeños en tamaño.
    •Baja latencia para garantizar que los trabajos de impresión se procesen rápidamente.

    
    c. Digital library.
    
    Biblioteca digital: Las necesidades de rendimiento de una biblioteca digital dependen del número de usuarios que acceden a ella y del tamaño de los objetos digitales que se acceden.
    Requiere
    •Alto ancho de banda promedio para transferir objetos digitales grandes rápidamente. 
    •Baja latencia para garantizar que los usuarios puedan acceder a los objetos digitales rápidamente. 

    
    
    d. Routine monitoring of remote weather instruments.
    
    Monitoreo rutinario de instrumentos meteorológicos remotos: Las necesidades de rendimiento del monitoreo rutinario dependen de la frecuencia con la que se recopilan los datos y del tamaño de los datos que se transmiten. 
    Requiere
    •Bajo ancho de banda promedio porque los datos suelen ser pequeños en tamaño. 
    •Baja latencia para garantizar que los datos se recopilen en tiempo real. 

    
    e. Voice.
    
    Voz: Las necesidades de rendimiento de la comunicación por voz dependen del número de partes involucradas y la calidad del audio que se transmite. 
    Requiere
    •Bajo ancho promedio, baja latencia y tolerancia a la pérdida.

    
    f. Video monitoring of a waiting room.
    
    Monitoreo por video en una sala espera: Las necesidades rendimiento del monitoreo por video dependen del número cámaras involucradas y calidad del video que se transmite. El monitoreo por video 
    Requiere
    •Alto ancho promedio, baja latencia y tolerancia a la pérdida.

    
    g. Television broadcasting.
    
    
    Transmisión televisiva: Las necesidades rendimiento televisivo dependen del número receptores involucrados y calidad del video que se transmite. 
    Requiere
    •Alto ancho promedio, baja latencia y tolerancia a la pérdida.



```python

```
