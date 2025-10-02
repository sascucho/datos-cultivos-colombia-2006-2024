# 🌾 Análisis Exploratorio de Datos (EDA) de Cultivos en Colombia (2006-2024)

## 📌 Introducción y Objetivo del Proyecto

Este proyecto constituye un **Análisis Exploratorio de Datos (EDA)** del sector agrícola en Colombia, utilizando la información histórica de la **Evaluación Agropecuaria (EVA)**.

El objetivo principal fue **consolidar y limpiar** las bases de datos históricas (2006-2018 y 2019-2024) y generar hallazgos visuales sobre la distribución del área sembrada en el país durante este periodo.

---

## 🛠️ Metodología y Herramientas

### 1. Fuentes de Datos
* **Origen:** Evaluaciones Agropecuarias Municipales (EVA) del DANE / UPRA.
* **Periodo Consolidado:** 2006 a 2024.

### 2. Herramientas
* **Entorno:** Google Colab.
* **Lenguaje:** Python.
* **Librerías Clave:**
    * **Pandas:** Para la carga, consolidación, limpieza y transformación de datos (unión de bases, manejo de valores nulos y mapeo de categorías).
    * **Unidecode/Regex:** Utilizadas en la fase de limpieza para la normalización avanzada de nombres de cultivos y departamentos (eliminación de tildes, mayúsculas y caracteres especiales, y corrección manual por diccionario de mapeo).
    * **Matplotlib / Seaborn:** Para la visualización de los resultados del EDA.

### 3. Fases del Proceso
1.  **Consolidación:** Carga y concatenación de las dos bases de datos (2006-2018 y 2019-2024).
2.  **Limpieza y Homogeneización:** Normalización de las columnas categóricas (`Cultivo`, `Departamento`), incluyendo un **diccionario de mapeo manual** para corregir inconsistencias lógicas (ej: agrupar variaciones de un mismo cultivo).
3.  **Análisis Exploratorio:** Conteo de datos faltantes, verificación de unicidad y análisis del área sembrada.
4.  **Visualización:** Creación de un gráfico de barras para el ranking de los 10 cultivos con mayor área sembrada acumulada.

---

## 📊 Hallazgos Clave del EDA

El análisis del área sembrada entre 2006 y 2024 reveló la estructura dominante del sector:

| Ranking | Cultivo (FINAL CORREGIDO) | Área Sembrada Acumulada (ha) |
| :---: | :--- | :--- |
| **#1** | [CAFE] | [16`014.408,67] |
| **#2** | [ARROZ] | [10`919.929,20] |
| **#3** | [MAIZ] | [10`879.069,82] |
| _..._ | _..._ | _..._ |
| **#10** | [CANA PANELERA	] | [2`837.352,49] |

> **Conclusión Principal:** El análisis del área sembrada acumulada entre 2006 y 2024 revela una estructura agrícola fuertemente cimentada en la **tradición y el valor de exportación**. El **Café** se consolida como el cultivo con la mayor extensión territorial, liderando el ranking y subrayando su continua relevancia económica y cultural en la producción nacional. Este dominio es seguido de cerca por el **Arroz** y el **Maíz**, lo que indica una estructura dual donde conviven la producción de la canasta básica (Maíz, Arroz) y los cultivos agroindustriales de renta (Palma, Caña de Azúcar). El Top 10 demuestra que los cultivos de ciclo **Permanente** ocupan la mayor parte del suelo agrícola en el largo plazo.
---

## 💾 Acceso al Código

El código completo del proyecto, incluyendo todos los pasos de la consolidación, la limpieza (normalización y mapeo) y la generación del gráfico final, se encuentra en el siguiente cuaderno de Google Colab:

* [**`datos_colombia.ipynb`**](datos_colombia.ipynb) *(Clic para ver el código)*
