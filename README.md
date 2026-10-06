# Auditoría de RSE · Liderazgo y Administración

Taller colaborativo en el que equipos de estudiantes auditan la responsabilidad social de una empresa mexicana (Grupo Bimbo, FEMSA, Cemex, Walmart de México y Centroamérica o ASUR). Combina el análisis de las **5 fuerzas de Porter** con una **auditoría de RSE en 4 áreas** (ambiental, social, gobernanza y económica) y termina en un **reporte en PDF** que cada estudiante sube a Brightspace.

Escuela Internacional de Negocios · Universidad Anáhuac Cancún.

## Contenido del repositorio

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La aplicación completa en un solo archivo. No requiere instalación ni compilación. |
| `README.md` | Este documento. |
| `.nojekyll` | Indica a GitHub Pages que publique el archivo tal cual. |

## Qué hace la aplicación

1. **Registro:** cada estudiante elige su grupo (Liderazgo o Administración) y su empresa; el equipo marca a sus integrantes en la lista del grupo y cada quien entra con su nombre.
2. **Responsabilidades:** cada integrante asume un rol: Coordinación, Análisis Porter, Auditoría RSE, Fuentes y APA o Redacción del dictamen.
3. **Fase 1 · Porter:** 2 preguntas por fuerza, intensidad (baja, media, alta) y fuente.
4. **Fase 2 · RSE:** 3 preguntas por área con cifras y fuente; se pide al menos una fuente independiente.
5. **Fase 3 · Evaluación:** calificación del 1 al 10 por área con justificación, recomendación, relación Porter + RSE y dictamen.
6. **Reporte:** mapa de Porter, radar de RSE, semáforo, hallazgos, integrantes con sus responsabilidades y referencias en APA 7. Se descarga en PDF con el nombre del estudiante.

Incluye la sección «¿Qué se pide?» con criterios de evaluación y ejemplos de respuesta débil frente a respuesta esperada, además de un ejemplo resuelto completo con una empresa ficticia.

## Importante: qué funciona fuera de Claude

La versión original se publicó como página de Claude (claude.ai), que aporta una **base de datos compartida**, la **identificación de la cuenta** de cada visitante y la **presencia en vivo**. GitHub Pages solo sirve archivos; no tiene esos servicios. Por eso:

| Función | En Claude (claude.ai) | En GitHub Pages |
|---|---|---|
| Ver instrucciones, criterios y ejemplo resuelto | ✅ | ✅ |
| Registrar equipo y trabajar en las fases | ✅ | ✅ solo en ese navegador y mientras la página siga abierta |
| Trabajo simultáneo del equipo desde varios dispositivos | ✅ | ❌ |
| Guardado automático del avance | ✅ | ❌ se pierde al recargar |
| Descargar el reporte en PDF o HTML | ✅ | ✅ |
| Panel docente, registro de accesos, participación y entregas | ✅ | ❌ |

**Recomendación:** para la clase, usa el enlace de Claude. El repositorio sirve como respaldo del código, para compartirlo con otros docentes y como punto de partida si se conecta una base de datos propia (por ejemplo Firebase o Supabase) para tener trabajo compartido fuera de Claude.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `auditoria-rse`.
2. Sube los archivos de esta carpeta: **Add file → Upload files**, arrastra `index.html`, `README.md` y `.nojekyll`, y confirma con **Commit changes**.
   - `.nojekyll` es un archivo oculto; si tu computadora no lo muestra, puedes omitirlo.
3. Ve a **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`, y guarda.
5. En uno o dos minutos la página queda en `https://TU-USUARIO.github.io/auditoria-rse/`.

## Modificar las listas de estudiantes

Las listas están en `index.html`, en la constante `GRUPOS`. Cada estudiante es un par `["Apellidos","Nombres"]`:

```js
const GRUPOS=[{k:"L",n:"Liderazgo",off:0,lista:[["Álvarez García","Sofía Ximena"], ...]},
 {k:"A",n:"Administración",off:5,lista:[["Escobar Ramos","José René"], ...]}];
```

Para agregar a alguien, añade un par dentro de `lista`, separado por coma. No se guardan correos electrónicos en el archivo porque la página es pública.

## Modificar empresas y fuentes

Las cinco empresas y sus ligas están en la constante `EMP`; el directorio general de fuentes, en `DIRG`. Las preguntas de Porter están en `PORTER` y las de RSE en `RSE`.

## Tecnologías

React 18, html2canvas y jsPDF, cargados desde cdnjs. Tipografías Archivo e IBM Plex Mono desde Google Fonts. Se necesita conexión a internet para cargarlos.
