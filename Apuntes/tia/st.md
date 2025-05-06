# Texto estructurado (ST/SCL)

## InOut vs Out (FC)

### Razones para usar VAR_IN_OUT en lugar de VAR_OUT:

1. **Referencia directa**: 
   - Con VAR_IN_OUT, trabajas directamente con la referencia a la variable original.
   - Con VAR_OUT, se crea una variable temporal interna que luego se copia al final de la ejecución.

2. **Eficiencia de memoria**:
   - VAR_IN_OUT no requiere espacio adicional de memoria para variables temporales.
   - VAR_OUT crea variables temporales que consumen memoria adicional.

3. **Actualización inmediata**:
   - Con VAR_IN_OUT, cualquier cambio se refleja inmediatamente en la variable original durante la ejecución.
   - Con VAR_OUT, los cambios solo se reflejan al finalizar la ejecución completa de la función.

4. **Comportamiento con estructuras complejas**:
   - Para tipos de datos simples como BOOL, la diferencia puede ser mínima.
   - Para estructuras de datos más complejas, VAR_IN_OUT es más eficiente porque evita la copia completa de la estructura.

### Ejemplo comparativo:

Con VAR_IN_OUT (recomendado):
```scl
FUNCTION Reset_Variables : VOID
VAR_IN_OUT
    Var1 : BOOL;
    Var2 : BOOL;
END_VAR

BEGIN
    Var1 := FALSE;
    Var2 := FALSE;
END_FUNCTION
```

Con VAR_OUT (menos eficiente):
```scl
FUNCTION Reset_Variables : VOID
VAR_OUT
    Var1 : BOOL;
    Var2 : BOOL;
END_VAR

BEGIN
    Var1 := FALSE;
    Var2 := FALSE;
END_FUNCTION
```

En el segundo caso, si el programa principal ya ha cambiado el valor de las variables originales después de llamar a la función pero antes de que termine su ejecución, estos cambios podrían perderse cuando la función termine y sobrescriba las variables con sus valores de salida.
