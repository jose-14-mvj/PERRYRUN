# 🦆 Perry Runner 3D

Videojuego **endless runner 3D** hecho en Unity, inspirado en el juego del dinosaurio de Chrome. Perry, un ornitorrinco universitario con chaqueta y sombrero, corre por una ciudad inspirada en La Paz esquivando obstáculos y juntando monedas para llegar a tiempo a clases.

▶️ **Jugar online:** https://jose-14-mvj.github.io/PERRYRUN/

> Proyecto de la asignatura **Game Development · Unidad 2: Scripting y matemáticas para videojuegos**.

---

## 🎮 Cómo se juega

Perry corre solo hacia adelante. Tú decides cuándo saltar y cuándo deslizarte. Solo se usa el teclado.

| Tecla | Acción | Para qué sirve |
|---|---|---|
| ↑ Flecha arriba | Saltar | Esquivar obstáculos bajos (vallas) |
| ↓ Flecha abajo | Deslizarse | Pasar bajo obstáculos altos (barras) |
| R o Enter | Reiniciar | Volver a empezar al terminar la partida |

> Haz clic una vez dentro del juego para que reciba el teclado.

## 📏 Reglas y puntuación

- Empiezas con **3 vidas**. Cada choque con un obstáculo quita una vida; con 0 vidas aparece **JUEGO TERMINADO** y tu puntuación final.
- **10 puntos por segundo** sobrevivido.
- Las **monedas doradas** aparecen en filas de tres y dan **+25 puntos** cada una.
- Al llegar a **1000 puntos** aparece **¡NUEVO RÉCORD!** con tu puntuación y las monedas juntadas.
- Tras un golpe tienes **1,2 s de invulnerabilidad**.
- Los obstáculos aparecen al azar, cada **1,3 a 2,4 s**, y siempre dejan tiempo para aterrizar o levantarse.

## ⚡ Dificultad

El mundo parte a **11 u/s** y acelera **0,18 u/s cada segundo**, así que el juego se vuelve más rápido mientras más sobrevives.

| Parámetro | Valor |
|---|---|
| Altura del salto | 2,6 m |
| Duración del deslizamiento | 1,1 s |
| Vidas | 3 |
| Puntos para el récord | 1000 |

## 🧍 Personaje y arte

- **Perry**: ornitorrinco aventurero, valiente y decidido, con chaqueta universitaria vino y sombrero marrón.
- Estilo **Cartoon 3D (Low Poly)**: formas simples, colores llamativos y ambientación de ciudad universitaria inspirada en La Paz.
- Creado a partir de un concepto 2D y generado como modelo 3D en **Tripo** (modo Modelo HD).
- **4 animaciones:** Correr (en bucle), Saltar, Agacharse y Morir.

## 🛠️ Tecnología

- **Unity 6** (6000.6.1f1), scripts en C#
- Build **Web** (WebGL) publicada con **GitHub Pages**
- Portal en HTML, CSS y JavaScript puro, sin dependencias

---

## 📁 Qué hay en este repositorio

```
PERRYRUN/
├── index.html        Portal del juego (historia, personaje, mecánicas, datos, galería y botón para jugar)
├── README.md         Esta guía
├── .nojekyll         Evita que GitHub Pages procese los archivos con Jekyll
├── assets/
│   ├── personaje.png     Imagen de Perry (fondo transparente)
│   ├── captura.png       Captura principal del juego
│   └── galeria-1..4.jpg  Capturas de la galería
└── juego/            Build Web de Unity (lo que se carga al presionar "Jugar")
    ├── index.html
    ├── Build/
    └── TemplateData/
```

## ▶️ Probarlo en tu computadora

El juego no abre haciendo doble clic en el archivo; necesita un servidor local. Desde esta carpeta:

```
python -m http.server 8000
```

y abre http://localhost:8000

## 🚀 Publicar o actualizar el juego

1. En Unity: **File → Build Profiles → Web → Build**.
2. Antes, en *Player Settings → Publishing Settings*, pon **Compression Format = Disabled** (GitHub Pages no sirve bien archivos `.br` o `.gz`).
3. Reemplaza el contenido de `juego/` con la carpeta generada (`index.html`, `Build/`, `TemplateData/`).
4. Sube los cambios:

```
git add .
git commit -m "Actualizar build del juego"
git push
```

5. En unos minutos GitHub Pages muestra la nueva versión. Si no ves cambios, actualiza con Ctrl+F5.

> Límite de GitHub: ningún archivo puede pesar más de 100 MB.

## 👥 Equipo

**Los Pato Locos**
- Mijhail Alvaro Vichini Fernandez
- Mario Macuchapi Villa
