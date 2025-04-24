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
