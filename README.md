[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Fs-anpaq)

#  DeepForest: Análisis de Imágenes Aéreas

Este proyecto utiliza el modelo preentrenado **DeepForest** para detectar árboles en imágenes aéreas RGB y realizar un análisis visual y cuantitativo con resultados en gráficos y un archivo `.csv`.

---

##  Configuración del ambiente

Realiza la configuración del ambiente de `conda` siguiendo las instrucciones oficiales:  
🔗 https://deepforest.readthedocs.io/en/v1.5.0/getting_started/install.html

---

##  Recursos

- Documentación general de DeepForest: https://deepforest.readthedocs.io/en/v1.5.0/
- Repositorio oficial: https://github.com/weecology/DeepForest
- Tutorial usado:  
   https://deepforest.readthedocs.io/en/v1.5.0/getting_started/intro_tutorials/03_use_pretrained_model.html

---

##  Objetivo

Aplicar el modelo preentrenado de **DeepForest** para detectar árboles en una imagen aérea personalizada y realizar un análisis completo, incluyendo:

- Visualización con cajas y etiquetas.
- Cálculo de áreas.
- Análisis de vegetación (índices ExG y VARI).
- Estadísticas RGB e interpretación visual.
- Exportación de resultados.

---

##  Imagen usada

La imagen usada en el proyecto es:
mi_imagen/imagen_taller7.jpg

Esta puede ser reemplazada por cualquier imagen RGB de alta resolución.

---

##  Actividades

1. **Carga de imagen y predicción**
   - Se carga la imagen personalizada y se aplica el modelo `weecology/deepforest-tree` para detectar árboles.

2. **Visualización con identificadores**
   - Se muestra la imagen con *bounding boxes* y un identificador numérico por árbol detectado.

3. **Cálculo de áreas y dataframe**
   - Se calcula el área en píxeles de cada árbol.
   - Se genera un dataframe con: `id_arbol`, `xmin`, `ymin`, `xmax`, `ymax`, `area_px`.

4. **Índices de vegetación**
   - Se calculan:
     - **ExG** = `2*G - R - B`
     - **VARI** = `(G - R) / (G + R - B + ε)`
   - Se obtiene el valor medio de cada índice por árbol detectado.

5. **Histogramas RGB**
   - Se grafican histogramas de intensidad en los canales R, G y B comparando árboles vs no árboles.

6. **Diagramas de dispersión RGB**
   - Se grafican R vs G, G vs B y R vs B diferenciando regiones de árboles y no árboles mediante colores.

7. **Exportación de datos**
   - Toda la información procesada se guarda en un archivo `.csv` (`datos_arboles.csv`).

---

##  Estructura del proyecto

deepforest-chachi-solve/
├── analisis_arboles.ipynb # Cuaderno principal del proyecto
├── datos_arboles.csv # DataFrame con resultados exportado
├── mi_imagen/
│ └── imagen_taller7.jpg # Imagen usada en el análisis
├── requirements.txt # Librerías necesarias
└── README.md # Este archivo

## Entrega esperada
✅ analisis_arboles.ipynb: el cuaderno con todo el proceso documentado.

✅ datos_arboles.csv: archivo con resultados por árbol detectado.

✅ Visualizaciones generadas: cajas, histogramas, diagramas RGB.

## INTEGRANTES DE CHACHI SOLVE
Farid Pedroza

Joan Rincón

Juan Guerra
