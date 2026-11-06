# 🤝 Contribuir a BuildBot Lab

Gracias por tu interés en contribuir a BuildBot Lab.

BuildBot Lab es un proyecto educativo de robótica en una etapa temprana de desarrollo.

Actualmente existe un prototipo experimental y estamos trabajando progresivamente para convertirlo en una arquitectura modular, comprobable y mantenible.

Las contribuciones deben priorizar:

- simplicidad;
- valor educativo;
- claridad;
- mantenibilidad;
- resultados verificables.

---

# Antes de contribuir

Antes de comenzar:

1. Lee `README.md`.
2. Revisa los Issues existentes.
3. Selecciona un Issue antes de implementar una funcionalidad importante.
4. Si existen dudas, discútelas primero en el Issue.
5. Mantén los cambios limitados al alcance del Issue.

Evita combinar en una misma Pull Request:

- refactorización;
- nuevas funcionalidades;
- cambios importantes de interfaz;
- nuevas dependencias;
- cambios de arquitectura.

---

# Principios de desarrollo

## 1. Conservar el comportamiento existente

El prototipo HTML original se conservará como referencia durante el proceso de modularización.

Al separar una parte del prototipo:

```text
Extraer
   ↓
Verificar
   ↓
Crear pruebas
   ↓
Mejorar
```

Primero debemos conservar el comportamiento existente.

Después podremos mejorarlo.

---

## 2. Mantener pequeño el MVP

El objetivo inicial es demostrar el siguiente recorrido:

```text
Configurar
    ↓
Programar
    ↓
Simular
    ↓
Observar
    ↓
Resolver un reto
```

Una funcionalidad que no contribuya directamente a este flujo probablemente pueda esperar a una fase posterior.

---

## 3. Separar responsabilidades

La arquitectura objetivo diferencia claramente:

```text
Interfaz
│
├── Programación
├── Renderizado
└── Telemetría

Motor de simulación
│
├── Cinemática
├── Sensores
├── Colisiones
├── Metas
└── Retos
```

Los módulos del simulador deben, siempre que sea posible:

1. recibir datos;
2. calcular;
3. devolver resultados.

No deberían modificar directamente elementos HTML.

De la misma manera, el renderizado debe mostrar el estado del simulador sin alterar su comportamiento físico.

---

# Flujo de trabajo

## 1. Selecciona un Issue

Cada cambio significativo debe estar relacionado con un Issue.

## 2. Crea una rama

Ejemplos:

```text
feature/distance-sensor
feature/scenario-editor

refactor/kinematics
refactor/canvas-renderer

fix/robot-collision

test/kinematics

docs/update-readme
```

## 3. Implementa un cambio específico

Evita modificaciones no relacionadas.

## 4. Verifica

Cuando sea aplicable, agrega pruebas automatizadas.

## 5. Abre una Pull Request

La Pull Request debe hacer referencia al Issue correspondiente.

---

# Commits

Utiliza mensajes pequeños y descriptivos.

Ejemplos:

```text
chore: preserve standalone prototype
```

```text
refactor: extract level configuration
```

```text
refactor: extract differential drive kinematics
```

```text
test: add straight movement kinematics test
```

```text
fix: prevent zero wheel separation
```

```text
docs: document simulation coordinate system
```

Aunque la documentación del proyecto esté en español, recomendamos mantener los nombres técnicos de ramas y commits en inglés para mantener consistencia con las convenciones habituales de proyectos open source.

---

# Pull Requests

Una Pull Request debe explicar:

## ¿Qué cambió?

Describe concretamente la implementación.

## ¿Por qué?

Indica el Issue o requisito que resuelve.

## ¿Cómo se verificó?

Utiliza solamente los elementos que realmente hayas ejecutado:

```text
Verificación:

- [ ] Se agregaron o actualizaron pruebas unitarias.
- [ ] Las pruebas existentes se ejecutaron correctamente.
- [ ] Se realizó una prueba manual.
- [ ] Se actualizó la documentación.
```

No marques una prueba como completada si realmente no fue ejecutada.

## Limitaciones conocidas

Indica claramente cualquier elemento que:

- todavía no funcione;
- no haya sido probado;
- necesite investigación adicional.

---

