@AGENTS.md

# PuntoMedio

Calculadora de punto de encuentro ideal entre varias personas (mapa interactivo). El proyecto más chico y simple del portfolio.

## Claude's Role

Mantenimiento liviano: es un proyecto estable de un solo archivo, sin backend. Ayudar si aparece un bug puntual o una mejora chica (ej. nueva categoría de lugar cercano).

If a session is drifting hacia algo grande para este proyecto, nudge me back: "¿Esto todavía entra en 'proyecto chico de un archivo', o ya amerita separar en backend/frontend?"

## Process

1. Bug o mejora chica detectada al usar la app
2. Se edita directo `punto-medio.html` (vanilla JS, sin build step)
3. Se prueba local con `npx serve .`

## Key People

Solo yo (Matías).

## Folder Structure

- `punto-medio.html` — toda la app (HTML + CSS + JS vanilla)
- `00 System/` — scripts/config reusables de este proyecto (vacío por ahora)
- `01 Skills/` — skills en markdown de este proyecto (vacío por ahora)
- `02 Attachments/` — imágenes/screenshots (vacío por ahora)
- `03 Iteration Logs/` — notas de qué mejorar entre iteraciones (vacío por ahora)

## Rules & Conventions

- **`(C)` prefix** — Archivos creados por Claude llevan prefijo `(C)`
- **Editing rule** — Antes de editar un archivo sin el prefijo `(C)`, pedir permiso primero
- **Skills** — Automatizaciones reusables de este proyecto van en `01 Skills/` como markdown, no como Claude Code skills
- Requiere una API key propia de Google Maps (Maps JavaScript API + Places API (New) + Geocoding API) — facturable si se supera la cuota gratuita
- No sirve bien desde `file://`, necesita servidor local

## Current Status

> **Last updated:** 2026-07-13
> **Status:** Estable, sin cambios recientes. Último commit real: 2026-06-24.

Sin tests, sin CI — no aplica dado el tamaño del proyecto.
