# Cómo trabajamos en Nessis

## Ramas
- `main`: solo código probado y estable.
- `develop`: rama de integración. Todos los PRs llegan aquí.
- Una rama por issue, nombrada como sugiere el issue, p. ej. `epic3/3-5-flujo-repack`.
  (En cada issue viene el nombre exacto bajo "Rama Git sugerida".)

## Ciclo de cada tarea
1. Toma tu issue del tablero (https://github.com/users/HugoL8/projects/1) y muévelo a "En curso".
2. Crea tu rama desde `develop` (botón "Create a branch" del issue o `git checkout -b <rama> develop`).
3. Trabaja aislado. **La prueba individual va en la misma rama** — el checklist del issue
   (los pasos del diagrama de Miro) es el guion de esa prueba. Sin prueba no se integra.
4. Abre un Pull Request hacia `develop` con `Closes #<número>` en la descripción:
   el issue se cierra solo al integrarse y el tablero se actualiza solo.
5. Otro miembro del equipo revisa el PR antes del merge.
6. Cuando una rama operativa completa del diagrama está en `develop`,
   se corre su prueba end-to-end (Epic 6) y de ahí `develop` → `main`.

## Bloqueos
Si algo te detiene, marca el issue como "Bloqueado" en el tablero y usa la relación
"Blocked by" hacia el issue que te bloquea. Eso alimenta el reporte diario de Hugo.

## Diagramas
El diagrama maestro y los 15 procesos detallados viven en Miro (tablero "Nessis MX Int V1").
Cada issue enlaza el suyo. El diagrama manda: si el código y el diagrama difieren, se
actualiza uno de los dos, nunca se ignora.
