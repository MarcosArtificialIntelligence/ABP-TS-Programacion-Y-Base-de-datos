# Diagrama de Base de Datos

Esta en la carpeta pero sino podes ver la captura de pantalla del Diagrama en google drive: https://drive.google.com/file/d/14zIDjKkFemKt3MNg04JGfitqj1iteXSL/view?usp=sharing


## 🗄️ o crear el Esquema en dbdiagram.io

link con el diagrama ya creado: dbdiagram: https://dbdiagram.io/d/68efc4fb2e68d21b41a1e477

O copia y pega el siguiente código en [dbdiagram.io](https://dbdiagram.io/) para visualizar el diagrama:

```sql
// ============================================================================
// DIAGRAMA DE BASE DE DATOS - ETL CON PANDAS
// Sistema de Análisis de Ventas y Clientes
// ============================================================================

// Tabla de Clientes
Table customers {
  customer_id varchar(10) [primary key, note: 'Identificador único del cliente']
  gender varchar(10) [not null, note: 'Género del cliente (Male/Female)']
  age integer [not null, note: 'Edad del cliente']
  payment_method varchar(20) [not null, note: 'Método de pago preferido']
  age_group varchar(10) [note: 'Grupo de edad categorizado']
  
  indexes {
    gender
    age_group
  }
}

// Tabla de Ventas
Table sales {
  invoice_no varchar(10) [primary key, note: 'Número de factura único']
  customer_id varchar(10) [not null, ref: > customers.customer_id, note: 'Referencia al cliente']
  category varchar(50) [not null, note: 'Categoría del producto']
  quantity integer [not null, note: 'Cantidad vendida']
  price decimal(10,2) [not null, note: 'Precio unitario']
  invoice_date date [not null, note: 'Fecha de la transacción']
  shopping_mall varchar(100) [not null, note: 'Centro comercial']
  total_amount decimal(12,2) [note: 'Monto total calculado (quantity * price)']
  year integer [note: 'Año extraído de la fecha']
  month integer [note: 'Mes extraído de la fecha']
  day integer [note: 'Día extraído de la fecha']
  weekday varchar(10) [note: 'Día de la semana']
  month_name varchar(10) [note: 'Nombre del mes']
  amount_category varchar(20) [note: 'Categoría del monto']
  
  indexes {
    customer_id
    category
    shopping_mall
    invoice_date
    (year, month)
  }
}

// Tabla de Análisis por Categoría (Vista/Tabla agregada)
Table category_analysis {
  category varchar(50) [primary key, note: 'Categoría del producto']
  total_ventas decimal(15,2) [note: 'Total de ventas en la categoría']
  promedio_venta decimal(10,2) [note: 'Venta promedio']
  num_facturas integer [note: 'Número de facturas']
  total_cantidad integer [note: 'Cantidad total vendida']
}

// Tabla de Análisis por Centro Comercial (Vista/Tabla agregada)
Table mall_analysis {
  shopping_mall varchar(100) [primary key, note: 'Centro comercial']
  total_ventas decimal(15,2) [note: 'Total de ventas en el centro']
  promedio_venta decimal(10,2) [note: 'Venta promedio']
  num_facturas integer [note: 'Número de facturas']
  total_cantidad integer [note: 'Cantidad total vendida']
}

// Tabla de Análisis Demográfico (Vista/Tabla agregada)
Table demographic_analysis {
  id integer [primary key, increment, note: 'ID único']
  gender varchar(10) [note: 'Género']
  age_group varchar(10) [note: 'Grupo de edad']
  total_ventas decimal(15,2) [note: 'Total de ventas del segmento']
  promedio_venta decimal(10,2) [note: 'Venta promedio']
  num_facturas integer [note: 'Número de facturas']
  total_cantidad integer [note: 'Cantidad total vendida']
  
  indexes {
    (gender, age_group)
  }
}

// Tabla de Datos Combinados (Vista desnormalizada)
Table merged_sales_customers {
  invoice_no varchar(10) [primary key, note: 'Número de factura']
  customer_id varchar(10) [not null, note: 'ID del cliente']
  category varchar(50) [note: 'Categoría del producto']
  quantity integer [note: 'Cantidad']
  price decimal(10,2) [note: 'Precio unitario']
  invoice_date date [note: 'Fecha de transacción']
  shopping_mall varchar(100) [note: 'Centro comercial']
  total_amount decimal(12,2) [note: 'Monto total']
  year integer [note: 'Año']
  month integer [note: 'Mes']
  gender varchar(10) [note: 'Género del cliente']
  age integer [note: 'Edad del cliente']
  payment_method varchar(20) [note: 'Método de pago']
  age_group varchar(10) [note: 'Grupo de edad']
  
  indexes {
    customer_id
    (category, gender)
    invoice_date
  }
}

// Relaciones
// Ref: sales.customer_id > customers.customer_id [note: 'Un cliente puede tener múltiples ventas']
```

## 📊 Descripción de las Tablas

### 1. **customers** (Clientes)
Tabla principal que almacena la información demográfica de los clientes.

**Campos:**
- `customer_id`: Identificador único del cliente
- `gender`: Género (Male/Female)
- `age`: Edad del cliente
- `payment_method`: Método de pago preferido (Credit Card, Debit Card, Cash)
- `age_group`: Categorización por edad (18-25, 26-35, 36-50, 51-65, 65+)

**Cardinalidad:** ~99,440 registros

---

### 2. **sales** (Ventas)
Tabla principal que almacena todas las transacciones de ventas.

**Campos:**
- `invoice_no`: Número de factura único
- `customer_id`: Referencia al cliente (FK)
- `category`: Categoría del producto (Clothing, Shoes, Books, etc.)
- `quantity`: Cantidad vendida
- `price`: Precio unitario
- `invoice_date`: Fecha de la transacción
- `shopping_mall`: Centro comercial donde se realizó la venta
- `total_amount`: Monto total (calculado)
- Campos derivados de fecha: year, month, day, weekday, month_name
- `amount_category`: Categorización del monto (Muy Bajo, Bajo, Medio, Alto, Muy Alto)

**Cardinalidad:** ~99,440 registros
**Relación:** 1 cliente → N ventas

---

### 3. **category_analysis** (Análisis por Categoría)
Vista agregada con métricas por categoría de producto.

**Métricas:**
- Total de ventas
- Venta promedio
- Número de facturas
- Cantidad total vendida

**Cardinalidad:** ~8 categorías

---

### 4. **mall_analysis** (Análisis por Centro Comercial)
Vista agregada con métricas por centro comercial.

**Métricas:**
- Total de ventas
- Venta promedio
- Número de facturas
- Cantidad total vendida

**Cardinalidad:** ~10 centros comerciales

---

### 5. **demographic_analysis** (Análisis Demográfico)
Vista agregada con métricas por segmento demográfico (género y edad).

**Dimensiones:**
- Género (Male/Female)
- Grupo de edad (5 grupos)

**Métricas:**
- Total de ventas
- Venta promedio
- Número de facturas
- Cantidad total vendida

**Cardinalidad:** 10 segmentos (2 géneros × 5 grupos de edad)

---

### 6. **merged_sales_customers** (Datos Combinados)
Vista desnormalizada que combina información de ventas y clientes para análisis.

**Uso:** Análisis multidimensional, reportes ejecutivos, dashboards

**Cardinalidad:** ~99,440 registros

---

## 🔑 Relaciones Clave

### Relación Principal
```
customers (1) ←→ (N) sales
```

- **Tipo:** One-to-Many (1:N)
- **Clave foránea:** `sales.customer_id` → `customers.customer_id`
- **Integridad:** Cada venta debe tener un cliente válido

### Índices Importantes
1. **customers.customer_id**: Búsqueda rápida de clientes
2. **sales.invoice_no**: Búsqueda de facturas
3. **sales.customer_id**: Join eficiente con customers
4. **sales.(year, month)**: Análisis temporal
5. **sales.category**: Análisis por categoría
6. **merged_sales_customers.(category, gender)**: Análisis cruzado

---

## 📈 Normalización

### Forma Normal: 3NF (Tercera Forma Normal)

**Tabla customers:**
- ✅ 1NF: Todos los atributos son atómicos
- ✅ 2NF: No hay dependencias parciales
- ✅ 3NF: No hay dependencias transitivas

**Tabla sales:**
- ✅ 1NF: Todos los atributos son atómicos
- ✅ 2NF: No hay dependencias parciales
- ⚠️ 3NF: Campos derivados (year, month, etc.) por diseño para optimización

**Vistas agregadas:**
- Desnormalizadas intencionalmente para consultas analíticas rápidas

---

## 💾 Consideraciones de Diseño

### Ventajas del Diseño:
1. **Separación de datos transaccionales y maestros**
2. **Vistas agregadas para consultas rápidas**
3. **Índices estratégicos para análisis**
4. **Campos derivados para optimización**

### Escalabilidad:
- **Particionamiento por fecha**: Posible en sales por year/month
- **Archivado**: Datos antiguos pueden moverse a tablas históricas
- **Caching**: Vistas agregadas pueden cachearse

---

## 🔍 Consultas SQL Típicas

### Consulta 1: Ventas por Cliente
```sql
SELECT 
    c.customer_id,
    c.gender,
    c.age_group,
    COUNT(s.invoice_no) as num_compras,
    SUM(s.total_amount) as total_gastado
FROM customers c
LEFT JOIN sales s ON c.customer_id = s.customer_id
GROUP BY c.customer_id, c.gender, c.age_group;
```

### Consulta 2: Top Categorías por Género
```sql
SELECT 
    c.gender,
    s.category,
    SUM(s.total_amount) as total_ventas
FROM sales s
JOIN customers c ON s.customer_id = c.customer_id
GROUP BY c.gender, s.category
ORDER BY c.gender, total_ventas DESC;
```

### Consulta 3: Ventas Mensuales
```sql
SELECT 
    year,
    month,
    month_name,
    SUM(total_amount) as ventas_mes,
    COUNT(invoice_no) as num_facturas
FROM sales
GROUP BY year, month, month_name
ORDER BY year, month;
```

---

**Nota:** Este diagrama representa la estructura de datos del proceso ETL implementado con Pandas. Las "tablas" son DataFrames que pueden exportarse a bases de datos SQL si se requiere.
