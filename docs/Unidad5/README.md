# Unidad 5: Reconocimiento de Imágenes
## Índice de Archivos

### Archivos Creados

#### 1. **Unidad5_Introduccion.qmd** → `Unidad5_Introduccion.html`
- **Tipo**: Documento introductorio (HTML)
- **Propósito**: Overview de la unidad, estructura, relación con unidades anteriores
- **Contenido**:
  - Propósito general de la Unidad 5
  - Estructura modular (3 documentos)
  - Flujo recomendado de estudio
  - Competencias a desarrollar
  - FAQ sobre selección de algoritmos
  - Recursos y referencias

---

#### 2. **Unidad5_01_Algoritmos_Supervisados_NoSupervisados.qmd** → `Unidad5_01_Algoritmos_Supervisados_NoSupervisados_handout.html`
- **Tipo**: Documento conceptual con código ejecutable (HTML Quarto jupyter)
- **Secciones**:
  1. Propósito y objetivos
  2. Introducción al flujo de reconocimiento
  3. **Aprendizaje Supervisado**:
     - Regresión Logística (idea, ventajas, implementación)
     - SVM (kernels, margin, implementación)
     - Árboles de Decisión (partición, interpretabilidad)
     - Random Forest (ensemble, importancia)
  4. **Aprendizaje No-supervisado**:
     - K-means (repaso, aplicación a características)
     - Clustering Jerárquico (dendrograma, linkage)
  5. **Reducción de Dimensionalidad**:
     - PCA (varianza, componentes principales)
     - t-SNE (visualización no-lineal)
  6. Pipeline típico (scaler + classifier)
  7. Tabla comparativa de algoritmos
  8. Consideraciones prácticas (escalamiento, data leakage, hiperparámetros)
  9. Referencias

- **Librerías clave**: scikit-learn, numpy, matplotlib

---

#### 3. **Unidad5_02_Evaluacion_Desempeno.qmd** → `Unidad5_02_Evaluacion_Desempeno_handout.html`
- **Tipo**: Documento conceptual con código ejecutable (HTML Quarto jupyter)
- **Nota**: Nombre sin caracteres especiales para compatibilidad con todos los sistemas operativos
- **Secciones**:
  1. Motivación: exactitud no es suficiente
  2. Matriz de confusión y métricas derivadas:
     - TP, FP, FN, TN
     - Exactitud, Precisión, Recall, F1, Especificidad
     - Extensión a multiclase (macro, micro, weighted)
  3. Validación Cruzada:
     - k-fold, stratified k-fold
     - Variantes (LOO, time series)
  4. Curvas ROC:
     - Concepto de threshold, TPR vs FPR
     - AUC (área bajo la curva)
     - Cuándo usar ROC
  5. Curvas Precision-Recall:
     - Alternativa para desbalance severo
  6. Búsqueda de Hiperparámetros:
     - GridSearchCV (exhaustiva)
     - RandomizedSearchCV (eficiente)
     - Evitar overfitting durante búsqueda
  7. Flujo completo de evaluación
  8. Tabla de contextos y métricas
  9. Referencias

- **Librerías clave**: scikit-learn, matplotlib, seaborn

---

#### 4. **ejemplo_real_Unidad5_clasificacion_flores.qmd** → `ejemplo_real_Unidad5_clasificacion_flores_handout.html`
- **Tipo**: Ejemplo completo ejecutable (HTML Quarto jupyter)
- **Flujo**:
  1. **Librerías** e importaciones
  2. **Descargar dataset** (TensorFlow flowers, 4 clases)
  3. **Extracción de características**:
     - GLCM (72 características)
     - Hu (7 características)
     - Color (9 características)
     - Total: 88 características por imagen
  4. **Preparación de datos**:
     - División 70% train / 30% test (estratificada)
     - Escalamiento StandardScaler
  5. **Modelos Supervisados** (entrenamiento y evaluación):
     - Logistic Regression
     - SVM (RBF kernel)
     - Random Forest
     - Decision Tree
  6. **Modelos No-supervisados**:
     - K-Means con etiquetado posterior
  7. **Comparación Global**:
     - Tabla de exactitud y F1
     - Gráfico comparativo
  8. **Validación Cruzada**:
     - 5-Fold Estratificado
     - Comparación de F1 CV entre modelos
  9. **Matrices de Confusión**: 
     - Visualización de 4 modelos supervisados
  10. **Curvas ROC** (one-vs-rest multiclase)
  11. **Análisis de Características Importantes**:
     - Top 20 características
     - Importancia por familia (GLCM, Hu, Color)
  12. **Conclusiones y Recomendaciones**

- **Datasets usados**: Flowers (4 clases: daisy, sunflowers, roses, tulips)
- **Salidas principales**: acuracidad, F1, matrices, curvas ROC, gráficos comparativos

---

