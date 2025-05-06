# Electrotecnia

## Protectores


| **Dispositivo**        | **Protege contra**                  | **Protección contra sobrecarga** | **Protección contra cortocircuito** | **Rearme**  | **Características adicionales**                 |
|------------------------|-------------------------------------|----------------------------------|-------------------------------------|-------------|--------------------------------------------------|
| **Relé térmico**        | Sobrecargas (por calor)             | Sí                               | No                                  | No          | Protege principalmente a motores eléctricos.     |
| **Magnetotérmico**      | Sobrecargas y cortocircuitos        | Sí                               | Sí                                  | Sí          | Combina protección térmica y magnética.           |
| **Diferencial**         | Fallos a tierra (fugas de corriente) | No                               | No                                  | Sí          | Detecta diferencias de corriente entre fase y neutro. |
| **Disyuntor**           | Sobrecargas y cortocircuitos        | Sí                               | Sí                                  | Sí          | Se puede resetear tras un disparo.               |
| **Fusible**             | Sobrecargas y cortocircuitos        | Sí                               | Sí                                  | No          | Se quema al sobrepasar un límite de corriente.    |

### Resumen:
- **Relé térmico**: Protege contra sobrecargas por temperatura, pero no contra cortocircuitos.
- **Magnetotérmico**: Protege tanto contra sobrecargas como cortocircuitos y es rearmable.
- **Diferencial**: No protege contra sobrecargas ni cortocircuitos, solo contra fugas de corriente a tierra.
- **Disyuntor**: Protege contra sobrecargas y cortocircuitos, y es rearmable.
- **Fusible**: Protege contra sobrecargas y cortocircuitos, pero no es rearmable y debe ser reemplazado.

## Detectores
- A diferencia de los sensores, que te dan una magnitud, los detectores detectan algo.

### Presión
#### Sin transmición
##### Manómetro 
Mira la diferencia entre dos presiones, puede ser absoluta (sobre atmosfera) o diferencial (sobre una presion conocida)
##### Bourdom 
Tubo curvado que ejerce una medida directa de la presión
#### Transmisores de presión 
Contienen un elementro primario (mide) y secundario (envia la señal/transforma)
##### Piezorresictivos
Elementos piezorresistivos dentro de un único chip de silicio, actuando este como un diafragma que se deforma por la presión introducida.

    • 🧠 Un piezorresistivo es un cristal que al comprimirse produce una carga proporcional a la presión.

##### Capacitivos
Generan una capacidad lineal por la presion ejercida, son diferenciales.
### Caudal
#### Presión
Los siguientes tipos utilizan el principio de Bernouilli, para calcular la presión.
##### Desplazamiento volumen
_Miden la cantidad de desplazamiento con unas ruedas_
##### Presión diferencial
Por obstruccion y una union en cada punto, podemos obtener la diferencia.
##### Pilot
Es un palo con dos agujeros, en uno cerrado metemos la presion estatica y en el otro introduccimos la presion dinamica para obtener la velocidad en ese punto.
#### Electromagneticos
Los siguientes tipos utilizan la fuerza magnetica para obtener la medida de una forma electrica.
##### Sensor de caudal electromagneticos
Para fluidos conductores, Utilizan la diferencia de campos, del propio fluido vs el de un electroiman.
##### Vortex
A partir del Número de Strouhal podemos obtener el caudal al obtener la velocidad media.
#### Massa
Los siguientes tipos utilizan la fuerza de Coriolis para obtener la magnitud.
##### Coriolis
### Nivel
#### Presión hidrostática
A partir de la presión podemos deducir la altura si conocemos el fluido
#### Ultrasonidos
A partir de ondas se refleja el 