# 📈 Análisis de Negocio: Ventas, Clientes e Insights

> **Análisis ETL completo para identificación de segmentos de clientes más valiosos**

## 🎯 Descripción del Proyecto

Este proyecto implementa un **proceso ETL completo** (Extract, Transform, Load) utilizando Pandas y SQLite para analizar datos de ventas y clientes de centros comerciales. El análisis incluye limpieza de datos, transformaciones avanzadas, análisis exploratorio y generación de insights de negocio con validación SQL.

### 🎓 Contexto Académico
- **Materia:** Programación y Base de Datos
- **Trabajo:** Exploración, Transformación y Limpieza de Datos
- **Dataset:** Sales and Customer data (Kaggle)
- **Objetivo:** Implementar proceso ETL completo para análisis de datos

---

## 🚀 Instalación y Configuración

### Prerrequisitos
- **Anaconda** instalado desde su web oficial
- **Python 3.10** o superior
- **Git** para clonar el repositorio

### 📋 Instrucciones de Instalación

#### 1. Clonar el Repositorio
```bash
git clone https://github.com/MarcosArtificialIntelligence/ABP-TS-Programacion-Y-Base-de-datos.git
cd ABP-TS-Programacion-Y-Base-de-datos-ARRUTI-ISSETTA-MRAD
```

#### 2. Crear el Entorno Conda

⚠️ **IMPORTANTE - Limpieza Previa Recomendada:**

Si ya tienes un entorno anterior o quieres una instalación completamente limpia:

```bash
# 1. Desactivar entorno actual (si está activo)
conda deactivate

# 2. Eliminar entorno anterior (si existe)
conda env remove -n ABP-2025

# 3. Cerrar terminal completamente y abrir una nueva
# (Esto limpia variables de entorno y memoria)
```

**Crear el entorno:**
```bash
# Crear el entorno desde el archivo environment.yml
conda env create -f environment.yml

# Activar el entorno
conda activate ABP-2025
```

**Verificar instalación:**
```bash
# Verificar que el entorno esté activo
conda info --envs
# Deberías ver ABP-2025 con un asterisco (*)
```

#### 3. Lanzar Jupyter Lab

```bash
# Asegúrate de estar en el directorio del proyecto
cd "ruta/a/tu/proyecto"

# Lanzar Jupyter Lab
jupyter lab
```

#### 4. Ejecutar el Análisis

1. Abrir `Analisis-de-negocio-Ventas-Clientes-Insights.ipynb`
2. **IMPORTANTE:** Ejecutar todas las celdas en orden secuencial
3. Si hay errores, reiniciar el kernel: `Kernel → Restart Kernel`
4. Los datos se procesarán automáticamente

---

## ⚠️ Consideraciones Importantes

### 🔄 **Antes de Crear el Entorno**

Si ya tienes un entorno anterior o quieres una instalación limpia:

1. **Desactivar entorno actual:**
   ```bash
   conda deactivate
   ```

2. **Eliminar entorno anterior (opcional):**
   ```bash
   conda env remove -n ABP-2025
   ```

3. **Cerrar terminal completamente:**
   - Cierra la terminal actual
   - Abre una nueva terminal
   - Esto limpia variables de entorno y memoria

4. **Verificar estado limpio:**
   ```bash
   conda info --envs
   # No debería mostrar ningún entorno con asterisco (*)
   ```

### 🚨 **Comandos Críticos**

- **NUNCA ejecutes** `conda env create` dos veces - te dará error
- **SIEMPRE activa** el entorno antes de trabajar: `conda activate ABP-2025`
- **Verifica** que estés en el directorio correcto antes de ejecutar comandos
- **Si tienes problemas**, puedes recrear el entorno completo

### 🔧 **Secuencia de Trabajo Diaria**

```bash
# 1. Abrir terminal
# 2. Navegar al proyecto
cd "ruta/a/tu/proyecto"

# 3. Activar entorno
conda activate ABP-2025

# 4. Lanzar Jupyter
jupyter lab

# 5. En Jupyter: Kernel → Restart Kernel (si hay problemas)
```

### 🐛 **Solución de Problemas Comunes**

#### Error: "Environment already exists"
```bash
# Eliminar entorno existente
conda env remove -n ABP-2025
# Crear nuevamente
conda env create -f environment.yml
```

#### Error: "Command not found: conda"
```bash
# Reinicializar conda
conda init
# Cerrar y abrir nueva terminal
```

#### Error: "Kernel died"
```bash
# En Jupyter: Kernel → Restart Kernel
# O cerrar Jupyter y reactivar entorno
conda deactivate
conda activate ABP-2025
jupyter lab
```

---

## 📂 Estructura del Proyecto

