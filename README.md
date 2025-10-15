# 📊 Análisis de Negocio: Ventas, Clientes e Insights

> **Proceso ETL completo con Pandas** | Análisis exploratorio de datos de ventas y clientes

[![Python 3.10](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Pandas >=1.5](https://img.shields.io/badge/Pandas-1.5%2B-green.svg)](https://pandas.pydata.org/)
[![Conda ENTORNO-ABP](https://img.shields.io/badge/Conda-ENTORNO--ABP-orange.svg)](https://docs.conda.io/)

---

## 🎯 Descripción del Proyecto

Este proyecto implementa un **proceso ETL completo** (Extract, Transform, Load) utilizando Pandas para analizar datos de ventas y clientes de centros comerciales. El análisis incluye limpieza de datos, transformaciones avanzadas, análisis exploratorio y generación de insights de negocio.

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
# 1. Clonar el repositorio
git clone <repository-url>
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
└── 📁 datos_procesados/                                  # Resultados (generado)
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
- ✅ Exportación de resultados

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

### 🔍 Análisis por Dimensiones
- **Demográfico:** Comportamiento por género y edad
- **Productos:** Precios y categorías más rentables
- **Temporal:** Tendencias mensuales y estacionales
- **Geográfico:** Rendimiento por centros comerciales

---

## 🛠️ Tecnologías Utilizadas

### 📚 Librerías Principales
- **Pandas** - Manipulación de datos
- **NumPy** - Operaciones numéricas
- **Matplotlib** - Visualizaciones básicas
- **Seaborn** - Visualizaciones avanzadas

### 🐍 Entorno de Desarrollo
- **Python 3.10** - Lenguaje principal
- **Conda** - Gestión de entornos
- **Jupyter Lab** - Entorno interactivo

### 📦 Dependencias Completas
```yaml
# Análisis de datos
pandas>=1.5.0
numpy>=1.21.0

# Visualización
matplotlib>=3.5.0
seaborn>=0.11.0

# Procesamiento
openpyxl>=3.0.9
python-dateutil>=2.8.0

# Desarrollo
jupyter>=1.0.0
jupyterlab>=3.0.0
```

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
3. Revisar resultados y visualizaciones

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

### ✅ **Análisis de Datos**
8. ✅ Análisis exploratorio completo
9. ✅ Resumen, evaluación y síntesis del estudio

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

---

## 📚 Documentación Adicional

- **`DIAGRAMA_BASE_DATOS.md`** - Diagrama de base de datos y relaciones
- **Comentarios en el código** - Documentación inline detallada
- **Docstrings** - Documentación de funciones principales

---

## 🤝 Contribución

### 🔄 Flujo de Trabajo
1. Fork del repositorio
2. Crear rama para nueva feature
3. Realizar cambios y pruebas
4. Enviar Pull Request

### 📝 Estándares de Código
- Seguir PEP 8 para Python
- Documentar funciones complejas
- Incluir comentarios explicativos

---

## 📄 Licencia

Este proyecto es parte de un trabajo académico del **ISPC** (Instituto Superior Politécnico de Córdoba).

---

## 👥 Autores

**Equipo de Desarrollo:**
- ARRUTI, ISSETTA, MRAD
- **Materia:** Programación y Base de Datos
- **Institución:** ISPC

---

<div align="center">

**🎓 Trabajo Práctico - ISPC**  
*Proceso ETL completo con Pandas*

[⬆️ Volver al inicio](#-análisis-de-negocio-ventas-clientes-e-insights)

</div>