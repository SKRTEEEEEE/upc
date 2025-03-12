# Flancos en PLC

## Definición
Los flancos son utilizados para detectar cambios de estado en una señal digital. Generan un pulso que dura **un solo scan del PLC** y permiten reaccionar ante transiciones específicas de la señal.

### Tipos de flancos
1. **Flanco de subida (Rising Edge, R_TRIG)**
   - Se activa cuando la señal cambia de `0` a `1`.
   - Solo dura **un scan**.
   - Detecta el instante exacto en que la señal pasa de bajo a alto.

2. **Flanco de bajada (Falling Edge, F_TRIG)**
   - Se activa cuando la señal cambia de `1` a `0`.
   - Solo dura **un scan**.
   - Detecta el instante exacto en que la señal pasa de alto a bajo.

---

## Ejemplo básico
### Suposición
**El input cambia de estado cada 5 scans.**
### Introducción

- En los scans donde ocurre un cambio de `0` a `1`, se activará el **flanco de subida**.
- En los scans donde ocurre un cambio de `1` a `0`, se activará el **flanco de bajada**.

### Tabla de ejemplo:

| Scan | Input | Flanco de subida | Flanco de bajada |
|------|-------|-----------------|-----------------|
| 5    | 0     | 0               | 0               |
| 6    | 1     | 1               | 0               | ← **Se activa el flanco de subida**
| 7    | 1     | 0               | 0               |
| 10   | 1     | 0               | 0               |
| 11   | 0     | 0               | 1               | ← **Se activa el flanco de bajada**
| 12   | 0     | 0               | 0               |
| 15   | 0     | 0               | 0               |
| 16   | 1     | 1               | 0               | ← **Nuevo flanco de subida**

### Claves a recordar
✅ El flanco **solo se activa en el scan donde hay un cambio de estado**.  
✅ Si el input cambia **cada 5 scans**, los cambios ocurren en `6, 11, 16, 21...`.  
✅ Un flanco de subida solo se activará en los scans `6, 16, 26...`, mientras que un flanco de bajada se activará en `11, 21, 31...`.  
✅ **El flanco dura un solo scan y luego vuelve a 0**.  

---

## Aplicación en contacto normalmente abierto (NO)
Si tenemos un **contacto normalmente abierto (NO) con un flanco de subida**, el comportamiento será:

1. **En el scan 6**, el input pasa de `0` a `1` → Se activa el flanco de subida.
2. **En el scan 7**, el flanco vuelve a `0`.
3. **En el scan 16**, el input vuelve a cambiar de `0` a `1` → Se activa el flanco nuevamente.

Lo mismo sucede con el flanco de bajada, pero en dirección opuesta.

---

**Conclusión**  
📌 Los flancos permiten detectar eventos específicos de cambio en una señal.  
📌 Son útiles para contar eventos, sincronizar procesos o detectar entradas momentáneas.  
📌 Su duración es de un solo scan, por lo que deben usarse adecuadamente en la lógica del programa.

