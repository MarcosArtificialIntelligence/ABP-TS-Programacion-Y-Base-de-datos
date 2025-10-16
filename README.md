# 📈 Análisis de Negocio: Ventas, Clientes e Insights

> **Proceso ETL completo con Pandas y SQL** | Análisis exploratorio de datos de ventas y clientes

[![Python 3.10](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Pandas >=1.5](https://img.shields.io/badge/Pandas-1.5%2B-green.svg)](https://pandas.pydata.org/)
[![Conda ENTORNO-ABP](https://img.shields.io/badge/Conda-ENTORNO--ABP-orange.svg)](https://docs.conda.io/)
[![SQLite](https://img.shields.io/badge/SQLite-3.x-lightblue.svg)](https://sqlite.org/)

---

## 🎯 Descripción del Proyecto

Este proyecto implementa un **proceso ETL completo** (Extract, Transform, Load) utilizando Pandas y SQLite para analizar datos de ventas y clientes de centros comerciales. El análisis incluye limpieza de datos, transformaciones avanzadas, análisis exploratorio y generación de insights de negocio con validación SQL.

### 🎓 Contexto Académico
- **Materia:** Programación y Base de Datos
- **Trabajo:** Exploración, Transformación y Limpieza de Datos
- **Dataset:** Sales and Customer data (Kaggle)
- **Objetivo:** Implementar proceso ETL completo para análisis de datos

---

## 🚀 Inicio Rápido

### 📋 Prerequisitos
- **Python 3.10**
- **Anaconda/Miniconda**

### ⚡ Instalación en 3 pasos

```bash
# 1. Clonar el repositorio o correr el cd
git clone https://github.com/MarcosArtificialIntelligence/ABP-TS-Programacion-Y-Base-de-datos.git

cd ABP-TS-Programacion-Y-Base-de-datos-ARRUTI-ISSETTA-MRAD

# 2. Crear y activar entorno conda
conda env create -f environment.yml
conda activate ENTORNO-ABP

# 3. Ejecutar el análisis
jupyter lab
```

### 📂 Estructura del Proyecto

```
📁 Proyecto/
├── 📓 Analisis-de-negocio-Ventas-Clientes-Insights.ipynb  # Notebook principal
├── 📁 Dataset-Kaggle/                                     # Datos originales
│   ├── customer_data.csv                                  # 99,457 clientes
│   └── sales_data.csv                                     # 99,457 transacciones
├── 📄 environment.yml                                     # Entorno conda
├── 📄 requirements.txt                                    # Dependencias pip
├── 📄 DIAGRAMA_BASE_DATOS.md                             # Diagrama de BD
├── 📄 .gitignore                                          # Archivos ignorados
└── 📄 ventas_clientes.db                                 # Base de datos SQLite (generado)
```

---

## 🔍 Proceso ETL Implementado

### 📥 **Extract** - Extracción de Datos
- ✅ Carga de archivos CSV desde `Dataset-Kaggle/`
- ✅ Validación de estructura y tipos de datos
- ✅ Verificación de integridad referencial

### 🔄 **Transform** - Transformación de Datos
- ✅ Limpieza y normalización de datos
- ✅ Categorización por edad y género
- ✅ Análisis de métodos de pago por segmentos
- ✅ Cálculo de métricas derivadas

### 📤 **Load** - Carga de Datos
- ✅ DataFrame final con datos limpios
- ✅ Validación de restricciones de integridad
- ✅ Carga a base de datos SQLite

---

## 📊 Análisis Realizados

### 🎯 Métricas Clave
- **99,457 transacciones** analizadas
- **99,457 clientes únicos**
- **Período:** 2021-2023
- **Calidad de datos:** 100% completitud

### 📈 Insights Principales
- **Género predominante:** Female (59.7% de ventas)
- **Grupo etario líder:** 51+ años (36.3% de ventas)
- **Categoría top:** Clothing (45.3% de ventas)
- **Método de pago:** Cash (44.7% de transacciones)

### 📊 Visualizaciones Profesionales
El notebook incluye **dashboard ejecutivo** con visualizaciones de nivel empresarial:

#### 🎨 **Dashboard Ejecutivo Principal**
- **Heatmap demográfico** para segmentación por género y edad
- **Gráficos de barras horizontales** para top categorías por ingresos
- **Gráficos de pie** para distribución de métodos de pago
- **Tendencias temporales** con análisis de evolución

#### 📋 **Validación SQL**
- **Base de datos SQLite** con todos los datos del ETL
- **Consultas SQL** que validan los hallazgos clave
- **Tablas estilizadas** con formato profesional

---

## 🛠️ Tecnologías Utilizadas

### 📚 Librerías Principales
- **Pandas** - Manipulación de datos
- **NumPy** - Operaciones numéricas
- **Matplotlib** - Visualizaciones básicas
- **Seaborn** - Visualizaciones avanzadas
- **SQLite3** - Base de datos local (built-in)

### 🐍 Entorno de Desarrollo
- **Python 3.10** - Lenguaje principal
- **Conda** - Gestión de entornos
- **Jupyter Lab** - Entorno interactivo

---

## 🎮 Uso del Proyecto

### 🖥️ Interfaz Recomendada
```bash
# Opción 1: JupyterLab (recomendado)
conda activate ENTORNO-ABP
jupyter lab

# Opción 2: Jupyter Notebook
conda activate ENTORNO-ABP
jupyter notebook
```

### 📓 Ejecución del Notebook
1. Abrir `Analisis-de-negocio-Ventas-Clientes-Insights.ipynb`
2. Ejecutar celdas secuencialmente (Shift + Enter)
3. **Especial atención a la celda 3** que contiene el dashboard ejecutivo
4. **Celda 5** incluye la validación SQL de los hallazgos clave
5. Revisar resultados y dashboards ejecutivos

### 🔄 Ejecución Alternativa
```bash
# Convertir a script Python
jupyter nbconvert --to python Analisis-de-negocio-Ventas-Clientes-Insights.ipynb
python Analisis-de-negocio-Ventas-Clientes-Insights.py
```

---

## 📋 Consignas Implementadas

### ✅ **Extracción de Datos (Extract)**
1. ✅ Carga de datos CSV en DataFrames separados
2. ✅ Descripción detallada del proceso de extracción
3. ✅ Unificación de DataFrames con información relevante

### ✅ **Transformación de Datos (Transform)**
4. ✅ Transformaciones adicionales implementadas:
   - Modo de pago más frecuente por género
   - Métodos de pago por rango etario (25-35 años)
   - Métodos de pago más utilizados por mujeres
   - Precios por categoría de productos
5. ✅ Documentación completa de transformaciones

### ✅ **Carga de Datos (Load)**
6. ✅ DataFrame final con datos limpios y transformados
7. ✅ Restricciones de integridad aplicadas y documentadas

### ✅ **Base de Datos SQL**
8. ✅ Carga de datos a base de datos SQLite
9. ✅ Consultas SQL que validan los hallazgos clave
10. ✅ Formato profesional de tablas SQL

### ✅ **Análisis de Datos**
11. ✅ Análisis exploratorio completo
12. ✅ Resumen, evaluación y síntesis del estudio

---

## 🎯 Resultados del Análisis

### 📊 Dashboard de Métricas
```
🎯 MÉTRICAS GENERALES
├── Período: 01/01/2021 - 08/03/2023
├── Clientes únicos: 99,457
├── Transacciones: 99,457
├── Ingresos totales: $251,505,794.25
└── Valor promedio: $2,528.79

👥 INSIGHTS POR GÉNERO
├── Female: $150,207,136.02 (59.7%)
└── Male: $101,298,658.23 (40.3%)

👴 INSIGHTS POR EDAD
├── 18-25: $38,075,393.69 (15.2%)
├── 26-35: $47,826,744.49 (19.0%)
├── 36-50: $74,133,147.83 (29.5%)
└── 51+: $91,193,246.77 (36.3%)
```

### 🏆 Top Categorías por Ventas
1. **Clothing** - $113,996,791.04 (45.3%)
2. **Shoes** - $66,553,451.47 (26.5%)
3. **Technology** - $57,862,350.00 (23.0%)

---

## 🔧 Personalización

### 📝 Modificar Rutas de Datos
```python
# En la celda de carga de datos
customer_file = "ruta/a/tu/customer_data.csv"
sales_file = "ruta/a/tu/sales_data.csv"
```

### 🎨 Personalizar Visualizaciones
```python
# Modificar configuración de gráficos
plt.style.use('seaborn-v0_8')
sns.set_palette("viridis")
```

### 📊 Agregar Nuevas Métricas
```python
# Extender análisis en celdas adicionales
custom_analysis = final_df.groupby('shopping_mall')['total_amount'].sum()
```

### 🗄️ Consultas SQL Personalizadas
```python
# Agregar nuevas consultas SQL
custom_query = """
SELECT category, COUNT(*) as transacciones
FROM ventas_clientes 
GROUP BY category
ORDER BY transacciones DESC
"""
result = pd.read_sql_query(custom_query, conn)
```

---

## 🐛 Solución de Problemas

### ❌ Error: "No se encontró el archivo"
```bash
# Verificar estructura de directorios
ls -la Dataset-Kaggle/
# Asegurar que los archivos CSV estén presentes
```

### ❌ Error: "Memory Error"
```python
# Para datasets grandes, usar procesamiento por chunks
chunk_size = 10000
for chunk in pd.read_csv(file, chunksize=chunk_size):
    # Procesar chunk
```

### ❌ Error de Dependencias
```bash
# Reinstalar entorno completo
conda env remove -n ENTORNO-ABP
conda env create -f environment.yml
```

### ❌ Error de Base de Datos SQLite
```python
# Verificar que sqlite3 esté disponible (built-in en Python)
import sqlite3
print(sqlite3.version)
```

---

## 📚 Documentación Adicional

- **`DIAGRAMA_BASE_DATOS.md`** - Diagrama de base de datos y relaciones
- **Comentarios en el código** - Documentación inline detallada
- **Docstrings** - Documentación de funciones principales
- **`ventas_clientes.db`** - Base de datos SQLite generada

---

## 🎨 **Características del Proyecto**

### 📊 **Visualizaciones Profesionales**
- **Diseño ejecutivo** con paleta de colores coherente
- **Insights destacados** en cada gráfico
- **Formato profesional** listo para presentaciones
- **Dashboard integrado** con múltiples tipos de gráficos

### 🗄️ **Base de Datos SQL**
- **SQLite integrado** para persistencia de datos
- **Consultas optimizadas** para validación de hallazgos
- **Tablas estilizadas** con formato profesional
- **Validación cruzada** entre Pandas y SQL

### 📈 **Valor para Ciencia de Datos**
- **Comunicación efectiva** de hallazgos complejos
- **Storytelling con datos** para audiencias ejecutivas
- **Validación estadística** de hipótesis
- **Base sólida** para toma de decisiones estratégicas

**✅ Proceso ETL completo con Pandas y SQL implementado exitosamente**

---

## 👥 Autores

**Equipo de Desarrollo:**
- **ARRUTI Marcos Agustín** - Análisis y desarrollo
- **ISSETTA Rocío Belén** - Documentación y testing
- **ARRUTI Julián Alejandro** - Visualizaciones y diseño
- **MRAD Caro Farid Yusef** - Base de datos y SQL

**Materia:** Programación y Base de Datos  
**Institución:** ISPC - Instituto Superior Politécnico de Córdoba

---

<div align="center">

**🎓 Trabajo Práctico - ISPC**  
*Proceso ETL completo con Pandas y SQL*

[⬆️ Volver al inicio](#-análisis-de-negocio-ventas-clientes-e-insights)

</div>