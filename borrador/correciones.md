# Lista de Correcciones y Observaciones del Documento de Tesis

Documento base: `main.tex`  
Título actualizado: **«Sistema de reconstrucción tridimensional mediante 3DGS y técnicas de inteligencia artificial para la identificación de vulnerabilidades en viviendas autoconstruidas»**  
Fecha de actualización: 30 de septiembre de 2026  
Institución: Universidad Nacional Mayor de San Marcos (UNMSM) — FISI  

---

## Resumen Ejecutivo del Estado del Documento

| Componente | Estado Previo | Estado Actual | Verificación |
| :--- | :--- | :--- | :---: |
| **Título y Metadatos** | Genérico / Incompleto | Actualizado en portada y `\hypersetup` | [x] |
| **Portada Institucional** | Placeholders en blanco | Completado (FISI, Ing. de Software, Dr. Ciro Rodríguez) | [x] |
| **Preliminares** | Inexistentes | Dedicatoria, Agradecimientos, Resumen y Abstract redactados | [x] |
| **Marco DSR (Pilares)** | 5 OEs dispersos sin trazabilidad | 4 Pilares DSR ($PE_i \leftrightarrow OE_i \leftrightarrow CE_i$) alineados | [x] |
| **Estructura de Capítulos** | Contradicción (6 vs. 7 capítulos) | 7 Capítulos consolidados con Marco Teórico y RSL en Cap. II | [x] |
| **Estado del Arte (RSL)** | 5 bloques de *Lorem Ipsum* | Síntesis analítica completa en Q1 a Q5 sin texto simulado | [x] |
| **Tablas de la RSL** | Papers ajenos (cabello, hidrocarburos, modas) | Sustituidos por literatura de 3DGS, arquitectura y visión 3D | [x] |
| **Bibliografía (`.bib`)** | 4 referencias básicas | 22 referencias completas vinculadas con `\citep` y `\citet` | [x] |
| **Conclusiones y Discusión**| Textos guía de plantilla | Conclusión general y 4 específicas redactadas formalmente | [x] |
| **Apéndice A (Matriz)** | Texto de plantilla | Matriz de Consistencia completa en formato horizontal | [x] |

---

## 1. Nivel Crítico (Resuelto)

### [CRIT-01] Desfase de subtítulos en el Marco Teórico
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Las tipologías de autoconstrucción (informal, asistida, progresiva, comunitaria) se agruparon bajo la Sección 2.6 (`Autoconstrucción de viviendas y riesgos estructurales`). Se redactó la Sección 2.7 técnica sobre inspección visual, ensayos no destructivos (NDT) y cumplimiento de las normas técnicas peruanas RNE E.060 (Concreto Armado) y RNE E.070 (Albañilería Confinada).

### [CRIT-02] Contradicción en la organización y estructura de capítulos
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se unificó la estructura a 7 capítulos de acuerdo con las directrices de Design Science Research (DSR):
  1. Capítulo I: Introducción (Planteamiento del problema y objetivos DSR).
  2. Capítulo II: Marco teórico y estado del arte (RSL Kitchenham + Bases de ingeniería civil).
  3. Capítulo III: Análisis y formalización de requisitos (OE1, ISO/IEC/IEEE 29148).
  4. Capítulo IV: Diseño y arquitectura de la solución (OE2, UML 2.5.1 y algoritmos de proyección 2D-3D).
  5. Capítulo V: Implementación del prototipo y curaduría del dataset (OE3, FastAPI, 3DGS, YOLO, dron/iPhone).
  6. Capítulo VI: Resultados y validación experimental (OE4, $E = (D,M,B,P,R)$, ISO/IEC 25010).
  7. Capítulo VII: Discusión, conclusiones y recomendaciones ($OE_i \leftrightarrow C_i$).

### [CRIT-03] Texto simulado (*Lorem Ipsum*) en la RSL
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se redactaron análisis críticos originales para cada una de las 5 preguntas de investigación (Q1: Métodos de reconstrucción; Q2: Ventajas y limitaciones de 3DGS; Q3: Datasets y brecha de autoconstrucción; Q4: Métricas fotométricas y geométricas; Q5: Aplicaciones y justificación del sistema propuesto). No queda ningún término "lorem" en el documento.

