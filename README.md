# 🤖 BuildBot Lab

**Construye. Programa. Simula. Aprende.**

BuildBot Lab es un proyecto educativo de robótica que permite a los estudiantes construir, programar, simular y compartir robots virtuales. Su propósito es facilitar el aprendizaje de robótica y programación sin exigir que el estudiante disponga inicialmente de un robot físico.

## 📋 Descripción del proyecto

El proyecto propone una aplicación web en la que los estudiantes pueden experimentar con un robot virtual en un entorno 2D. La plataforma busca integrar el diseño del robot, el uso de motores y sensores, la programación de movimientos y la resolución de retos educativos.

Actualmente, el repositorio conserva un prototipo experimental que funciona directamente en el navegador mediante un archivo HTML independiente. Este prototipo sirve para validar la idea educativa antes de desarrollar una arquitectura más modular y mantenible.

## 🎯 Problema o necesidad

El aprendizaje de robótica suele depender de kits físicos, componentes electrónicos, espacio de trabajo y acompañamiento técnico. Estos recursos no siempre están disponibles para todos los estudiantes o instituciones educativas.

BuildBot Lab busca reducir esa barrera mediante un entorno virtual accesible desde un navegador, donde el estudiante pueda:

- Comprender los componentes básicos de un robot.
- Observar cómo los motores producen movimiento.
- Experimentar con sensores virtuales.
- Programar el comportamiento del robot.
- Probar soluciones sin riesgo de dañar equipos físicos.
- Resolver retos de robótica de forma práctica.
- Compartir sus proyectos con otras personas.

## 👥 Público objetivo

El proyecto está dirigido principalmente a:

- Estudiantes de secundaria que comienzan a aprender robótica y programación.
- Docentes que necesitan una herramienta de apoyo para actividades educativas.
- Clubes de robótica y comunidades de aprendizaje.
- Personas interesadas en experimentar con conceptos básicos de sensores, motores y movimiento de robots.

A largo plazo, se contempla un modo avanzado para estudiantes universitarios y sistemas robóticos más complejos. Este modo no forma parte del MVP inicial.

## 💡 Origen de la idea

La idea nació de la necesidad de crear una herramienta educativa que permita aprender robótica aunque no se disponga de hardware físico. El objetivo es que los estudiantes puedan pasar gradualmente de una representación virtual del robot a conceptos aplicables en un robot real.

El proyecto también busca promover la colaboración, permitiendo que otras personas propongan retos, mejoren la documentación, reporten errores y contribuyan al desarrollo de nuevas funciones.

## 🚧 Estado actual

**Estado: prototipo inicial / Pre-MVP.**

El repositorio contiene un prototipo experimental ejecutable en el navegador. Actualmente permite explorar las siguientes funciones:

- Simulación 2D de un robot de tracción diferencial.
- Control independiente de los motores izquierdo y derecho.
- Sensores de distancia simulados.
- Sensores IR o sensores de suelo simulados.
- Detección básica de colisiones con obstáculos.
- Detección de llegada a una meta.
- Retos predefinidos.
- Modo Sandbox para experimentar con escenarios.
- Secuencias básicas de comandos mediante bloques.
- Interfaz experimental con sintaxis similar a Python.
- Telemetría de motores y sensores.
- Controles para ejecutar, pausar y reiniciar la simulación.

> [!WARNING]
> El prototipo es experimental. La precisión de la simulación, las unidades de medida, la cinemática, los modelos de sensores y el sistema de programación todavía deben verificarse de manera independiente.

## 📁 Estructura actual