# Pruebas

La intención es utilizar pruebas automatizadas para los componentes matemáticos y de comportamiento.

## Pruebas unitarias

Se propone utilizar Vitest para componentes como:

- cinemática diferencial;
- sensores;
- colisiones;
- detección de meta;
- validación de proyectos.

Por ejemplo:

```text
Motor izquierdo = 50 %
Motor derecho   = 50 %

Resultado esperado:

El robot se desplaza en línea recta.
La orientación no cambia.
```

Otro caso:

```text
Motor izquierdo = -50 %
Motor derecho   = 50 %

Resultado esperado:

El robot rota sobre su eje sin desplazamiento lineal intencional.
```

Los resultados numéricos deberán definirse utilizando unidades y convenciones documentadas.

---

# Cinemática

Antes de afirmar que la simulación es físicamente precisa deben definirse y verificarse:

- sistema de coordenadas;
- unidad de distancia;
- unidad angular;
- dirección correspondiente al ángulo cero;
- sentido positivo de rotación;
- distancia entre ruedas;
- relación entre porcentaje de motor y velocidad;
- paso temporal de simulación;
- tolerancias numéricas.

No asumas estas convenciones silenciosamente.

Deben documentarse.

---

# Python

Python será el lenguaje principal de programación mediante código.

El prototipo contiene actualmente una implementación experimental con sintaxis similar a Python.

No debe describirse como un intérprete completo de Python.

Una implementación futura podrá utilizar Pyodide dentro de un Web Worker.

Antes de considerar segura esta ejecución deberán evaluarse:

- ciclos infinitos;
- límites de tiempo;
- memoria;
- APIs disponibles;
- bloqueo de la interfaz;
- aislamiento;
- recuperación ante errores.

No afirmes que la ejecución es segura hasta haberla verificado.

---

# Programación mediante bloques

Blockly es la tecnología propuesta para la futura programación visual.

Los bloques y Python no deben implementar motores distintos de simulación.

Ambos métodos deberán utilizar una API común.

```text
Blockly ───────┐
               │
               ▼
           Robot API
               │
               ▼
         Simulación
               ▲
               │
Python ────────┘
```

---

# Dependencias

No agregues una dependencia importante sin documentar:

- por qué es necesaria;
- qué problema resuelve;
- qué alternativas existen;
- qué licencia utiliza.

También debes verificar que el problema no pueda resolverse razonablemente con las herramientas ya incluidas en el proyecto.

---

# Seguridad

Nunca subas al repositorio:

- contraseñas;
- tokens;
- claves privadas;
- service keys;
- secretos de Supabase;
- archivos `.env` con secretos;
- información personal de estudiantes.

---

# Privacidad

BuildBot Lab está pensado también para estudiantes de secundaria.

Debemos utilizar el principio de minimización de datos.

No agregues recopilación de información como:

- dirección particular;
- número de teléfono;
- fecha completa de nacimiento;
- centro educativo;
- nombre real obligatorio;

sin una necesidad documentada y una revisión de privacidad.

Las funciones relacionadas con:

- autenticación;
- analítica;
- almacenamiento en la nube;
- perfiles públicos;
- proyectos compartidos;

deberán ser revisadas antes de desplegarse públicamente.

---

# Documentación

La documentación deberá distinguir siempre entre:

## Implementado

Existe y ha sido verificado al nivel indicado.

## Experimental

Existe, pero todavía requiere validación.

## Planificado

Forma parte del desarrollo previsto, pero todavía no está implementado.

## Idea futura

Forma parte de la visión del proyecto pero todavía no existe un compromiso de implementación.

No presentes una funcionalidad planificada como si ya estuviera implementada.

---

# Definición de terminado

Un Issue puede considerarse terminado cuando:

- se completó el alcance acordado;
- se agregaron las pruebas aplicables;
- las pruebas relevantes se ejecutaron correctamente;
- se actualizó la documentación necesaria;
- se documentaron las limitaciones conocidas;
- la Pull Request fue revisada.

Nunca reportes pruebas que no hayan sido realmente ejecutadas.

---

# Licencia

Al contribuir a BuildBot Lab aceptas que tus contribuciones sean distribuidas bajo la licencia MIT del proyecto.
