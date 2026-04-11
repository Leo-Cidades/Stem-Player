<div align="center">

# Stem Player
### Simulador virtual de un proyecto físico

Aplicación web local hecha con **Node.js** para cargar, reproducir y mezclar canciones separadas en **4 pistas** desde una interfaz simple.

</div>

---

## Descripción

Este repositorio contiene **solo el simulador virtual** del proyecto **Stem Player**.

El proyecto original nació como una idea física, pero esta versión está pensada para usarse desde la computadora, ejecutándose con un **Node server** y una interfaz web local.

El simulador permite trabajar con canciones separadas en estas 4 pistas:

- **vocals**
- **other**
- **bass**
- **drums**

Desde la interfaz se pueden reproducir las pistas en simultáneo, mutearlas, ajustar el volumen de cada una y moverse entre canciones o carpetas.

> El ZIP del proyecto contiene el código del programa correspondiente a esta versión virtual.

---

## Funciones

- Reproducción sincronizada de 4 pistas
- Control de volumen independiente por pista
- Mute / unmute por pista
- Play / pausa
- Canción anterior y siguiente
- Rebobinado y avance rápido
- Barra de progreso
- Carga de una carpeta individual o de una carpeta principal con subcarpetas
- Guardado y aplicación de presets de volumen

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
└── public/
    ├── index.html
    ├── scripts.js
    └── styles.css
```

---

## Requisitos

Solo necesitas:

- **Node.js** instalado
- un navegador moderno  
  Recomendado: **Google Chrome** o **Microsoft Edge**

---

## Instalación

1. Descarga o extrae el ZIP del proyecto.
2. Abre una terminal dentro de la carpeta del proyecto.
3. Ejecuta:

```bash
npm install
```

---

## Ejecución

Con el proyecto ya instalado, inicia el servidor con el comando:

```bash
node server
```

Luego abre en el navegador:

```bash
http://localhost:3000/
```

---

## Uso

### 1. Abrir una canción

La interfaz ofrece dos opciones:

- **Abrir Carpeta Principal**  
  Para cargar una carpeta que contenga varias subcarpetas, cada una con una canción.

- **Abrir Carpeta Específica**  
  Para cargar directamente una sola canción.

### 2. Formato esperado

Cada canción debe estar dentro de una carpeta con estas 4 pistas:

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

### 3. Controles disponibles

Desde la interfaz puedes:

- reproducir y pausar
- ir a la canción anterior o siguiente
- rebobinar
- adelantar
- mover la barra de progreso
- mutear o desmutear cada pista
- ajustar el volumen de cada pista
- guardar un preset
- aplicar un preset guardado

---

## Atajos de teclado

También hay atajos para **mutear y desmutear** pistas rápidamente:

- `1` → vocals
- `2` → other
- `3` → bass
- `4` → drums

---

## Recomendación

Para conseguir canciones separadas en pistas, se recomienda usar **Stem Roller**:

[https://www.stemroller.com/](https://www.stemroller.com/)

---

## Notas

- El proyecto está pensado para ejecutarse en entorno local.
- Si falta alguna de las 4 pistas, la canción no podrá cargarse correctamente.
- La organización correcta de las carpetas es importante para que el simulador funcione bien.

---

## Créditos

Desarrollado por:

- **Leonel Cidades**
