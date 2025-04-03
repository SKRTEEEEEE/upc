# Robótica

## Definición de puntos en espació
Dos tipos:
1. World - base robot -> **usaremos este**
2. Tool (TCP) - base herramienta
### Ruta
La `z` nos indica la precision de paso por el punto, si queremos la maxima precisión utilizaremos `fine`, sino la z nos indica los mm de precision por el que pasara el punto.
#### Uso de `robtarget`
Mas información sobre el uso de `orient rot` y `confdata robconf` en [la pagina 12-14 del PDF extra de S33 + Introducció Rapid](../../Documents/Teoria/Tools/S33%20+%20INTRODUCCIO%20RAPID.pdf). Basados en [caterniones](https://es.wikipedia.org/wiki/Cuaterni%C3%B3n#:~:text=%2C%20los%20cuaterniones%20son%20una%20extensi%C3%B3n,espacio%20vectorial%20de%20dimensi%C3%B3n%204.)

## RobotStudio
### Simulación
Para para ver la simulación, diseñar puntos y rutas con la interfaz del programa
### Rapid
Zona para programar los programas con rapid
### Sincronización
Podemos sincronizar de Rapid a Simulación y de Simulacón a Rapid.
#### Primera vez desde Simulación
Si hemos creado los puntos y la ruta desde Simulación, haremos 