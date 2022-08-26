# Flow2-NodeRed
En este repositorio se muestran los archivos para realizar el flow2 del curso de NodeRed de código IoT.

## Introducción

Este ejercicio permite demostrar el uso de el nodo function en NodeRed. Este ejecicio consiste en darle un formato legible para humanos al timestamp y mostrar la fecha en la sección debug. Se usaran los siguentes nodos

- Inject

   > El nodo **inject** inyecta datos al flow ya sea manualmente o por un intervalo
- Debug

   > El nodo **debug** visualiza el proceso en la barra de debug
- Function
 
   > El nodo **function** ejecuta una función de JavaScript en el mensaje que esta siendo recibido 

### Material Necesario

Para realizar este ejercicio necesitaras lo siguente

- [Ubuntu 20.04](https://ubuntu.com/download/desktop)
- [NodeJs](https://nodejs.org/en/)
  - [NPM](https://www.npmjs.com/)
  - [NodeRed](https://nodered.org/)

### Material de referencia

- [Instalación de Virtual Box](https://edu.codigoiot.com/course/view.php?id=810)
  - [Instalación de Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
- [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817)
- [Intoducción a NodeRed](https://edu.codigoiot.com/course/view.php?id=278)

# Instrucciones

## Requisitos previos

1. Tener instalado todo el software listado en el **Material necesario**
2. Arrancar NodeRed escribiendo el comando `node-red` en la terminal
3. Abrir aplicacion de NodeRed en un navegador con la dirección ["http://localhost:1880"](http://localhost:1880/#flow/d0319225ca32761b)

## Instrucciones de ejecución

1. Se arrastra un nodo de **inject** y se configura de la siguente forma
   - msg.payload = timestamp
   - Repeat = interval
   - every 1 second
2. Se arrastra un nodo de **function** y se le escribe el siguente código
   - `var date = new Date(msg.payload)`
     `msg.payload = date.toString();`
     `return msg;`
3. Se conecta el nodo **inject** y el nodo **function**
4. Se arrastra un nodo de **Debug**
6. Se conecta el nodo de **debug** con el nodo de **function**
5. Se guarda el flow oprimiendo el botón **Deploy**

# Resultados 

El flow debera verse como el flow de la siguiente imagen

![resultados del flow](https://github.com/hugoescalpelo/Flow2-NodeRed/blob/main/Screenshot%20from%202022-08-26%2009-42-57.png)

## Evidencias

[Repositorio](https://github.com/davidGalaviz/Flow2-NodeRed)

# Creditos

Desarrollado por David Galaviz

[GitHub](https://github.com/davidGalaviz)
