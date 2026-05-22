## 👥 Integrantes:
* **Teo Maita**
* **Melanie Buenaño**

# Talller-Creaci-n-y-visualizaci-n-de-KPIs
Taller hecho en clase: Sistema de Información Gerencial (MIS) desarrollado en Python para la consolidación, análisis y visualización de KPIs estratégicos a partir de datos transaccionales (TPS).
# 📊 Management Information System (MIS) - Visualización de KPIs

## 🏫 Información del Proyecto
* **Institución:** Escuela Politécnica Nacional (EPN)
* **Asignatura:** Sistemas de Información Gerenciales
* **Autor:** Teo Maita
* **Entorno de Desarrollo:** Google Colab / Python

---

## 🚀 Descripción del Sistema
Este repositorio contiene la implementación de la capa del **Sistema de Información Gerencial (MIS)**. El objetivo fundamental de este módulo es consumir los datos atómicos e históricos generados en tiempo real por el sistema transaccional (**TPS**), unificarlos en un repositorio común y procesar cálculos matemáticos y estadísticos para transformarlos en indicadores clave de rendimiento (**KPIs**). 

Esta solución automatiza la extracción de datos dispersos para transformarlos en conocimiento táctico y estratégico, apoyando la toma de decisiones medibles por parte de los mandos medios y gerenciales.

---

## 🛠️ Arquitectura de Datos y Repositorio
Siguiendo las directrices arquitectónicas del taller, este sistema mantiene un **repositorio desacoplado e independiente** del código fuente del TPS, simulando un entorno empresarial real donde el módulo analítico consume las fuentes de datos de forma relacional.

### Fuentes de Datos Transaccionales Consumidas:
* `facturas.csv`: Registro atómico de transacciones que almacena campos como `Cedula`, `Cliente` y el monto `Total` devengado por transacción.
* `productos.csv`: Catálogo maestro de inventario que registra los atributos físicos de los productos, categorías, precios y existencias en tiempo real (`stock`).

---

## 📉 KPIs Implementados

El cuadro de mando ejecuta el procesamiento y renderizado de tres indicadores de alto impacto:

1.  **KPI 1: Ventas Totales Generales (Rendimiento Financiero)**
    * *Métrica:* Consolidación macro del flujo de caja bruto mediante una agregación escalar lineal (`.sum()`).
    * *Visualización:* Tarjeta indicadora discreta (*KPI Card*) minimalista para mitigar ruido analítico.
2.  **KPI 2: Top 10 Productos con Mayor Stock (Control de Disponibilidad)**
    * *Métrica:* Ordenamiento descendente por QuickSort y truncamiento para identificar densidad de almacenamiento físico.
    * *Visualización:* Diagrama de barras horizontales con *data labeling* dinámico en las puntas.
3.  **KPI 3: Top 10 Clientes Estratégicos (Segmentación por Volumen de Compra)**
    * *Métrica:* Agregación multidimensional por clave compuesta (`Cedula` + `Cliente`) para anular colisiones por homónimos.
    * *Visualización:* Gráfico de barras corporativo con inyección de máscaras financieras de precisión flotante (`$X,XXX.XX`).

---

## 🧪 Tecnologías y Sanitización de Datos (Principio GIGO)
El proyecto está construido sobre el ecosistema científico de Python, utilizando librerías estándar en la ingeniería de datos:
* **Pandas:** Para el parsing, filtrado, uniones matriciales (`joins`) y agrupaciones (`groupby`).
* **Matplotlib & Seaborn:** Para la programación de la capa gráfica y estilización ejecutiva.

Para inmunizar los reportes contra el principio **GIGO** (*Garbage In, Garbage Out*), el pipeline de código inyecta rutinas de limpieza vectorial:
* `str.strip()`: Elmina espacios en blanco huérfanos que provocan fallos de indexación.
* `str.lower()`: Normaliza metadatos de columnas contra inconsistencias de tipografía humana.
* `astype(str)`: Ejecuta un casting explícito en variables de identidad para prevenir distorsiones continuas en los ejes cartesianos.

---

## 💻 Cómo Ejecutar el Cuaderno
1.  Asegúrate de que los archivos `facturas.csv` y `productos.csv` estén presentes en el directorio raíz o cargados en el entorno de almacenamiento local.
2.  Abre el archivo `.ipynb` provisto en este repositorio.
3.  Ejecuta las celdas en orden secuencial presionando `Shift + Enter` para inicializar el entorno gráfico y desplegar el Dashboard analítico.
