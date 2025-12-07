# Generación y Análisis de Hostnames para Infraestructura Tecnológica

Este proyecto implementa un sistema completo para la **generación, clasificación y análisis de hostnames** utilizados en entornos corporativos de infraestructura IT.  
Incluye la creación de un conjunto sintético de hosts, su categorización automática y la generación de visualizaciones que permiten entender la distribución de plataformas, entornos y países dentro de un ecosistema tecnológico.

El objetivo es demostrar un flujo profesional de automatización, análisis de datos y visualización utilizando Python y bibliotecas estándar como **Pandas** y **Matplotlib**.

---

## Objetivos del proyecto

El sistema desarrollado permite:

- Generar nombres de host siguiendo reglas reales utilizadas en compañías tecnológicas.
- Codificar dentro del hostname atributos como:
  - Sistema operativo  
  - Entorno de uso (Producción, Staging, Testing…)  
  - País o región  
  - Número de nodo dentro de un clúster  
- Construir un **dataset estructurado** a partir de los hostnames generados.
- Realizar análisis estadístico y gráfico sobre:
  - Distribución de sistemas operativos  
  - Distribución por país  
  - Distribución por entorno  
  - Relación entre países y entornos  
- Exportar los datos generados en formato **CSV** para integraciones posteriores.

---

## Componentes principales

### 🔹 1. Generación de hostnames  
El proyecto implementa un generador que construye hostnames siguiendo una estructura codificada:

Con probabilidades definidas para asegurar distribuciones realistas en:

- **Sistema operativo**  
- **Entorno**  
- **País o región**  
- **Número de nodo** incremental por combinación

### 🔹 2. Clasificación automática  
Se implementan funciones que interpretan un hostname y extraen:

- Tipo de sistema operativo  
- Entorno correspondiente  
- País asociado  
- Número de nodo  

Esto permite transformar un string complejo en información estructurada.

### 🔹 3. Creación del DataFrame  
El proyecto construye un **DataFrame profesional** que consolida toda la información extraída de los hostnames, dejando los datos listos para análisis.

### 🔹 4. Exportación de datos  
El dataset completo se exporta en formato:


peritiendo su uso en procesos ETL, auditorías, dashboards o análisis posteriores.

---

## 📊 Visualizaciones generadas

El proyecto incluye varias visualizaciones profesionales:

### ✔ Distribución de hostnames según entorno y país  
Gráfico de barras comparativo generado mediante `unstack()`.

### ✔ Figura analítica 2x2 con cuatro subgráficos
Incluye:

1. **Distribución del sistema operativo por país**  
   - Barras horizontales  
   - Agrupación por OS y país  

2. **Total de sistemas operativos**  
   - Gráfico de tarta  
   - Etiquetas con valores  
   - Porcentajes en leyenda  

3. **Total de hostnames por país**  
   - Barras horizontales  
   - Anotaciones con cantidades  
   - Ajuste dinámico del eje X  

4. **Hostnames por país y entorno**  
   - Gráfico de barras agrupadas  

Todas las visualizaciones siguen buenas prácticas de claridad, etiquetado y estilo.

---

## 🛠️ Tecnologías utilizadas

- **Python 3**  
- **Pandas** – Manipulación de datos  
- **NumPy** – Gestión numérica  
- **Matplotlib** – Visualización  
- **Random / String** – Generación de secuencias  

---

##  Estructura del repositorio
hostname-analysis/
│
├── notebooks/
│ └── hostname_generation.ipynb # Notebook principal del proyecto
│
├── data/
│ └── hosts.csv # Dataset generado (opcional)
│
├── README.md # Documentación del proyecto
└── requirements.txt # Dependencias (opcional)

---

## ▶️ Ejecución del proyecto

1. Clonar el repositorio:

```bash
git clone https://github.com/<usuario>/<repositorio>.git
cd <repositorio>
pip install -r requirements.txt

jupyter notebook notebooks/hostname_generation.ipynb




