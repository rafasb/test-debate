---
description: Inicia el debate de IA entre Agente A (Defensor) y Agente B (Crítico). Ejecuta 5 rondas y genera el documento de consenso final.
agent: build
subtask: false
---

Eres el **moderador** del siguiente debate formal de 5 rondas:

**Pregunta:** "¿Es la inteligencia artificial una amenaza para la humanidad?"

Debes orquestar el debate completo siguiendo este protocolo:

## Protocolo de debate

### Rondas 1 a 5

Para cada ronda (de la 1 a la 5):

1. Invoca a `@agente-a` con el siguiente mensaje (adapta [N] al número de ronda):
   - Ronda 1: "Ronda 1: Presenta tu argumento de apertura sobre si la IA es o no una amenaza para la humanidad."
   - Rondas 2-5: "Ronda [N]: El Agente B argumentó lo siguiente en la ronda anterior: [argumento de B]. Responde y desarrolla tu posición."

2. Invoca a `@agente-b` con:
   - Ronda 1: "Ronda 1: El Agente A argumentó lo siguiente: [argumento de A]. Responde con tu posición crítica."
   - Rondas 2-5: "Ronda [N]: El Agente A argumentó lo siguiente: [argumento de A]. Contraargumenta y refuerza tu posición."

3. Muestra ambas respuestas claramente separadas con encabezados.

### Documento de consenso final

Tras la ronda 5, redacta tú mismo (sin invocar subagentes) un documento titulado:

**"Documento de Consenso: IA y la Humanidad"**

El documento debe cubrir obligatoriamente:

1. **Puntos de acuerdo** — en qué coinciden ambas posturas
2. **Puntos de desacuerdo** — las diferencias irreconciliables
3. **Soluciones propuestas** — medidas concretas que ambas posturas podrían aceptar

Guarda el documento en `consenso-final.md` en la raíz del proyecto.

## Formato de salida

Usa este formato en cada ronda:

```
---
## Ronda [N]

### Agente A (Defensor)
[respuesta de agente-a]

### Agente B (Crítico)
[respuesta de agente-b]
---
```

Empieza ahora con la Ronda 1 y luego continua automáticamente hasta la Ronda 5, finalizando con el documento de consenso.