### [CRIT-04] Inconsistencias temáticas en las tablas de la RSL
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se auditaron y depuraron las Tablas 2.1, 2.2, 2.4, 2.5 y 2.6. Se sustituyeron los artículos que violaban los criterios de exclusión (animación capilar, generación de caras parlantes, hidrogeles de grafeno, diseño de modas) por investigaciones fundamentales y recientes de reconstrucción 3D y superficies de edificaciones:
  * *Scaffold-GS* (CVPR 2024): Renderizado adaptativo de estructuras.
  * *SuGaR* (CVPR 2024): Extracción de superficies y mallas a partir de 3DGS.
  * *2D Gaussian Splatting* (SIGGRAPH 2024): Precisión geométrica y consistencia de normales.
  * *VastGaussian* (CVPR 2024): Reconstrucción escalable de escenas urbanas y sitios de construcción.
  * *CityGaussian* (ECCV 2024): Renderizado de edificaciones y entornos a gran escala.
  * *GaussianPro* (ICML 2024): Propagación planar para reconstrucción de superficies de edificaciones.
  * *Octree-GS* (ScienceDirect 2025): Topografía aérea y niveles de detalle para arquitectura.
  * En la Tabla 2.6 (Q5), se asignaron aplicaciones pertinentes a cada artículo (gemelos digitales, cálculo de volúmenes, inspección aérea con drones, documentación de patrimonio).

---

## 2. Nivel Metodológico y Conceptual (Resuelto)

### [MET-01] Alineación conceptual: «Vulnerabilidades» vs. «Deficiencias observables»
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se precisó en el Resumen, Introducción, Objetivos y Conclusiones que el sistema realiza una identificación y localización de *vulnerabilidades físicas a través de deficiencias constructivas observables y no conformidades normativas* (fisuras, segregación, armadura expuesta, muros sin confinar), actuando como herramienta de triaje y asistencia técnica preliminar sin sustituir el cálculo analítico global de cargas.

### [MET-02] Coherencia en los 4 Pilares DSR
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** La captura de datos de campo se estableció formalmente como una actividad metodológica y un insumo experimental ($D$), integrándose dentro del OE3 (curaduría del dataset y prototipo), permitiendo que los 4 OEs reflejen los pilares del artefacto tecnológico: Formalización, Diseño Arquitectónico, Implementación y Evaluación Experimental.

---

## 3. Referencias Bibliográficas y Formato (Resuelto)

### [BIB-01] Citas huérfanas en el texto
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se actualizaron y enriquecieron las entradas de `referencias.bib` con metadatos completos y normalizados:
  * `castro2024`, `murillo2012`, `malatesta2007`, `luzdaconceicao2023`, `ardilaitriago2018`, `caf2017`.
  * `grade2023`, `inei2024`, `chumpitaz2023`, `flores2024`, `sencico2023`, `gao2023`.
  * `kitchenham2007`, `peffers2007`, `iso29148`, `iso25010`.
  * `kerbl2023`, `mildenhall2020`, `colmaptutorial`, `rneportal`.
  * `guedon2024_sugar`, `huang2024_2dgs`, `lin2024_vastgaussian`.
  Se reemplazaron todas las menciones en texto plano por comandos `\citep{...}` y `\citet{...}`.

---

## 4. Figuras, Tablas, Conclusiones y Apéndices (Resuelto)

### [EST-01] Captions de diagramas de Ishikawa
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se diferenciaron claramente:
  * Figura 3.1: *«Diagrama de Ishikawa de causas de la informalidad constructiva»*.
  * Figura 3.2: *«Diagrama de Ishikawa de limitaciones operativas de los actores involucrados»*.

### [EST-02] Referencia cruzada estática
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se cambió `Tabla 2.2` fija por `\ref{tab:criterios-inclusion-exclusion}`.

### [EST-03] Conclusiones y Discusión del Capítulo VII
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se eliminaron todos los textos de instrucción (*«Redactar la conclusión sobre...»*) y se redactó la Discusión completa, la Conclusión General y las 4 Conclusiones Específicas correspondientes a cada objetivo DSR.

### [EST-04] Matriz de Consistencia y Material Complementario
* **Estado:** **Resuelto [x]**
* **Acción ejecutada:** Se sustituyó el texto preliminar del Apéndice A por una tabla detallada en formato apaisado (`landscape`) de la **Matriz de Consistencia lógica DSR**. El Apéndice D se estructuró con el inventario técnico de paquetes del repositorio Git, servicios Docker Compose y acceso a evidencias.