#### 5. **style.css**
- **Tipo**: Hoja de estilos
- **Basada en**: style.css de Unidad 4
- **Propósito**: Consistencia visual en documentos HTML
- **Elementos**:
  - Colores (primario, acento, éxito, advertencia, peligro)
  - Estilos para headings, código, tablas
  - Links, blockquotes, alertas
  - Print-friendly

---

## Correspondencia con Contenidos Solicitados

### Capítulos del Curso → Archivos de Unidad 5

```
5. Reconocimiento de imágenes
  └── 5.1 Aprendizaje automático
      └── Unidad5_01_Algoritmos... (Introducción general)
      
  └── 5.2 Algoritmos supervisados aplicados a imágenes
      └── Unidad5_01_Algoritmos... (Secciones 1.1-1.4)
      └── ejemplo_real_Unidad5... (Secciones 5.1-5.4)
      
  └── 5.3 Algoritmos no-supervisados aplicados a imágenes
      └── Unidad5_01_Algoritmos... (Sección 2)
      └── ejemplo_real_Unidad5... (Sección 6)
      
  └── 5.4 Reducción de la dimensión
      └── Unidad5_01_Algoritmos... (Sección 3)
      
  └── 5.5 Evaluación del desempeño de los modelos
      └── Unidad5_02_Evaluacion... (Todas las secciones)
      └── ejemplo_real_Unidad5... (Secciones 8-12)
```

---

## Consistencia Asegurada

### ✓ Estructura Didáctica
- Sigue patrón Unidad 4: teoría + ejemplo real
- Documentos independientes pero conectados
- Progresión: conceptos → implementación → comparación

### ✓ Profundidad y Rigor
- Ecuaciones matemáticas (KaTeX) para fundamento
- Implementación completa en scikit-learn
- Consideraciones prácticas (data leakage, overfitting)
- Comparación cuantitativa de algoritmos

### ✓ Librerías y Funciones
- **OpenCV**: lectura, preprocesamiento (como Unidades 1-4)
- **scikit-learn**: modelos, pipelines, evaluación
- **scikit-image**: GLCM, grayscale co-ocurrence
- **scipy**: estadísticas, clustering
- **numpy, pandas**: manipulación de datos
- **matplotlib, seaborn**: visualización

### ✓ Dataset Reutilizado
- Flowers de Unidad 4: 4 clases (daisy, sunflowers, roses, tulips)
- Descarga automática en ejemplo_real
- Extracción de características (GLCM, Hu, Color) idéntica a Unidad 4

### ✓ Funciones Consistentes
- `extract_glcm_features()`: idéntica a Unidad 4
- `extract_hu_features()`: idéntica a Unidad 4
- `extract_color_moments()`: idéntica a Unidad 4

---

## Sugerencias de Uso en Aula

### Sesión 1 (2-3 horas):
- Leer Unidad5_Introduccion.qmd
- Clase magistral basada en Unidad5_01_Algoritmos...
- Q&A sobre selección de algoritmos

### Sesión 2 (2 horas):
- Clase magistral Unidad5_02_Evaluacion...
- Casos prácticos: qué métrica usar en cada contexto

### Sesión 3-4 (3-4 horas laboratorio):
- Ejecutar ejemplo_real_Unidad5... paso a paso
- Modificar parámetros, observar cambios
- Experimentar: cambiar K en K-Means, C en SVM, profundidad en árboles

### Sesión 5 (Proyecto):
- Aplicar flujo a dataset propio del estudiante
- Reportar: selección de algoritmo, justificación, resultados

---

## Archivos Generados (Resumen)

| Archivo | Tipo | Salida HTML | Líneas |
|---------|------|------------|--------|
| Unidad5_Introduccion.qmd | Intro | Unidad5_Introduccion.html | ~280 |
| Unidad5_01_Algoritmos_Supervisados_NoSupervisados.qmd | Teoría + código | ...handout.html | ~650 |
| Unidad5_02_Evaluacion_Desempeño.qmd | Teoría + código | ...handout.html | ~550 |
| ejemplo_real_Unidad5_clasificacion_flores.qmd | Ejemplo | ...handout.html | ~650 |
| style.css | Estilos | (no aplica) | ~100 |

**Total**:  ~2,230 líneas de contenido educativo

---

## Próximos pasos (para docente)

1. ✓ Archivos creados en Unidad5/
2. **Pendiente**: Renderizar .qmd a HTML (requiere Quarto CLI)
   ```bash
   quarto render Unidad5/Unidad5_Introduccion.qmd
   quarto render Unidad5/Unidad5_01_Algoritmos_Supervisados_NoSupervisados.qmd
   quarto render Unidad5/Unidad5_02_Evaluacion_Desempeño.qmd
   quarto render Unidad5/ejemplo_real_Unidad5_clasificacion_flores.qmd
   ```
3. **Opcional**: Crear notebooks .ipynb si prefieres ambiente Jupyter puro
4. **Opcional**: Revisar/ajustar ejemplos para contexto local

---

**Unidad 5 completa y lista para usar. ✓**
