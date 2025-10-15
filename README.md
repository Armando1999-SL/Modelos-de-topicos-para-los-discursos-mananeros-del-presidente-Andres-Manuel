# Modelos de tópicos para los discursos mañaneros del presidente Andrés Manuel López Obrador

Este proyecto implementa un **modelo de tópicos** para analizar los discursos mañaneros del expresidente **Andrés Manuel López Obrador**.

Un **tópico** es una variable latente que representa o resume los conceptos principales de un texto. Está compuesto por un conjunto de palabras relacionadas semánticamente dentro de un contexto.

## Problema

Identificar los **tópicos más relevantes** en los discursos mañaneros y distinguir los principales temas abordados.

## Enfoque de solución

1. **Preprocesamiento de texto**: limpieza y selección de palabras relevantes.  
2. **Representación TF-IDF**: para obtener la importancia de cada término en los discursos.  
3. **Descomposición SVD**: probando distintos valores de *k* tópicos. Aunque útil, presentaba problemas de interpretabilidad debido a valores negativos en las matrices factorizadas.  
4. **Factorización No Negativa de Matrices (NMF)**: alternativa más adecuada para datos TF-IDF, ya que garantiza interpretabilidad y permite una clusterización más clara de los tópicos.  

Se exploraron también métodos de reducción de dimensionalidad como **PCA**, **Kernel PCA** y **t-SNE**, pero NMF resultó ser la opción más sólida para el objetivo.

## Resultados

Los principales temas identificados en las conferencias fueron:

1. **México** (palabras comunes como: *pueblo, gente, méxico, transformación, país*).  
2. **Programas de apoyo del gobierno**.  
3. **Tren Maya**.  
4. **Energía eléctrica**.  
5. **Pandemia**.  

Al aumentar el número de tópicos (*k*), surgieron también otros como:  
- Educación  
- Vacunas  
- Expresidentes y personajes relacionados con corrupción  

## Archivos del repositorio

- **conferencias_matutinas_amlo-master**  
  Base de datos con todos los discursos mañaneros desde 2019 hasta marzo de 2024.  

- **codigo.ipynb**  
  Implementación del modelo de tópicos y análisis.  

- **spanish.txt**  
  Lista de *Stop Words* utilizadas en el preprocesamiento.  

- **reporte.pdf**  
  Documento con los resultados del análisis.  

---

🔗 **Repositorio con los discursos:**  
[Conferencias Matutinas AMLO - GitHub](https://github.com/NOSTRODATA/conferencias_matutinas_amlo)
