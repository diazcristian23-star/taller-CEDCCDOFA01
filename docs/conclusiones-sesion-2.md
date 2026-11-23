# Tarea sesión 2 — CI de calidad

## Parte 0. Preparación

Se preparó el entorno de trabajo con Git y Docker y se ejecutaron las pruebas iniciales.

### Resultados de Catalog
- Pruebas: 28 aprobadas y 0 fallidas.
- Cobertura de líneas del servicio: 66,14 %.
- Cobertura de líneas de shifts.ts: 80 %.
- Línea sin cubrir en shifts.ts: 15.
- Mutación: 5 mutantes, 1 muerto y 4 sobrevivientes.
- Puntaje de mutación: 20 %.

### Observación inicial
Aunque todas las pruebas de Catalog pasan, cuatro de cinco cambios artificiales no fueron detectados. Por lo tanto, las pruebas actuales no garantizan que todas las reglas del sistema estén correctamente verificadas.

### Otros servicios
- Notifications: pruebas ejecutadas correctamente.
- Incidents: pruebas ejecutadas correctamente (100 %, sin errores).

## Parte 1. Un bug, de rojo a verde

## Parte 2. Cobertura y mutación

## Parte 3. Análisis estático

## Parte 4. Dependencias y secretos

## Parte 5. Gate de calidad

## Parte 6. Contenedores

## Registro de uso de IA

## Conclusiones finales

### Resultados Parte 1: De rojo a verde

Se incorporó una prueba para verificar que un turno siga activo durante su último día.

- Antes de la corrección: 28 pruebas aprobadas y 1 fallida.
- Error detectado: el último día del turno se consideraba inactivo.
- Después de la corrección: 29 pruebas aprobadas y 0 fallidas.
- Evidencia: ejecución de npm test en services/catalog.
- Commits: 9040e32 (prueba) y ac388a1 (corrección).

El ejercicio demuestra que una prueba automatizada puede detectar un error y comprobar posteriormente su corrección.

### Resultados Parte 2: Cobertura y mutación

Se incorporó una prueba para verificar que, cuando existen varios turnos vigentes, se seleccione el de menor identificador.

- Pruebas: 30 aprobadas y 0 fallidas.
- Cobertura general de líneas: 66,14 % inicial y 66,66 % final.
- Cobertura de shifts.ts: 80 % inicial y 100 % final.
- Mutación inicial: 5 mutantes, 1 muerto y 4 sobrevivientes (20 %).
- Mutación final: 4 mutantes, 1 muerto y 3 sobrevivientes (25 %).

La cobertura aumentó, pero todavía existen mutantes sobrevivientes. El aumento del puntaje de mutación también está influido por la reducción del número de mutantes generados.

Conclusión: una cobertura elevada no garantiza que las pruebas detecten todos los errores.
