# HEMOTECA 1.0 · Plataforma Integral de Hemoterapia e Inmunohematología

App web progresiva (PWA), sin dependencias externas, que funciona sin conexión tras la primera carga.

> **Aviso:** proyecto académico y de consulta. Los resultados simulados no corresponden a pacientes reales y **no autorizan la liberación ni la transfusión de hemocomponentes**. No sustituye los POE, la normativa vigente ni la valoración profesional. No ingreses datos identificables.

## Contenido
Estudio (inmunohematología, banco de sangre, hemocomponentes, medicina transfusional, reacciones adversas) con buscador, favoritos y progreso · Compatibilidad (simulador y tabla) · Calculadoras con fórmula visible y validación · Simulador de laboratorio (ABO/RhD, rastreo, prueba cruzada AHG) · Casos con decisiones ramificadas · Evaluaciones con corrección · Biblioteca · Notas, historial, exportar/importar JSON.

## Estructura
`index.html`, `manifest.json`, `service-worker.js`, `css/styles.css`, `js/app.js`, `data/*.json` (preguntas, casos, bibliografía, tablas), `assets/icons/`.

## Publicar en GitHub
1. Crea un repositorio **público** llamado `hemoteca-1.0` en github.com.
2. Sube **todo el contenido de la carpeta** (con sus subcarpetas) a la raíz: con GitHub Desktop (Add local repository → Commit → Push) o con «Add file → Upload files».
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
4. Tras 1–2 minutos, abre `https://TU-USUARIO.github.io/hemoteca-1.0/`.

## Instalar en iPhone y probar sin conexión
1. Abre la dirección en **Safari** → Compartir → **Añadir a pantalla de inicio**.
2. Abre la app desde el ícono con internet y navega por todas las secciones.
3. Activa el modo avión, cierra la app por completo y vuelve a abrirla: debe cargar y funcionar (la etiqueta superior dirá «Sin conexión»).
4. Para actualizar tras cambiar archivos, sube el cambio y aumenta `V` en `service-worker.js`.

## Ampliar contenido
Preguntas, casos, bibliografía y tablas están en `data/`. Agrega elementos con el mismo formato y vuelve a subir; no hay que tocar el código.

## Pruebas
**Ejecutadas (Node):** sintaxis de `app.js` y `service-worker.js`; validez de los JSON; fórmulas (Hb final, volumen, CCI), interpretación ABO (4 grupos y una discrepancia) y selección de componentes.
**Pendientes (requieren dispositivo):** Safari/iPhone, instalación, funcionamiento sin conexión, persistencia tras cerrar la app, exportación en iOS, revisión científica por un especialista.

## Limitaciones conocidas
Banco inicial de 13 preguntas y 3 casos (ampliables). Los valores, vigencias y rangos son generales y varían según normativa, fabricante y protocolo local.
