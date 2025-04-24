# Configuración estación 90
Configuración de la estación seteada en el puerto `10.20.30.90`
## [Modulos necesarios](./configuracion_hardware_PLC_siemens.xlsx)
## Variables
### De entrada
#### Botonera selector
##### Selector
I0.2 - I0.3
##### Paro NC (boton rojo)
I0.1 
##### Marcha (boton verde)
I0.0
#### Stop Emergencia NC
_NC con enclavamiento_

I0.4
#### Botonera dos verdes
##### Boton Rojo NC
I0.5
##### Botones verde
I0.6 - I0.7


### De salida
#### Luz verde
Q0.0
#### Luz naranja
Q0.1
#### Luz roja
Q0.2
#### Cilindro inferior
Q3.0
##### Reed inicio carrera
I3.0
##### Reed final carrera
I3.1
#### Cilindro superior
Q3.1
##### Reed inicio carrera
I3.2
##### Reed final carrera
I3.3
#### Cilindro carro peq
Q3.2
##### Reed inicio carrera
I3.4
##### Reed final carrera
I3.5