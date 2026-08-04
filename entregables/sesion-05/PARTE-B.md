# Parte B - Auditoría de documentación del proyecto

## Matriz de Auditoría por Tipo de Documentación

| Tipo de Documentación | Estado | Observación | Ubicación |
| :---: | :---: | --- | :---: |
| README de proyecto| Completo | Explica correctamente como levantar el proyecto pero tuve que consultar cómo solucionar el error que dió al ejecutar los comandos del backend. Al proyecto full-stack-adonisjs-s5-base-202607-seniors le falta una carpeta tmp, por lo que falta informar en el README o agregar la carpeta en el repositorio| README.md (Raíz) |
| Descripción de la arquitectura general | Inexistente | En el README.md de la carpeta docs se menciona que los ADRs y Diagramas de arquitectura se van añadir en sesiones posteriores, no encontré diagramas | - |
| Documentación de la API o de los endpoints | Inexistente | No se usa swagger (no se encuentra el archivo `/config/swagger.ts` en la ubicación) ni scalar. | - |
| Docstrings y comentarios significativos en código (TSDoc/JSDoc) | Parcial | Se utiliza VineJS por lo relevado (desconozco que tan correcto es el uso en el proyecto). Los archivos .ts de los controllers se encuentran documentados pero no estan completos, les faltan @param, @return, @throws del estándar TSDoc o JSDoc | `/backend/app/controllers`, `backend/app/validators` (VineJS)|
| Decisiones técnicas registradas | Inexistente | No se encuentran ADR / MADR que justifiquen el uso de los componentes del Stack Tecnológico | - |
| Guía operacional | Parcial | En el readme se menciona el uso de flujo spec-driven con Claude Code o Cursor, no encontre archivos que comenten cómo realizar el despliegue o workflows CI/CD| README.md |
| Convenciones de código del proyecto | Parcial | Se mencionan las convenciones del proyecto en el config.yaml, también se encuentran convenciones el archivo CLAUDE.md (Archivo AGENTS) | `openspec/config.yaml` y CLAUDE.md (Raíz)|
| Especificación OpenSpec y su trazabilidad con el código | Completo | Se encuentra el flujo de OpenSpec en cada agente | openspec (Raíz), `.cursor/commands`, `.claude/skills`, `.claude/commands`, `.cursor/skills`|
| Testing de documentación en CI y docs para LLSm | Inexistente | No he encontrado archivos de cobertura de TSDoc, workflows | - |




## Top 3 carencias que más duelen:
1. ADRs, no quedan evidenciadas las decisiones técnicas. Por ejemplo, la elección de usar una BD SQLite. Se pierde el contexto histórico
2. Documentación de código TypeScript (TSDoc/TypeDoc). Ayuda tanto al equipo, como para que los copilotos no alucinen y para generar la documentación de la API
3. Agregar el uso de Context7 a CLAUDE.md para que implemente los cambios con la documentación actualizada



## Top 3 cosas que ya están bien:
1. README.md - Explica correctamente como levantar el proyecto, da un onboarding rápido de qué es lo que tiene el proyecto y
2. OpenSpec - El flujo para aplicar un change se aplica sin problemas (al menos el de Claude, que fue el que pude probar)
3. CLAUDE.md - Cumple con informar la arquitectura, non-goals, convenciones dando un contexto claro
