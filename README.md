<h1 align = "center"> Laboratorio 2 - Conociendo a Pepper </h1>

<h2 align = "center"> Grupo 2 </h2>
<p align = "center"> Díaz Suesca, Díaz Vargas, López Maldonado </p>
<br><br>
<p align = "center"> Sistemas Digitales III </p>



# Introducción

<p align = "justify">
Este documento introduce tres frentes de trabajo para la primera interacción con el robot \*\*Pepper\*\*: (1) una revisión de las librerías esenciales del ecosistema NAOqi, (2) la creación de una coreografía sencilla en \*\*Choregraphe\*\*, y (3) el acceso por \*\*SSH\*\* para programar pasos básicos desde la terminal. El objetivo es que el estudiante comprenda el propósito de cada herramienta y la secuencia general de tareas antes de entrar en el detalle técnico.
</p>
---

## 1\) Librerías clave para el funcionamiento de Pepper

<p align = "justify">
El stack de Pepper se apoya en NAOqi y en librerías de Python que permiten comunicación, control de movimiento y manejo de datos.
> \*\*Resultado esperado:\*\* Identificar para qué sirve cada librería y cuándo usarla en un script típico que controle o consulte capacidades de Pepper.
</p>
---

## 2\) Choregraphe: instalación y creación de una coreografía sencilla

**Choregraphe** es el entorno visual de NAOqi para diseñar comportamientos sin programar desde cero. En esta fase se busca una primera secuencia de movimientos/acciones:

* **Instalación y conexión**: Instalar Choregraphe en el PC, abrir el proyecto base y conectarse al robot (o simulador) introduciendo la IP del Pepper.
* **Construcción del flujo**: Arrastrar *boxes* (p. ej., *ALMotion → Posture*, *Animation*, *Say*) y conectarlas para crear una **secuencia** coherente (saludo → postura inicial → pasos simples → despedida).
* **Parámetros clave**: Ajustar tiempos, velocidades y transiciones (p. ej., `setAngles`, `goToPosture`, duración de animaciones, *timelines*).
* **Prueba y despliegue**: Ejecutar en modo *play* sobre el robot/simulador, iterar hasta lograr suavidad, y guardar el comportamiento como proyecto.

> \*\*Resultado esperado:\*\* una \*\*coreografía breve\*\* (10–20 s) que combine postura inicial, uno o dos gestos del torso/brazos, desplazamientos mínimos y un mensaje de voz.

---

## 3\) Acceso por SSH y creación de pasos básicos desde terminal

Para comprender el flujo «bajo nivel», se accede a Pepper por **SSH** y se desarrollan pasos simples mediante un script de Python:

* **Ingreso por terminal**: Conectarse con `ssh nao@ip\_Pepper`. Verificar acceso, espacio disponible y rutas relevantes para scripts.
* **Creación del archivo**: Abrir un editor de consola (p. ej., `nano`) y crear un script que:

  * Establezca una **sesión `qi`** con el robot.
  * Obtenga el servicio **ALMotion** (`motion`) y, si aplica, **ALTextToSpeech**.
  * Use `almath`/`math` para cálculos mínimos (ángulos, pausas).
  * Ejecute una **secuencia corta**: postura inicial → mover articulaciones → pequeña pausa → volver a reposo.
  * Emplee `argparse` para parámetros como IP/puerto y `json`/`os` para leer configuración simple.

* **Ejecución y registro**: Dar permisos si fuese necesario, ejecutar el script, observar comportamiento y anotar el **comportamiento observado**, mensajes en consola y cualquier ajuste de seguridad/estabilidad (p. ej., límites de velocidad o postura).

> \*\*Resultado esperado:\*\* un \*\*script documentado\*\* (comentado) que pueda correrse desde la terminal para reproducir una secuencia de pasos básicos y que explique claramente qué librerías se usaron y por qué.

---

## Cierre

<p align = "justify">
Tras completar estas tres etapas, el estudiante habrá reconocido las \*\*librerías fundamentales\*\*, sabrá \*\*crear y ajustar\*\* una coreografía en Choregraphe y tendrá la \*\*base práctica\*\* para controlar a Pepper por terminal, sentando las condiciones para trabajos más complejos de percepción, diálogo y navegación.

</p>

