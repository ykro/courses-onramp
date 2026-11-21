# Repositorios On-Ramp — Nivelación rápida antes de cada curso

Este índice reúne los tres repositorios de práctica corta (**~60 minutos cada uno**) pensados para cualquier estudiante que diga *"no entiendo"* o *"el curso está muy avanzado"* antes de entrar a **Backend (FastAPI)**, **Frontend (React y Next.js)** o **Android (Kotlin y Jetpack Compose)**.

Cada repositorio tiene **5 pasos independientes**: no hace falta seguirlos en orden. Si ya dominas HTTP o HTML, puedes empezar directo en el **Paso 3** o en el tema que necesites reforzar, verificar solo ese paso con un comando y consultar el repositorio de solución donde queda detallado qué se trabajó y qué se cambió en cada paso.

![Mapa de los tres repositorios On-Ramp](docs/diagrams/overview.svg)

---

## Mapa rápido de repositorios

| Área | Pasos | Repositorio de práctica (empieza aquí) | Solución explicada paso a paso | Repositorio del curso |
| :--- | :---: | :--- | :--- | :--- |
| **Backend (Python y FastAPI)** | 5 independientes | [ykro/backend-onramp](https://github.com/ykro/backend-onramp) | [ykro/backend-onramp-solution](https://github.com/ykro/backend-onramp-solution) | [ykro/backend-course](https://github.com/ykro/backend-course) |
| **Frontend (React y Next.js)** | 5 independientes | [ykro/frontend-onramp](https://github.com/ykro/frontend-onramp) | [ykro/frontend-onramp-solution](https://github.com/ykro/frontend-onramp-solution) | [ykro/frontend-course](https://github.com/ykro/frontend-course) |
| **Android (Kotlin y Compose)** | 5 independientes | [ykro/android-onramp](https://github.com/ykro/android-onramp) | [ykro/android-onramp-solution](https://github.com/ykro/android-onramp-solution) | [ykro/android-course](https://github.com/ykro/android-course) |

---

## Qué practicas en cada uno

### 1. Backend — [ykro/backend-onramp](https://github.com/ykro/backend-onramp)
- **Paso 1:** peticiones y respuestas HTTP (`201`, `204`, `404`) y aislamiento de estado entre peticiones.
- **Paso 2:** validación estricta con Pydantic (`extra="forbid"`, `Decimal` para dinero y `422`).
- **Paso 3:** tu primera base de datos en SQLite puro (`PRAGMA foreign_keys = ON`, PK/FK, `INNER JOIN`, `ORDER BY/LIMIT` con `?` e índice verificado con `EXPLAIN QUERY PLAN`).
- **Paso 4:** `Depends`, `dependency_overrides`, lectura Base64Url de un JWT y separación `401` frente a `403`.
- **Paso 5:** protección contra llamadas simultáneas con `threading.Lock` bajo `Barrier(5)`.
- **Verificación por paso:** `uv run onramp check --paso 1` .. `--paso 5` (o `uv run onramp check` para todos).
- **Solución paso a paso:** [ykro/backend-onramp-solution](https://github.com/ykro/backend-onramp-solution).

### 2. Frontend — [ykro/frontend-onramp](https://github.com/ykro/frontend-onramp)
- **Paso 1:** pasar de `<div>`s a HTML semántico operable con teclado (`<label>`, `aria-invalid`, `aria-describedby` y `getByRole`).
- **Paso 2:** layout con Flexbox, CSS Grid de 2 columnas y foco visible (`:focus-visible`).
- **Paso 3:** por qué mutar un arreglo con `.push()` congela React (`Object.is`) y por qué `key={index}` desordena inputs al filtrar.
- **Paso 4:** convertir texto de `<input>` de forma segura sin mentirle a TypeScript con `as number`.
- **Paso 5:** revisar `response.ok` ante HTTP 404, cancelar búsquedas lentas con `AbortController` y separar `"use client"` de secretos de servidor.
- **Verificación por paso:** `npm run check:paso1` .. `check:paso5` (o `npm run check` para todos).
- **Solución paso a paso:** [ykro/frontend-onramp-solution](https://github.com/ykro/frontend-onramp-solution).

### 3. Android — [ykro/android-onramp](https://github.com/ykro/android-onramp)
- **Paso 1:** verificación de entorno (`JDK 21+` y `ANDROID_HOME`).
- **Paso 2:** lambdas con receptor (`Column { Text(...) }`, `module { single { ... } }`), `sealed interface` y `StateFlow` inmutable.
- **Paso 3:** `suspend` y `delay` con reloj virtual (`runTest` + Turbine), no atrapar `CancellationException` y `remember` al redibujar.
- **Paso 4:** lectura tolerante de JSON contra `MockWebServer` y errores HTTP/parseo.
- **Paso 5:** tu primera tabla SQLite (`CREATE TABLE`, `PRIMARY KEY`, `SELECT/ORDER BY` y `ON CONFLICT DO UPDATE` para no borrar favoritos locales + equivalencia a Room 3).
- **Verificación por paso:** `./gradlew paso1 --no-parallel` .. `paso5` (o `./gradlew ready --no-parallel` para todos, sin emulador).
- **Solución paso a paso:** [ykro/android-onramp-solution](https://github.com/ykro/android-onramp-solution).

---

## Cómo trabajar con IA y con las soluciones

Puedes usar tu asistente de IA favorito (Claude Code, Antigravity, Codex o Gemini CLI) mientras resuelves cualquier paso. Cada repositorio trae un archivo `AGENTS.md` configurado en **modo tutor socrático** para guiarte con preguntas y pistas.

Cuando quieras revisar qué se trabajó exactamente en cada paso o destrabarte en un punto puntual, abre el repositorio `*-solution` correspondiente: su `README.md` tiene la tabla **Dónde ver la solución de cada paso**, enlazando cada criterio directamente al archivo resuelto.
