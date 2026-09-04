# Plan PPL — Manual de entrenamiento

Página estática con el plan **Push / Pull / Legs** (Martes / Miércoles / Jueves).
23 ejercicios, cada uno con:

- **Foto real de ejecución**: posición inicial → final. En escritorio con el cursor;
  en el móvil tocando la foto o deslizando sobre ella (el botón indica en cuál de las
  dos posiciones estás).
- **Lámina anatómica** con el músculo objetivo resaltado en rojo (vista frontal o posterior).
- Series × repeticiones, RIR y la indicación técnica clave.

## Uso

Abrí `index.html` en el navegador. No necesita servidor ni dependencias.
Todos los recursos están en `assets/`, así que funciona sin conexión
(las tipografías de Google Fonts son lo único que se carga online, con
alternativas del sistema si no hay red).

## Editar el plan

Los ejercicios están en el array `DAYS` al final de `index.html`. Cada ficha es:

```js
{ name:'Sentadilla profunda', equip:'Barra libre o Smith',
  cue:'Cuádriceps y glúteo…', rir:'RIR 2', sets:'4 × 6-8',
  img:'Barbell_Full_Squat',   // carpeta en assets/exercises/
  view:'front',               // 'front' | 'back'
  m:['m10'],                  // superposiciones de assets/anatomy/
  muscle:'Cuádriceps' }
```

Referencia de superposiciones anatómicas (`assets/anatomy/`):

| Archivo | Músculo | Vista |
|---|---|---|
| `m1` | Bíceps braquial | frontal |
| `m2` | Deltoides anterior | frontal |
| `m3` | Serrato anterior | frontal |
| `m4` | Pectoral mayor | frontal |
| `m5` | Tríceps braquial | posterior |
| `m6` | Recto abdominal | frontal |
| `m7` | Gemelos | posterior |
| `m8` | Glúteo mayor | posterior |
| `m9` | Trapecio | posterior |
| `m10` | Cuádriceps | frontal |
| `m11` | Isquiotibiales | posterior |
| `m12` | Dorsal ancho | posterior |
| `m13` | Braquial anterior | frontal |
| `m14` | Oblicuos | frontal |
| `m15` | Sóleo | posterior |
| `m-adductors` | Aductores | frontal |

## Créditos y licencias

- **Fotografías de ejercicios**: [free-exercise-db](https://github.com/yuhonas/free-exercise-db)
  — base de datos abierta de 870+ ejercicios, dominio público (Unlicense).
- **Láminas anatómicas**: sistema muscular y superposiciones del proyecto
  [wger](https://github.com/wger-project/wger), licencia AGPL-3.0.
  `m-adductors.svg` es una adaptación de `m10` recortada a la cara interna del muslo.

Los SVG anatómicos se normalizaron con `viewBox` común (`0 0 200 369`) para poder
superponer base y músculo a cualquier tamaño.

## PyOS

IDE de Python que corre en el navegador (Pyodide), con tema oscuro estilo PyCharm/Darcula, resaltado de sintaxis, archivos, consola y REPL: [`pyos/`](pyos/index.html)
