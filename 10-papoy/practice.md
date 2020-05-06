---
title: Práctica Final - Batalla Naval
layout: practice
permalink: /practice/papoy
---

# Práctica Final: Batalla Naval

Crear un juego online para jugar a la batalla naval.

![Batalla Naval](../10-papoy/battleship.jpg)

## Flujo de pantallas

1. Login: al ingresar a la página, se pedirá al usuario que se autentique
  - La autenticación sera por medio de Facebook.
2. Home: una vez autenticado, podrá jugar y ver el historial con algunas estadísticas de las partidas jugadas.
  - Para jugar habrá un botón "Play" que esperará un contrincante y los llevara al juego
  - Bonus: historial mostrando el usuario contrincante, resultado (ganado, perdido, abandonado), fecha, duración y eficiencia.
  - Bonus: gráfico de performance/eficiencia a través del tiempo, o porcentaje de ganados vs perdidos.
3. Juego, preparación:
  - Una vez encontrados los dos oponentes, se creara una nueva ejecución.
  - Cada jugador ubicará sus barcos en el tablero (drag & drop).
  - Cuando ambos jugadores estén listos comenzará la batalla.
  - Bonus: botón para disponer los barcos de manera automática.
  - Bonus: tiempo de expiración, superado ese tiempo, los barcos que todavía no se ubicaron serán dispuestos automáticamente.
4. Juego, batalla:
  - Consistirá en un juego de turnos donde, alternadamente, cada jugador disparará un tiro.
  - Los turnos serán dados por el servidor.
  - En cada turno el jugador estará esperando recibir el tiro del oponente, o estará haciendo uso de su posibilidad de tiro.
  - Se deberá mostrar feedback de cada tiro a ambos usuarios y el resultado de los mismos será computado en el servidor.
  - Bonus: botón "Auto-Play" para disparar automáticamente.
  - Bonus: tiempo de expiración, superado ese tiempo, el tiro se dispara automáticamente.
  - Bonus: sonido, animación.
5. Juego, finalización:
  - Si el server detecta un ganador, se notificara a cada jugador su resultado.
  - Botón para volver a la home.
  - Bonus: botón para buscar otro oponente.  
  - Bonus: botón para volver a jugar contra el mismo oponente.

## Entregas:

1. 06/05
  - Propuesta de diseño de pantallas en papel (papper prototiping).
2. 13/05
  - Login con Facebook
  - Home (únicamente con boton de play)  
3. 20/05
  - Prototipo de mensajería para el juego, donde se conecte a dos usuarios por websockets y estos puedan mensajearse entre si
4. 27/05
  - Preparación. Ubicación de flota en el tablero.
5. 03/06
  - Estados del juego.
  - Sincronización de turnos.
  - Prototipo de batalla.
6. 10/06
  - Batalla.
7. 17/06
  - Finalización.
8. 24/06
  - Deployment.
9. 01/07
  - Presentación.

## Requerimientos:

- A la hora de la entrega, el juego deberá estar hosteado y disponible online.
- Podrán usarse todas las librerías y servicios SAS que se crean convenientes
  - Ejemplo: storage en SqlDB, MongoDB o DynamoDB...
- Bonus points: buen código, buen diseño y UX


![Batalla Naval](../10-papoy/paper.jpg)
