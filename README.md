# Línea de Tiempo Interactiva: Evolución Técnica y Cultural del LaserDisc (1961–2009)

**Asignatura:** Cultura Digital  
**Grado / Máster:** Universitat Oberta de Catalunya (UOC)  
**Actividad:** PEC 1 – Cronología de un Objeto Cultural y Tecnológico  
**Repositorio GitHub:** [Heipry/timeline_laserdisc](https://github.com/Heipry/timeline_laserdisc)  
**Despliegue en Vivo:** [GitHub Pages - Timeline LaserDisc](https://heipry.github.io/timeline_laserdisc/)  

---

## 1. Descripción del Proyecto

Este proyecto consiste en el desarrollo e implementación de una línea de tiempo interactiva e hipermedia sobre la trayectoria histórica, tecnológica e industrial del **LaserDisc** (1961–2009), el primer soporte óptico analógico de consumo masivo de la historia.

A través de **12 hitos fundamentales**, la cronología analiza tres ejes interconectados:
1. **Hardware:** La evolución desde la patente del disco óptico transparente hasta los reproductores combinados y el cese de producción de Pioneer.
2. **Software / Interactividad:** Las innovaciones en cine interactivo (Dragon's Lair), la invención de los contenidos extra de edición crítica (Criterion Collection), los sistemas híbridos hipermedia (LV-ROM y BBC Domesday) y el control informático (Apple HyperCard).
3. **Industria / Mercado:** Las guerras de estándares de videodisco (óptico vs. capacitivo CED SelectaVision de RCA), las mutaciones de marca (DiscoVision / Magnavision / LaserVision / LaserDisc) y la democratización doméstica a través de colecciones divulgativas en España.

---

## 2. Arquitectura Técnica e Infraestructura (Self-Hosted)

El proyecto ha sido diseñado siguiendo una premisa de **portabilidad, soberanía de datos e independencia de servicios de terceros**:

* **Motor Visual:** [TimelineJS3](https://timeline.knightlab.com/) de Knight Lab, integrado localmente mediante contenedor `index.html`.
* **Soporte de Datos:** Archivo estructurado `timeline.json` codificado en UTF-8 con soporte para metadatos jerárquicos (fechas, titulares, descripciones ampliadas, enlaces de consulta externa y agrupaciones por categorías).
* **Alojamiento Local de Recursos Visuales:** Las imágenes críticas del proyecto han sido integradas en el directorio raíz para garantizar la longevidad del sitio y evitar enlaces rotos (*hotlinking* o caducidad de servidores externos).
* **Despliegue Continuo:** Alojamiento mediante **GitHub Pages** sincronizado directamente con la rama `main` del repositorio de GitHub.
---

## 3. Guía de Ejecución Local

Para visualizar o modificar el proyecto en un entorno de desarrollo local:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Heipry/timeline_laserdisc.git
   cd timeline_laserdisc
   ```

2. **Ejecutar un servidor local (opcional pero recomendado):**
   Dado que `timeline.json` es cargado por `index.html` vía petición `fetch`, se recomienda utilizar un servidor HTTP local para evitar restricciones CORS del navegador:
   ```bash
   # Utilizando Python 3
   python -m http.server 8000
   ```
   Luego abre `http://localhost:8000` en tu navegador. Alternativamente, se puede utilizar la extensión *Live Server* en VS Code.

---

## 4. Atribución Académica y Procedencia de Fuentes Visuales

En cumplimiento del marco legal de **Derecho de Cita y Uso Legítimo para Fines Docentes e Investigadores** (Art. 32 de la Ley de Propiedad Intelectual en España / Normativa de Honestidad Académica UOC), a continuación se detalla la procedencia exacta de los recursos visuales utilizados en la línea de tiempo:

| Archivo / URL | Descripción del Contenido | Titular Intelectual / Marca | Fuente de Procedencia |
| :--- | :--- | :--- | :--- |
| `pioneer_vp1000.jpg` | Anuncio promocional del reproductor Pioneer VP-1000 (1980) | Pioneer Electronic Corp. | Material publicitario de archivo histórico comercial. |
| `page9.jpg` | Página impresa "Round and Round They Go" en *Technology Review* (Oct/Nov 1975, p. 9) | MIT / Philips-MCA | Escaneo de publicación técnica (*Technology Review*, Vol. 78, N.º 1). |
| `s-l1600.webp` | Edición en LaserDisc de *King Kong* (Criterion Collection, 1984) | The Voyager Company / RKO | Fotografías de archivo de colección particular de discos. |
| `coleccion-animales.jpg` | Estuche de la obra *El mundo de los animales y su medio ambiente* (1992) | Editorial Planeta / Plaza & Janés | Fotografía de archivo particular de compraventa de segunda mano. |
| `DVL9.jpg` | Bandeja de lectura para LD/DVD/CD del Pioneer DVL-9 (1996) | Pioneer Electronic Corp. | Fotografía de producto comercial de tienda de tecnología Hi-Fi vintage. |
| `US3430966-drawings-page-1.png` | Esquema del disco óptico transparente en la Patente US3430966A (1961/1969) | David Paul Gregg / USPTO | Enlace de repositorio público [Google Patents](https://patents.google.com/patent/US3430966A/en). |
| `dsc_dv72.jpg` | Prototipo de videodisco de la presentación conjunta Philips-MCA (1972) | Philips / MCA | Archivo histórico digital de preservación [Total Rewind](https://www.totalrewind.org/). |
| `271f03df23...jpg` | Reproductor Magnavox Magnavision VH-8000 (1978) | Magnavox (Philips) / MCA | Archivo de documentación publicitaria de DiscoVision. |
| `bfxc4vmm22lf1.jpeg` | Mueble de la máquina recreativa *Dragon's Lair* (1983) | Cinematronics / Don Bluth Studios | Material promocional de recreativas de época. |
| `armstrong-tycake.jpg` | Fotografía de la presentación del BBC Domesday System en LV-ROM (1986) | BBC / Acorn Computers | Publicación académica digital [*Ariadne Magazine* (Issue 36)](https://www.ariadne.ac.uk/issue/36/tna/). |
| `LaserDisc.png` | Captura de interfaz de pila HyperCard LaserStacks (1987) | Apple Computer / Bantam Books | Documentación sobre software histórico Mac OS. |
| `CF07F1E4...heic` | Reproductor de la última serie Pioneer DVL-919 (2009) | Pioneer Corporation | Catálogo de distribución Hi-Fi vintage ([Record Mart Hi-Fi](https://recordmarthifi.com/)). |

---

## 5. Licencia y Créditos

* **Texto y Contenidos Académicos:** Desarrollados bajo licencia [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es) (Atribución-NoComercial-CompartirIgual).
* **Software:** TimelineJS3 (Knight Lab) distribuido bajo Licencia Mozilla Public License v2.0.
* **Marcas registradas:** Los nombres de marcas comerciales (*LaserDisc*, *DiscoVision*, *Magnavision*, *SelectaVision*, *Pioneer*, *Philips*, *Criterion Collection*, *HyperCard*) pertenecen a sus respectivos titulares y son utilizados exclusivamente con fines analíticos y divulgativos.