# Proyecto 6 - Análisis de una empresa de telecomunicaciones

## 📌 Objetivo del proyecto

El objetivo de este proyecto es analizar cómo los clientes de **ConnectaTel**, empresa de telecomunicaciones con operaciones en México y Colombia, utilizan los servicios móviles de llamadas y mensajes.

El análisis busca identificar **patrones de uso, comportamientos atípicos y segmentos de clientes con necesidades diferenciadas**, con el fin de generar conclusiones accionables que permitan optimizar la oferta comercial y mejorar la experiencia del usuario.

---

## 📂 Datasets utilizados

El proyecto utiliza tres fuentes de datos:

1. **`plans.csv`**  
   Contiene información sobre los planes actuales, incluyendo precio, minutos incluidos, GB y costos adicionales.

2. **`users_latam.csv`**  
   Contiene información de los clientes, como edad, ciudad, fecha de registro, plan contratado y fecha de cancelación.

3. **`usage.csv`**  
   Contiene información sobre el uso real de los servicios, incluyendo llamadas, duración y mensajes.

Los datasets se relacionan mediante la información del usuario y permiten analizar el comportamiento de consumo según características demográficas y plan contratado.

---

## 🔄 Etapas del análisis

El proyecto se desarrolló siguiendo las siguientes etapas:

### 1. Carga y exploración de los datos
- Carga de los tres datasets.
- Revisión de dimensiones, columnas y tipos de datos.
- Exploración inicial de las variables.

### 2. Análisis de calidad de datos
- Identificación de valores faltantes.
- Detección de valores inválidos o sentinels.
- Revisión de fechas y valores fuera de rango.
- Identificación de columnas que no aportan valor analítico, como `id` y `user_id`.

### 3. Limpieza y preparación
- Tratamiento de valores faltantes según el significado de cada variable.
- Identificación de valores inválidos como `-999` en `age`.
- Estandarización de valores inconsistentes en variables categóricas.
- Conversión y preparación de fechas para el análisis.

### 4. Análisis estadístico
- Cálculo de medidas descriptivas.
- Análisis de edad, llamadas, mensajes y duración de llamadas.
- Comparación de comportamiento entre planes.

### 5. Visualización y análisis de outliers
- Histogramas y boxplots para identificar distribuciones y valores extremos.
- Análisis de outliers en mensajes, llamadas y minutos por llamada.
- Los valores extremos se conservaron cuando podían representar comportamientos reales de usuarios.

### 6. Segmentación de clientes
Se crearon segmentos considerando:
- **Edad:** Joven, Adulto y Adulto Mayor.
- **Nivel de uso:** Bajo uso, Uso medio y Alto uso.
- **Plan contratado:** Básico y Premium.

### 7. Análisis ejecutivo
Finalmente, se tradujeron los resultados en:
- Patrones de comportamiento.
- Segmentos de mayor interés comercial.
- Oportunidades de upselling y retención.
- Recomendaciones para mejorar o complementar la oferta de planes.

---

## 💻 Herramientas utilizadas

- Python
- Jupyter Notebook
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## ▶️ Cómo ejecutar el notebook

El proyecto puede ejecutarse utilizando **Google Colab** o Jupyter Notebook.

### Opción 1: Google Colab

1. Abrir el archivo `.ipynb` en Google Colab.
2. Subir los archivos `plans.csv`, `users_latam.csv` y `usage.csv`, o utilizar las rutas definidas en el notebook.
3. Ejecutar las celdas en orden, desde la carga de librerías hasta las conclusiones.
4. Verificar que los datasets estén disponibles en la ruta indicada por el notebook.

### Opción 2: Jupyter Notebook

Instalar las librerías necesarias:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Luego ejecutar:

```bash
jupyter notebook
```

Abrir el notebook del proyecto y ejecutar las celdas en orden.

---

## 🔁 Guía breve de reproducción

Para reproducir el análisis:

1. Descargar los tres datasets.
2. Colocarlos en la carpeta utilizada por el notebook.
3. Abrir el notebook `Proyecto_6_Analisis_ConnectaTel.ipynb`.
4. Ejecutar las celdas en orden.
5. Revisar las etapas de exploración, limpieza, análisis estadístico, visualización y segmentación.
6. Consultar la sección de análisis ejecutivo para las conclusiones y recomendaciones comerciales.

### Fuentes de datos

- `plans.csv`: https://drive.google.com/uc?export=download&id=17Mkcs9rRWwiC_gaqVBYuFieON7s9v7Bn
- `users_latam.csv`: https://drive.google.com/uc?export=download&id=17wuqxalUsUnw9PXvCN2_UaAz6xeS9B0T
- `usage.csv`: https://drive.google.com/uc?export=download&id=11T8MQf-ouxJu9tia4F8aNpY7M_fb9O4h

---

## 📊 Resultado esperado

El análisis permite obtener una visión general del comportamiento de los clientes de ConnectaTel, identificar diferencias entre segmentos de edad, nivel de uso y plan contratado, detectar comportamientos extremos y generar recomendaciones comerciales basadas en los patrones encontrados.
