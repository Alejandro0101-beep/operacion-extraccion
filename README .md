# Operación Extracción

Este es mi proyecto para [NOMBRE DEL CURSO]. Hice un juego de disparos en primera persona que se juega en el navegador, usando JavaScript y Three.js. La historia es simple: el jugador está en un hospital abandonado lleno de infectados y tiene que llegar al helipuerto para extraerse.


## Qué hace el juego

El jugador recorre el hospital zona por zona: almacén, pasillos, terraza y así hasta la última sala. En cada zona salen zombis y hay cajas de munición repartidas. En la sala H3 puse varias cajas extra para que se pueda llegar bien armado a la parte final.

Al final está el panel que abre la barrera. Cuando se activa aparecen el Tank y una horda de 20 zombis, y el jugador solo tiene un cohete de bazuca para esa pelea. Si mata al Tank, puede subir por la rampa al helipuerto y gana. Si un zombi lo toca, pierde.

## Controles

- W A S D: moverse
- Shift: correr
- Mouse: mirar
- Clic izquierdo: disparar
- 1, 2, 3: pistola, rifle y bazuca
- R: recargar
- E: recoger munición y activar el panel
- ESC: pausar


## Carpetas

- `index.html`: todo el código del juego
- `modelos/`: los .glb del zombi, el tank y las armas
- `texturas/`: las imágenes del suelo, las paredes, etc.
- `sonidos/`: la música y los efectos

## Cómo lo hice

- El mapa está armado con bloques, y cada bloque sólido tiene su caja de colisión.
- Los zombis usan un mapa de celdas con búsqueda en anchura (BFS) para encontrar el camino hacia el jugador. Cuando tienen línea recta libre, van directo.
- Los disparos son rayos que revisan si le dieron a algún enemigo. La bazuca lanza un cohete que explota y mata lo que esté cerca.
- Las zonas y oleadas dependen de una variable `etapa`: al entrar a una zona nueva se generan sus zombis.
- Al principio el mouse se trababa. Lo solucioné acumulando el movimiento y aplicándolo una sola vez por frame.

## Recursos externos

- Three.js v0.180.0: https://threejs.org
- Modelos 3D: [pistola:https://sketchfab.com/3d-models/pistol-9mm-semi-auto-7d363c3cf2f74a9a9fb0cab9874898eb? / zombie: https://www.fab.com/listings/72f19ad6-45c7-4fd9-9659-145371a0c22d? / bazoka: https://sketchfab.com/3d-models/bazooka-9d3011681c844967a7afff3df54b7e55 / tank: https://sketchfab.com/3d-models/left-4-dead-2-tank-rig-10b492f7646c411fb9bba72c51e79e50#download ]
- Texturas: [de dónde, enlace]
- Música y efectos de sonido: [sonido de tank: https://www.youtube.com/watch?v=cosC5YqHXlc / sonido general: https://www.youtube.com/watch?v=bJmLzn4aqLo&list=RDbJmLzn4aqLo&start_radio=1]
- Uso de IA: [la use para reestructurar el codigo y algunos errores y para obtener paginas que me den los modelados de forma gratuita para el proyecto]
