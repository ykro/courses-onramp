# On-ramps, nivelación antes de cada curso

Este índice reúne tres on-ramps, nivelaciones prácticas para llegar con lo mínimo a los cursos de **Backend (FastAPI)**, **Frontend (React y Next.js)** y **Android (Kotlin y Jetpack Compose)**. Están pensados para estudiantes que ya programan (estructuras de datos, algoritmos, orientación a objetos) pero sienten que el curso arranca muy arriba, y para quienes nunca han usado una base de datos.

![Mapa de los tres on-ramps](docs/diagrams/overview.svg)

## Por dónde empezar

Cada on-ramp tiene seis pasos. Backend y Frontend toman unas tres horas y media, y Android unas cuatro horas y media sin contar la instalación del SDK. El Paso 0 prepara tu entorno y te pone a correr algo real en minutos; hazlo siempre, aunque ya tengas experiencia. Si es tu primera vez con el tema, sigue los pasos del 0 al 5 en orden. Si ya dominas una parte, elige el paso que necesites, porque cada uno se verifica por separado.

Todos los pasos tienen la misma forma. Empiezan con tres preguntas para pensar antes de tocar código, explican por qué el tema importa en el curso y te piden leer, depurar y escribir algo pequeño. Cierran con preguntas sobre un caso nuevo y te piden explicar en tres líneas lo que cambiaste. Si te trabas, hay tres pistas que van de la idea general a un esqueleto de código, nunca a la respuesta completa. En el Paso 5 escribes tus propios tests, y el verificador los corre también contra versiones con un bug para confirmar que de verdad detectan errores.

| Área | Repositorio de práctica | Solución con respuestas | Curso |
| :--- | :--- | :--- | :--- |
| **Backend (Python y FastAPI)** | [ykro/backend-onramp](https://github.com/ykro/backend-onramp) | [ykro/backend-onramp-solution](https://github.com/ykro/backend-onramp-solution) | [ykro/backend-course](https://github.com/ykro/backend-course) |
| **Frontend (React y Next.js)** | [ykro/frontend-onramp](https://github.com/ykro/frontend-onramp) | [ykro/frontend-onramp-solution](https://github.com/ykro/frontend-onramp-solution) | [ykro/frontend-course](https://github.com/ykro/frontend-course) |
| **Android (Kotlin y Compose)** | [ykro/android-onramp](https://github.com/ykro/android-onramp) | [ykro/android-onramp-solution](https://github.com/ykro/android-onramp-solution) | [ykro/android-course](https://github.com/ykro/android-course) |

## Qué practicas en cada uno

### Backend, [ykro/backend-onramp](https://github.com/ykro/backend-onramp)

| Paso | Tiempo | Tema |
| --- | --- | --- |
| 0 | 35 min | Instalar `uv`, levantar tu primer servidor con FastAPI y hablarle con el navegador, `/docs` y `curl` |
| 1 | 40 min | Códigos HTTP (`201`, `204`, `404`, `422`), estado aislado y validación con Pydantic y `Decimal` |
| 2 | 50 min | Tu primera base de datos, tablas, llaves foráneas, `JOIN`, paginación con parámetros e índices en SQLite |
| 3 | 40 min | `Depends` y `dependency_overrides`, qué trae un JWT y la diferencia entre `401` y `403` |
| 4 | 25 min | Requests simultáneos, race conditions y `threading.Lock` |
| 5 | 30 min | Tests desde cero con `pytest` que se ponen en rojo ante dos versiones con un bug |

Verificación con `uv run onramp check --paso 0` hasta `--paso 5`, o `uv run onramp check` para todos.

### Frontend, [ykro/frontend-onramp](https://github.com/ykro/frontend-onramp)

| Paso | Tiempo | Tema |
| --- | --- | --- |
| 0 | 30 min | Instalar Node, levantar Vite y escribir tu primer componente con props, `useState` y `map` |
| 1 | 45 min | HTML semántico, roles y nombres accesibles, errores conectados al campo, Grid, Flexbox y `:focus-visible` |
| 2 | 30 min | Estado inmutable (`Object.is`) y `key` estable al filtrar listas |
| 3 | 20 min | Convertir el texto de un `<input>` en número con validación y narrowing, sin `as` |
| 4 | 45 min | `response.ok`, cancelar búsquedas con `AbortController` y la frontera entre cliente y servidor |
| 5 | 40 min | Tests desde cero con Vitest que se ponen en rojo ante dos versiones con un bug, y un test de componente con `getByRole` |

Verificación con `npm run check:paso0` hasta `npm run check:paso5`, o `npm run check` para todos.

### Android, [ykro/android-onramp](https://github.com/ykro/android-onramp)

| Paso | Tiempo | Tema |
| --- | --- | --- |
| 0 | 40 min | Revisar JDK y Android SDK con `doctor`, y Kotlin básico (tipos nulos, `data class`, `filter`/`map`, `when`) |
| 1 | 50 min | Lambdas con receptor (la sintaxis de Compose y Koin), `sealed interface` y `StateFlow` inmutable |
| 2 | 60 min | El hilo principal, `suspend` y `delay` con reloj virtual, cancelación con `Job`, estado que sobrevive al redibujo y tu primer `@Composable` con test de UI |
| 3 | 40 min | Requests con OkHttp fuera del hilo principal (`withContext`), JSON tolerante a campos nuevos y errores de red, HTTP o de parseo con `MockWebServer` |
| 4 | 45 min | Tu primera base de datos, tablas, llave primaria, `SELECT` y `ON CONFLICT DO UPDATE` en SQLite, y su equivalente en Room 3 |
| 5 | 30 min | Tests desde cero con JUnit que se ponen en rojo ante dos versiones con un bug |

Verificación con `./gradlew paso0 --no-parallel` hasta `./gradlew paso5 --no-parallel`, o `./gradlew ready --no-parallel` para todos. No necesita emulador.

Los tres repositorios incluyen un glosario, un ejemplo de cómo leer un ADR y una guía de Integración Continua (CI). Frontend y Android traen además una guía corta de Firebase.

## Cómo usar la IA y las soluciones

Puedes usar tu asistente de IA (Claude Code, Antigravity, Codex o Gemini CLI) mientras resuelves cualquier paso. Cada repositorio trae un `AGENTS.md` que le pide guiarte con preguntas y pistas antes de mostrarte código. Si aceptas código que no puedes explicar con tus palabras, el on-ramp pierde su sentido.

Cada repositorio `*-solution` tiene una tabla que explica qué se cambió en cada paso y por qué, y cada guía de paso termina con las respuestas de autoevaluación. Ábrelo después de intentar, no antes.