```text
Builbot-lab/
├── prototype/
│   └── simulador_y_programador_de_robot.html
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## 🚀 Cómo comenzar

### Requisitos

Para explorar el prototipo solamente se necesita:

- Un navegador web moderno, como Microsoft Edge, Google Chrome o Mozilla Firefox.
- Git, si se desea clonar el repositorio.
- Un editor como Visual Studio Code, si se desea revisar o modificar el código.

### Opción 1: Descargar desde GitHub

1. Abre el repositorio: [japonte14/Builbot-lab](https://github.com/japonte14/Builbot-lab).
2. Selecciona **Code**.
3. Selecciona **Download ZIP**.
4. Extrae el archivo descargado.
5. Abre la carpeta `prototype`.
6. Ejecuta `simulador_y_programador_de_robot.html` en el navegador.

### Opción 2: Clonar el repositorio

```bash
git clone https://github.com/japonte14/Builbot-lab.git
cd Builbot-lab
```

Después, abre el archivo ubicado en:

```text
prototype/simulador_y_programador_de_robot.html
```

No se requiere instalar dependencias para ejecutar el prototipo actual.

## 🧭 MVP propuesto

El primer MVP se concentrará en una experiencia educativa pequeña y verificable. El recorrido esperado es que un estudiante pueda:

1. Abrir la aplicación web.
2. Utilizar un robot virtual 2D.
3. Consultar un sensor frontal de distancia.
4. Programar movimientos mediante bloques o una interfaz similar a Python.
5. Ejecutar la simulación.
6. Observar el comportamiento del robot.
7. Completar un reto básico.
8. Guardar o compartir su proyecto en una etapa posterior.

## 🔜 Próximos pasos

- Definir la arquitectura técnica del MVP.
- Separar el prototipo en componentes modulares.
- Verificar la cinemática diferencial y las unidades de movimiento.
- Validar el comportamiento de los sensores virtuales.
- Mejorar la interfaz de programación por bloques.
- Definir el alcance de la programación con Python.
- Crear más retos educativos con niveles de dificultad.
- Agregar instrucciones visuales, capturas de pantalla y ejemplos.
- Incorporar pruebas técnicas y educativas.
- Diseñar opciones para guardar y compartir proyectos.
- Preparar una versión que pueda utilizarse fácilmente en clases.

## 🤝 Cómo contribuir

Las contribuciones son bienvenidas. Puedes colaborar de las siguientes maneras:

- Proponer una función o mejora mediante un **Issue**.
- Reportar errores e indicar cómo reproducirlos.
- Mejorar instrucciones, ejemplos o documentación.
- Crear nuevos retos educativos.
- Proponer mejoras de accesibilidad o experiencia de usuario.
- Corregir o validar los modelos de movimiento y sensores.
- Enviar cambios mediante un **Pull Request**.

Antes de contribuir, consulta el archivo [`CONTRIBUTING.md`](CONTRIBUTING.md).

## 🐛 Issue propuesto para el laboratorio

**Título:** Agregar capturas de pantalla e instrucciones visuales del prototipo

**Descripción:** El repositorio explica las funciones del prototipo, pero todavía necesita imágenes que permitan reconocer la interfaz, los controles del robot, los sensores y el área de simulación antes de ejecutar el archivo HTML.

**Resultado esperado:** Incorporar al README al menos tres capturas de pantalla con descripciones claras: vista general del simulador, controles de programación y ejecución de un reto.

## 🔀 Primera contribución mediante Pull Request

Para practicar el flujo de colaboración se puede crear una rama llamada:

```text
docs/add-prototype-images
```

En esa rama se pueden agregar las capturas de pantalla y actualizar este README. El Pull Request puede usar el siguiente contenido:

**Título:** Mejorar la documentación visual del prototipo

**Descripción:** Este cambio agrega imágenes e instrucciones visuales para facilitar que una persona nueva comprenda la interfaz y pueda ejecutar su primera simulación sin ayuda directa del autor.

Después de revisar los archivos modificados, el Pull Request debe integrarse en la rama `main` mediante **merge**.

## 🤖 Uso de inteligencia artificial

Se utilizó inteligencia artificial como apoyo para organizar la estructura del README, mejorar la redacción y preparar instrucciones de colaboración. El contenido fue revisado para asegurar que describa el estado actual del repositorio y no presente como terminadas funciones que todavía forman parte de la visión futura del proyecto.

## 📣 Presentación breve

### ¿Qué proyecto seleccioné y por qué?

Seleccioné BuildBot Lab porque combina educación, programación y robótica. El proyecto puede ayudar a estudiantes a aprender conceptos fundamentales aunque no tengan acceso inmediato a un kit de robótica físico.

### ¿Qué mejora propuse mediante el Issue?

Propuse agregar capturas de pantalla e instrucciones visuales del prototipo para que una persona nueva pueda comprender la interfaz y comenzar a utilizar el simulador con mayor facilidad.

### ¿Cómo podría crecer con futuras contribuciones?

El proyecto puede crecer mediante nuevos retos educativos, mejoras en la simulación, validación de sensores y cinemática, documentación más clara, pruebas, funciones de accesibilidad y herramientas para guardar o compartir proyectos.

## 📝 Reflexión final

Para que otra persona pueda comprender, utilizar y mejorar BuildBot Lab sin depender de su creador, el proyecto necesita documentación clara, instrucciones de instalación y uso, ejemplos verificables, una estructura de archivos comprensible, una lista transparente de limitaciones, un mecanismo para reportar errores y un proceso sencillo para proponer e integrar cambios.

Una comunidad puede continuar el proyecto cuando entiende no solo lo que ya funciona, sino también lo que falta por validar y cómo puede contribuir de forma segura y organizada.

## 📄 Licencia

Consulta el archivo [`LICENSE`](LICENSE) del repositorio para conocer las condiciones de uso y distribución.
