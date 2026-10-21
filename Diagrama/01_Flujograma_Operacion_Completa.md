
# Flujograma 1: Operación completa

**Proyecto:** Calculadora Java, Python y SQLite  

Este flujograma representa el proceso de ejecución de operaciones matemáticas, validación de datos, manejo de errores y almacenamiento de los resultados en la base de datos.

```mermaid

flowchart TD
    A([Inicio]) --> B[/Solicitar operacion y operandos/]
    B --> C{¿La operacion existe?}
    C -->|No| D[/Mostrar operacion inexistente/]
    D --> Z([Fin])
    C -->|Si| E{¿Operandos validos?}
    E -->|No| F[/Mostrar entradas invalidas/]
    F --> Z
    E -->|Si| G[Continuar con el calculo]
    G --> H{¿Ocurrio un error matematico?}
    H -->|Si| I[[Guardar calculo fallido en BD]]
    H -->|No| J[[Guardar calculo exitoso en BD]]
    I --> Z
    J --> Z

```