```
📁 Proyecto/
├── 📓 Analisis-de-negocio-Ventas-Clientes-Insights.ipynb  # Notebook principal
├── 📁 Dataset-Kaggle/                                     # Datos originales
│   ├── customer_data.csv                                  # 99,457 clientes
│   └── sales_data.csv                                     # 99,457 transacciones
├── 📁 datos_procesados/                                   # Datos procesados
│   ├── analisis_completo.xlsx
│   ├── clientes_procesados.csv
│   ├── datos_combinados.csv
│   └── resumen_*.csv
├── 📄 environment.yml                                     # Entorno conda
├── 📄 requirements.txt                                    # Dependencias pip
├── 📄 DIAGRAMA_BASE_DATOS.md                             # Diagrama de BD
└── 📄 ventas_clientes.db                                 # Base de datos SQLite (generado)
```

---

## 🔄 Proceso ETL Implementado

### 📥 **Extract** - Extracción de Datos
- ✅ Carga de archivos CSV desde `Dataset-Kaggle/`
- ✅ Validación de estructura y tipos de datos
- ✅ Verificación de integridad referencial
- ✅ Análisis exploratorio inicial

### 🔄 **Transform** - Transformación de Datos
- ✅ Limpieza y normalización de datos
- ✅ Categorización por edad y género
- ✅ Cálculo de métricas derivadas
- ✅ Unificación de datasets

### 📤 **Load** - Carga de Datos
- ✅ DataFrame final con datos limpios
- ✅ Validación de restricciones de integridad
- ✅ Carga a base de datos SQLite
- ✅ Consultas SQL de validación

---

## 📊 Análisis Realizados

### 🎯 Métricas Clave
- **99,457 transacciones** analizadas
- **99,457 clientes únicos**
- **Período:** 2021-2023
- **Calidad de datos:** 100% completitud

### 📈 Insights Principales
- **Género predominante:** Female (59.8% de clientes)
- **Grupo etario líder:** 51+ años (mayor valor por transacción)
- **Categoría top:** Clothing (mayor participación en ingresos)
- **Centros comerciales:** Análisis de performance por ubicación

### 📊 Visualizaciones Profesionales
El notebook incluye **dashboard ejecutivo** con visualizaciones de nivel empresarial:

#### 🎨 **Dashboard Ejecutivo Principal**
- **Heatmap demográfico** para segmentación por género y edad
- **Gráficos de barras horizontales** para top categorías por ingresos
- **Análisis de centros comerciales** segmentado por local
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

### 🔄 Ejecución Estándar
```bash
# Activar entorno
conda activate ABP-2025

# Lanzar Jupyter Lab
jupyter lab

# Abrir y ejecutar el notebook
# Analisis-de-negocio-Ventas-Clientes-Insights.ipynb
```

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
   - Segmentación demográfica por género y edad
   - Análisis de categorías de productos
   - Cálculo de métricas de negocio
   - Análisis de centros comerciales
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
├── Período: 01/01/2021 - 31/12/2022
├── Clientes únicos: 99,457
├── Transacciones: 99,457
├── Ingresos totales: $XXX,XXX,XXX.XX
└── Valor promedio: $X,XXX.XX

👥 INSIGHTS POR GÉNERO
├── Female: XX.X% de clientes
└── Male: XX.X% de clientes

👴 INSIGHTS POR EDAD
├── 18-25: XX.X%
├── 26-35: XX.X%
├── 36-50: XX.X%
└── 51+: XX.X%
```

### 🏆 Top Categorías por Ventas
1. **Clothing** - Mayor participación en ingresos
2. **Shoes** - Segunda categoría más importante
3. **Technology** - Tercera categoría relevante

---

## 🔧 Personalización

### 📝 Modificar Rutas de Datos
```python
# En la celda de carga de datos
customer_file = "ruta/a/tu/customer_data.csv"
sales_file = "ruta/a/tu/sales_data.csv"
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

## 👥 Autores

**Equipo de Desarrollo:**
- **ARRUTI Marcos Agustín** - Análisis y desarrollo
- **ISSETTA Rocío Belén** - Documentación y testing
- **ARRUTI Julián Alejandro** - Visualizaciones y diseño
- **MRAD Caro Farid Yusef** - Base de datos y SQL

**Materia:** Programación y Base de Datos  
**Institución:** ISPC - Instituto Superior Politécnico de Córdoba

---

## 📄 Licencia

Este proyecto es parte de un trabajo académico para la materia "Programación y Base de Datos" del ISPC.

---

**¡Análisis completado exitosamente!** ✅

Este análisis proporciona una base sólida para la toma de decisiones estratégicas basadas en datos, permitiendo optimizar recursos y maximizar el valor del cliente.
