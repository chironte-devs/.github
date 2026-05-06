# Manual de uso — Kanban (GitHub Projects) — Chironte

Tablero: https://github.com/orgs/chironte-devs/projects/1

## Objetivo
Tener trazabilidad (auditoría) y seguimiento: qué se pidió, qué se hizo, quién lo hizo, y con qué PR se entregó.

## Conceptos básicos
- **Issue** = unidad de trabajo (bug/feature/tarea). Es lo que se trackea.
- **PR (Pull Request)** = implementación. Debe referenciar una issue.
- **Project** = tablero Kanban que muestra issues.

## Columnas (campo Workflow)
- **Backlog**: ideas/pedidos sin priorizar.
- **Ready**: listo para ejecutar (descripción clara + criterios).
- **In progress**: en ejecución.
- **In review**: PR abierto esperando revisión.
- **Blocked**: bloqueado por dependencia.
- **Done**: terminado (idealmente mergeado + issue cerrada).

## Flujo de trabajo (paso a paso)
1) Crear una **Issue** (Bug/Feature/Task)
2) Completar la info mínima:
   - qué hay que hacer
   - criterios de aceptación
   - evidencia (si es bug)
3) Cuando alguien la toma: asignarse y mover a **In progress**.
4) Abrir un **PR** y en la descripción poner:
   - `Closes #123` (o `Fixes #123`)
   Esto es clave para auditoría: al mergear, GitHub cierra la issue.
5) Pasar a **In review** mientras el PR está abierto.
6) Merge → issue cerrada → mover a **Done** (si no se movió solo).

## Buenas prácticas
- No trabajar “por fuera”: si no hay issue, creala.
- Una issue debe tener un objetivo claro y verificable.
- Si te trabás, comentá el bloqueo y pasá a **Blocked**.

## Ejemplo rápido
- Issue: "Bug: error 500 al guardar cliente"
- PR: "Fix save client null constraint" con `Closes #45`
- Evidencia: log + pasos para reproducir
