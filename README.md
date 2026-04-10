<div align="center">

# Stem Player
### Simulador virtual de un proyecto físico

Proyecto web ejecutado con **Node.js** que permite cargar una canción separada en **4 pistas** y controlarlas desde una interfaz local.

</div>

---

## Descripción

Este repositorio contiene **solo la parte del simulador virtual** del proyecto **Stem Player**.

El proyecto original fue concebido como un dispositivo físico con controles dedicados, pero esta versión está orientada a la **simulación en PC** mediante un **Node server** y una interfaz web local.

La aplicación permite trabajar con una canción separada en cuatro stems:

- **vocals**
- **other**
- **bass**
- **drums**

Desde la interfaz se pueden reproducir las pistas en simultáneo, mutearlas, cambiar sus volúmenes, navegar entre canciones y guardar presets de mezcla.

> El ZIP del proyecto contiene el código del programa correspondiente a esta versión virtual.

---

## ¿Qué hace este simulador?

El simulador permite probar digitalmente la lógica del proyecto sin depender del armado físico.

Entre sus funciones principales están:

- reproducción sincronizada de 4 pistas
- control de volumen independiente por pista
- mute / unmute por pista
- play / pausa
- pista anterior y siguiente
- rebobinado y avance rápido
- barra de progreso
- carga de una carpeta individual o de una carpeta principal con subcarpetas
- guardado y aplicación de presets de volumen

---

## Tecnologías usadas

- **Node.js**
- **Express**
- **HTML**
- **CSS**
- **JavaScript**
- **Web Audio API**

---

## Estructura del proyecto

```bash
.
├── server.js
├── package-lock.json
├── node_modules/
└── public/
    ├── index.html
    ├── scripts.js
    └── styles.css
```

### Archivos principales

- **server.js**  
  Inicia el servidor local en el puerto `3000` y sirve los archivos estáticos.

- **public/index.html**  
  Contiene la estructura visual del reproductor.

- **public/scripts.js**  
  Maneja la lógica del simulador: carga de carpetas, reproducción, volumen, mute, presets y navegación.

- **public/styles.css**  
  Define el estilo visual de la interfaz.

---

## Requisitos

Para ejecutar el simulador necesitas:

- **Node.js** instalado
- un navegador moderno compatible con selección de carpetas  
  **Recomendado:** Google Chrome o Microsoft Edge

---

## Instalación

### Opción 1: usar el ZIP tal como está

Extrae el archivo ZIP del proyecto en una carpeta local.

En el ZIP ya se incluye el código del programa, junto con los archivos necesarios para correr esta versión virtual.

### Opción 2: reinstalar dependencias manualmente

Si necesitas reinstalar la dependencia principal, ejecuta:

```bash
npm install express
```

---

## Ejecución

Abre una terminal dentro de la carpeta del proyecto y corre:

```bash
node server.js
```

Luego abre en el navegador:

```bash
http://localhost:3000/
```

---

## Uso

### 1. Iniciar la aplicación

Ejecuta el servidor y abre la interfaz en el navegador.

### 2. Cargar una canción

La interfaz ofrece dos formas de carga:

- **Abrir Carpeta Principal**  
  Permite seleccionar una carpeta que contenga varias subcarpetas, cada una con una canción.

- **Abrir Carpeta Específica**  
  Permite abrir directamente una sola carpeta de canción.

### 3. Formato esperado de las pistas

Cada canción debe estar organizada en una carpeta con estas cuatro pistas:

```bash
Cancion/
├── vocals.mp3
├── other.mp3
├── bass.mp3
└── drums.mp3
```

También pueden usarse otros formatos compatibles con el navegador, siempre que los nombres base sean:

- `vocals`
- `other`
- `bass`
- `drums`

### 4. Controles disponibles

Desde la interfaz puedes:

- reproducir y pausar
- avanzar a la siguiente canción
- volver a la canción anterior
- rebobinar
- adelantar
- mover la barra de progreso
- mutear pistas individuales
- ajustar volumen por pista
- guardar un preset
- aplicar un preset guardado

---

## Atajos de teclado

El simulador también permite alternar mute rápidamente:

- `1` → vocals
- `2` → other
- `3` → bass
- `4` → drums

---

## Relación con el proyecto físico

Este simulador virtual forma parte de un proyecto más amplio que originalmente contemplaba controles físicos y comunicación con ESP32.

Sin embargo, este repositorio está enfocado únicamente en la **versión virtual ejecutada desde Node.js**, por lo que puede probarse sin montar el hardware.

---

## Notas

- El proyecto está pensado para ejecutarse en entorno local.
- Si falta alguna de las 4 pistas, la canción no podrá cargarse correctamente.
- La interfaz incluye lógica relacionada con ESP32, pero no es necesaria para probar el simulador virtual.
- La experiencia depende de que las carpetas estén bien organizadas.

---

## Créditos

Desarrollado por:

- **Leonel Cidades**
- **Tobias Godoy**

Materia: **Computadoras Electrónicas**

---

## Resumen

**Stem Player** es un **simulador virtual de un proyecto físico** realizado para funcionar con un **Node server**.

Permite cargar canciones separadas en cuatro pistas y controlarlas desde una interfaz web local.

