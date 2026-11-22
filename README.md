# On-ramps, nivelación antes de cada curso

Este índice reúne tres on-ramps, nivelaciones prácticas para llegar con lo mínimo a los cursos de **Backend (FastAPI)**, **Frontend (React y Next.js)** y **Android (Kotlin y Jetpack Compose)**. Están pensados para estudiantes que ya programan (estructuras de datos, algoritmos, orientación a objetos) pero sienten que el curso arranca muy arriba, y para quienes nunca han usado una base de datos.

![Mapa de los tres on-ramps](docs/diagrams/overview.svg)

## Por dónde empezar

Haz siempre el Paso 0: prepara tu entorno y te pone a correr algo real. Después, si vas atrasado, haz solo lo que pide la Unidad 1 y deja el resto para antes de la Unidad 2.

| Curso | Para la Unidad 1 | Recorrido completo | Cómo verificar |
| --- | --- | --- | --- |
| Backend | Pasos 0, 1, 3 (solo el `TODO 1`) y 5, unas dos horas | 6 pasos, unas cuatro horas | `uv run onramp check --paso N` |
| Frontend | Pasos 0, 1 (`CA-1.1` y `CA-1.2`), 2, 3 y 5, menos de tres horas | 6 pasos, unas tres horas y media | `npm run check:pasoN` |
| Android | Pasos 0, 1 (sin el ejercicio 2), 2, 3 y 6, unas tres horas y media | 7 pasos, unas cinco horas | `./gradlew pasoN --no-parallel` |

Cada paso empieza con tres preguntas, explica por qué importa en el curso y te pide leer, depurar y escribir algo pequeño. Si te trabas, tres pistas van de la idea general a un esqueleto, nunca a la respuesta. En el último paso escribes tus propios tests, y el verificador los corre contra dos versiones con un bug para confirmar que detectan errores. La tabla de pasos y temas está en el README de cada repositorio.

| Área | Repositorio de práctica | Solución con respuestas | Curso |
| :--- | :--- | :--- | :--- |
| **Backend (Python y FastAPI)** | [ykro/backend-onramp](https://github.com/ykro/backend-onramp) | [ykro/backend-onramp-solution](https://github.com/ykro/backend-onramp-solution) | [ykro/backend-course](https://github.com/ykro/backend-course) |
| **Frontend (React y Next.js)** | [ykro/frontend-onramp](https://github.com/ykro/frontend-onramp) | [ykro/frontend-onramp-solution](https://github.com/ykro/frontend-onramp-solution) | [ykro/frontend-course](https://github.com/ykro/frontend-course) |
| **Android (Kotlin y Compose)** | [ykro/android-onramp](https://github.com/ykro/android-onramp) | [ykro/android-onramp-solution](https://github.com/ykro/android-onramp-solution) | [ykro/android-course](https://github.com/ykro/android-course) |

Los tres repositorios incluyen un glosario, un ejemplo de cómo leer un ADR y una guía de Integración Continua (CI). Frontend y Android traen además una guía corta de Firebase.

## Cómo usar la IA y las soluciones

Puedes usar tu asistente de IA (Claude Code, Antigravity, Codex o Gemini CLI) mientras resuelves cualquier paso. Cada repositorio trae un `AGENTS.md` que le pide guiarte con preguntas y pistas antes de mostrarte código. Si aceptas código que no puedes explicar con tus palabras, el on-ramp pierde su sentido.

Cada repositorio `*-solution` tiene una tabla que explica qué se cambió en cada paso y por qué, y cada guía de paso termina con las respuestas de autoevaluación. Ábrelo después de intentar, no antes.
