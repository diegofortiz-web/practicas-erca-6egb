# Prácticas preprofesionales · Recursos digitales por fase del ciclo ERCA

Plantilla para publicar en **GitHub Pages** las planificaciones microcurriculares basadas en el **ciclo de aprendizaje ERCA** y el recurso digital de cada fase.
*Si tu planificación usa los momentos ACC (Anticipación, Construcción, Consolidación), usa la plantilla **practicas-acc-6egb**.*

| Fase ERCA | Propósito | Recurso del ejemplo |
|---|---|---|
| 1. Experiencia | Parte de una vivencia o situación concreta | Video (YouTube) |
| 2. Reflexión | Analiza y comenta la experiencia | Juego (Educaplay) |
| 3. Conceptualización | Construye el nuevo conocimiento | Presentación o infografía (Canva) |
| 4. Aplicación | Aplica lo aprendido | Cuestionario (Kahoot o Wayground) |

El ejemplo usa las tres planificaciones de **Informática Educativa, 6.º grado de EGB, Escuelas Municipales de Loja** (Unidad 2: *Utilizando Office: Word*).

---

## Estructura del sitio

```
index.html        → página (no se edita)
datos.js          → TUS DATOS Y ENLACES (el único archivo que editas)
assets/           → estilos, programa y logos de la UNL (no se editan)
recursos/         → aquí subes PDF o imágenes propias (opcional)
.nojekyll         → archivo necesario para GitHub Pages (no lo borres)
```

---

## Paso 1. Crear tu repositorio

1. Ingresa a <https://github.com> con tu cuenta (si no tienes, créala con tu correo institucional).
2. Abre el repositorio de la plantilla que compartió el docente y pulsa **Use this template ▸ Create a new repository**.
   *Si no aparece ese botón, crea un repositorio nuevo con **New**, márcalo como **Public** y sube los archivos de esta carpeta con **Add file ▸ Upload files**.*
3. Ponle un nombre sin espacios, por ejemplo: `practicas-erca-6egb`.

## Paso 2. Publicar con GitHub Pages

1. En tu repositorio entra a **Settings ▸ Pages**.
2. En **Build and deployment ▸ Source** elige **Deploy from a branch**.
3. En **Branch** elige **main** y la carpeta **/ (root)**. Pulsa **Save**.
4. Espera uno o dos minutos y recarga la página: aparecerá tu dirección, con este formato:
   `https://TU-USUARIO.github.io/practicas-erca-6egb/`

## Paso 3. Insertar tus recursos (iframes)

Abre `datos.js`, pulsa el ícono del lápiz (**Edit**) y completa, para cada fase, el campo `embed` con el enlace de inserción de tu recurso:

| Plataforma | Dónde se obtiene el enlace | Forma del enlace |
|---|---|---|
| YouTube | Compartir ▸ Insertar | `https://www.youtube.com/embed/CODIGO` |
| Educaplay | Compartir ▸ Insertar | `https://es.educaplay.com/juego/…` |
| Canva | Compartir ▸ Más ▸ Insertar | `https://www.canva.com/design/…/view?embed` |
| Wayground (Quizizz) | Compartir ▸ Insertar | `https://wayground.com/embed/…` |
| Heyzine (flipbook) | Share ▸ Embed | `https://heyzine.com/flip-book/….html` |
| Kahoot | No permite insertarse | Usa el campo `enlace` con el enlace del juego |

**Consejo:** puedes pegar el enlace solo o el código `<iframe …>` completo; la página toma el enlace automáticamente.

Ejemplo:

```js
reflexion: {
  actividad: "En parejas relacionan cada parte de la ventana de Word con su función…",
  recurso: "Educaplay «Relacionar columnas: partes de Word» (8 pares)",
  plataforma: "Educaplay",
  embed: "https://es.educaplay.com/juego/1234567-partes_de_word.html",
  enlace: ""
},
```

Guarda con **Commit changes**. En uno o dos minutos la página se actualiza sola.

## Paso 4. Datos de la práctica, flipbook y software educativo

- En `datos.js` cambia tus datos en `datos` (estudiante, ciclo, paralelo).
- En `flipbook.embed` pega el enlace de inserción de tus planificaciones en Heyzine.
  También puedes subir el PDF a la carpeta `recursos/` y escribir `enlace: "recursos/planificaciones.pdf"`.
- **Software educativo (Pilas Engine)**, al final de la página, después de la tercera planificación:
  1. En Pilas Engine abre tu juego y expórtalo como **HTML** (se descarga un `.zip`).
  2. Descomprímelo y sube su contenido a la carpeta `recursos/pilas-engine/` de tu repositorio
     (**Add file ▸ Upload files**). El archivo principal debe llamarse `index.html`.
  3. En `datos.js` escribe `embed: "recursos/pilas-engine/index.html"` dentro de `software`.
  *Si tu juego ya está publicado en internet, pega su enlace en `embed` o en `enlace`.*

---

## Identidad visual (Manual Corporativo UNL)

La plantilla ya aplica el manual; **no cambies** los colores, las tipografías ni los logotipos de `assets/`.

- Colores corporativos: rojo `#BF0811`, verde `#4F8E3A`, azul `#004C7B`, negro `#211915`.
- Tipografías: Montserrat en los títulos y Arial en los textos.
- El logotipo no se estira, no se gira, no se recolorea ni se coloca dentro de cajas; sobre fondos de color se usa su versión monocromática (blanca).
- El nombre de la carrera acompaña al logotipo como texto, separado por una línea vertical, como indica el manual para carreras y dependencias.

## Antes de entregar

- [ ] La página abre en la dirección de GitHub Pages.
- [ ] Cada fase de cada planificación muestra su recurso o, en Kahoot, el botón para abrirlo.
- [ ] El juego de Pilas Engine se abre y se puede jugar al final de la página.
- [ ] Los recursos son públicos (cualquier persona con el enlace puede verlos).
- [ ] No se publican fotos, nombres ni datos personales de los niños.
- [ ] Las imágenes y textos de terceros se citan en formato APA 7.

Envía al docente tutor la dirección de tu página (`https://…github.io/…`) por el EVA.
