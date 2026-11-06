# 🤖 BuildBot Lab

**Construye. Programa. Simula. Aprende.**

BuildBot Lab es un proyecto educativo de robótica cuyo objetivo es ayudar a estudiantes a comprender cómo se construyen, programan y controlan los robots sin necesidad de disponer inicialmente de un robot físico.

El proyecto está orientado principalmente a estudiantes de secundaria que están comenzando a aprender robótica, programación, sensores, motores y movimiento de robots.

A largo plazo, la visión incluye un modo avanzado para estudiantes universitarios y sistemas robóticos más complejos.

---

## 🚧 Estado del proyecto

**Prototipo inicial / Pre-MVP**

BuildBot Lab cuenta actualmente con un prototipo experimental que funciona en el navegador y está implementado como una aplicación HTML independiente.

El prototipo se utiliza para explorar y validar el concepto educativo antes de migrar el proyecto hacia una arquitectura modular, mantenible y verificable.

### El prototipo actual incluye

- Simulación 2D de un robot de tracción diferencial.
- Control independiente de motores izquierdo y derecho.
- Sensores de distancia simulados.
- Sensores IR/de suelo simulados.
- Detección básica de colisiones con obstáculos.
- Detección de llegada a una meta.
- Retos predefinidos.
- Modo Sandbox para experimentar con escenarios.
- Secuencias básicas de comandos mediante bloques.
- Interfaz experimental con sintaxis similar a Python.
- Telemetría de motores y sensores.
- Controles para ejecutar, pausar y reiniciar la simulación.

> ⚠️ El prototipo actual es experimental. La precisión de la simulación, unidades de medida, comportamiento de sensores, cinemática y sistema de programación todavía deben verificarse independientemente.

---

## 🎯 Objetivo

BuildBot Lab busca crear un entorno donde un estudiante pueda:

1. Comprender los componentes básicos de un robot.
2. Configurar un robot virtual.
3. Comprender cómo los motores producen movimiento.
4. Experimentar con sensores virtuales.
5. Programar el comportamiento del robot.
6. Simular su movimiento.
7. Resolver retos de robótica.
8. Crear sus propios escenarios.
9. Compartir proyectos con otros estudiantes.
10. En el futuro, relacionar el diseño virtual con la construcción de un robot físico.

La intención es hacer más accesible el aprendizaje de robótica cuando no se dispone de hardware físico.

---

## 👥 Usuarios

### Nivel inicial

BuildBot Lab estará orientado principalmente a estudiantes de secundaria.

La experiencia educativa buscará introducir conceptos como:

- Componentes de un robot.
- Motores.
- Sensores.
- Cinemática diferencial.
- Programación.
- Condiciones y toma de decisiones.
- Detección y evasión de obstáculos.
- Resolución de retos.

### Nivel avanzado

En el futuro se contempla un modo avanzado orientado a estudiantes universitarios.

Este podría incluir conceptos más complejos y eventualmente simulación de robots industriales.

> El modo avanzado no forma parte del MVP inicial.

---

## 🧪 Prototipo actual

El prototipo original se conservará como referencia durante el desarrollo.

```text
prototype/
└── simulador_y_programador_de_robot.html
```

Este archivo debe considerarse una implementación experimental y no representa necesariamente la arquitectura definitiva de BuildBot Lab.

La nueva aplicación se desarrollará progresivamente mientras el prototipo original se mantiene disponible para realizar comparaciones.

---

# 🚀 MVP propuesto

El primer MVP se concentrará intencionalmente en una experiencia educativa pequeña y verificable.

Un estudiante debería poder completar aproximadamente el siguiente recorrido:

```text
