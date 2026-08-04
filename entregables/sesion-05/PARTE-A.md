# Parte A - Revisión de tu backlog de historias de usuario


## Paso 1
Se realiza la revisión del entregable S4, se chequea el prompt redactado a partir del PRD de FlowSync


## Paso 2
Teniendo en cuenta el prompt que he redactado del ejercicio previo de la S4, detallo mis respuestas a continuación:

- ¿Siguen teniendo sentido las historias tal como las generaste? ¿El alcance sigue ceñido al MVP del PRD, o se coló alguna que la IA "inventó" fuera de scope?.  
    Sí, las historias siguen teniendo sentido funcional pero están orientadas al producto final. El alcance sigue ceñido al MVP. La IA no inventó ninguna funcionalidad y mantuvo las restricciones e indicaciones del prompt. Como oportunidad de mejora, creo que al prompt le faltó mayor especificación en el formato de salida y solicitar un desglose más técnico, ya que en el PRD se mencionaba que la audiencia incluía a los equipos de ingeniería (Backend y Frontend).


- ¿Hay historias cuyos **criterios de aceptación** ahora ves incompletos o poco verificables?  
    Si, al revisarlas noto que las historias son poco verificables e incompletas.
    Entiendo que una de las causas es la falta de detalle técnico y especificaciones en el prompt inicial. Sumado a esto, por lo visto en el ejercicio donde hemos aplicado el patrón "AI as poke-holes", deja en claro que las historias quedaron incompletas por falta de edge cases, escenarios, manejo de errores.
   
   
- ¿Hay historias que han **cambiado de naturaleza** desde entonces? (porque descubriste una dependencia, porque la spec evolucionó, porque entiendes mejor el dominio).  
    Si,  hay historias que han cambiado su naturaleza:
    - La US de la Sincronización con Google Calendar(Lo vimos en la  S5) pasó de ser una User Story a Spike Técnico. Faltaba especificación técnica o requería investigar.
    - La US de Login y Registro pasó a ser una US aislada a tener dependencias requiriendo ser priorizada en el backlog


- ¿Hay historias **nuevas** que no aparecieron cuando lo generaste y que ahora sí deberían estar?  
    Creo que un Spike sobre la autenticación y manejo de token hubiera sido interesante tener. Agregaría historias más técnicas, igual me genera dudas si es algo que puede esperar a realizar el _opsx:propose_
   
- Al contrastar con el backlog que el mentor construyó en el directo de S4 sobre Linear: ¿qué priorizaste distinto tú? ¿Quién acertó y por qué?
    Mis US tenían un orden pero no se mencionan dependencias. A simple vista se podían tomar cualquiera de ellas, trabajarlas, y no era así. Cuando el mentor le pidió a Claude que verifique cuales US tenían dependencias ahí me dí cuenta que no lo había mencionado en el prompt.




## Paso 3
Estos son los ajustes que haría a mi backlog:

- Ajuste 1: Spikes
```text
Ajuste: Convertir las historias de mayor incertidumbre a Spikes.
Motivo: Para evitar tener historias muy grandes, prevenir bloqueos al priorizar el backlog y visualizar qué US pueden trabajarse en simultáneo. Además, para poder reducir la ambigüedad en la solución.
```

- Ajuste 2: Criterios de aceptación
```text
Ajuste: Mejorar los CA, aplicando el patrón "AI as poke-holes" e identificar edge cases
Motivo: Los criterios de aceptación generados desde el prompt inicial no fueron suficientes. Los verificaría para evitar la _false completeness_ de la IA, lograr una mejor estimación y garantizar que sean testeables. Esto lo noté al utilizar este patrón en el ejercicio de la S4.
```

- Ajuste 3: Descomposición técnica
```text
Ajuste: Descomponer las historias por responsabilidades/roles técnicos
Motivo: Para evitar que lleguen historias complejas al desarrollador, que generan PRs gigantes, y para proporcionar un contexto acotado a los copilotos.  Al haber desarrolladores dedicados solo a Frontend o solo a Backend (o la participación de equipos como Arquitectura o DevOps), cada parte tendría su contexto y la información más específica para realizar su tarea.
```

- Ajuste 4: DoD y Non-Goals
```text
Ajuste: Agregar DoD y Non-Goals
Motivo: Para evitar que la tarea se extienda y no fuese ese el alcance, y para cumplir con los estándares de calidad. En el PRD se mencionaban riesgos conocidos (por ejemplo: rate limits, zonas horarias), al tener definidos los Non-Goals en las US podríamos evitar que los devs o los agentes agreguen funcionalidades no alcanzadas y al agregar el DoD nos permite asegurar que el entregable cumpla con todos los criterios de calidad.
```







