# Análisis de Mortalidad en Colombia 2019

## Descripción del Proyecto

Esta aplicación web dinámica analiza los datos de mortalidad en Colombia para el año 2019, utilizando herramientas avanzadas de visualización interactiva con Plotly y Dash en Python. La aplicación permite explorar patrones demográficos y regionales a través de diversos gráficos interactivos.

## Objetivo

Proporcionar una herramienta accesible para identificar patrones, tendencias y correlaciones clave en los datos de mortalidad de Colombia, facilitando el análisis visual intuitivo de la información.

## Estructura del Proyecto

```
├── app.py                 # Archivo principal de la aplicación Dash
├── requirements.txt       # Dependencias del proyecto
├── README.md             # Documentación del proyecto
├── Anexos/               # Datos fuente
│   ├── Anexo1.NoFetal2019_CE_15-03-23.xlsx    # Datos de mortalidad
│   ├── Anexo2.CodigosDeMuerte_CE_15-03-23.xlsx # Códigos de causas
│   └── Divipola_CE_.xlsx                      # División político-administrativa
├── css/                  # Archivos de estilo (no utilizados en esta versión)
├── js/                   # Archivos JavaScript (no utilizados en esta versión)
├── data/                 # Datos procesados (JSON)
└── screenshots/          # Capturas de pantalla de las visualizaciones
```

## Requisitos

- Python 3.8+
- Librerías especificadas en `requirements.txt`:
  - dash==3.2.0
  - plotly==6.4.0
  - pandas==2.3.3
  - openpyxl==3.1.5
  - numpy==2.2.6
  - gunicorn

## Instalación

1. Clona el repositorio:
   ```bash
   git clone <url-del-repositorio>
   cd Act04_web-analisis-mortalidad-colombia
   ```

2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

3. Ejecuta la aplicación localmente:
   ```bash
   python app.py
   ```

4. Abre tu navegador en `http://localhost:8050`

## Despliegue

### Opción 1: Render (Recomendado - GRATIS)
1. Crea una cuenta gratuita en [render.com](https://render.com)
2. Sube este repositorio a GitHub
3. Conecta tu repositorio a Render
4. Render detectará automáticamente la configuración desde `render.yaml`
5. La aplicación estará disponible en una URL gratuita

### Opción 2: Otros servicios gratuitos
- **Heroku**: 550 horas gratis/mes
- **Railway**: 512MB RAM gratis
- **PythonAnywhere**: Especializado en Python

### Opción 3: cPanel (Requiere soporte Python)
1. Acceder al panel de control CPANEL
2. Crear una carpeta el proyecto `mortalidad-colombia`
3. Subir los archivos del proyecto incluyendo `Anexos/` con los datos Excel
4. Configura el servidor web para ejecutar aplicaciones Python (WSGI/CGI)
5. Instala las dependencias requeridas en el servidor
6. Configura el archivo de inicio de la aplicación

## Visualizaciones

La aplicación incluye las siguientes visualizaciones interactivas con explicaciones de resultados:

1. **Mapa de Departamentos**: Visualización de la distribución total de muertes por departamento en Colombia para el año 2019. Permite identificar las regiones con mayor concentración de mortalidad.

2. **Gráfico de Líneas**: Representación del total de muertes por mes en Colombia, mostrando variaciones a lo largo del año. Ayuda a identificar patrones estacionales en la mortalidad.

3. **Gráfico de Barras - Ciudades Violentas**: Visualización de las 5 ciudades más violentas de Colombia, considerando homicidios (códigos X95, agresión con disparo de armas de fuego y casos no especificados). Destaca las áreas con mayor índice de violencia.

4. **Gráfico Circular**: Muestra las 10 ciudades con menor índice de mortalidad, proporcionando una perspectiva de las zonas más seguras en términos de mortalidad general.

5. **Tabla de Causas**: Listado de las 10 principales causas de muerte en Colombia, incluyendo su código, nombre y total de casos (ordenadas de mayor a menor). Facilita la identificación de las enfermedades y condiciones más letales.

6. **Gráfico de Barras Apiladas**: Comparación del total de muertes por sexo en cada departamento, para analizar diferencias significativas entre géneros y distribución regional.

7. **Histograma**: Distribución de muertes agrupando los valores de la variable GRUPO_EDAD1 según los rangos definidos en la tabla de referencia para identificar patrones de mortalidad a lo largo del ciclo de vida.

## Software Utilizado

- **Python**: Lenguaje de programación principal
- **Dash**: Framework para aplicaciones web
- **Plotly**: Librería de visualización interactiva
- **Pandas**: Manipulación y análisis de datos
- **OpenPyXL**: Lectura de archivos Excel

## Datos

Los datos utilizados provienen del DANE (Departamento Administrativo Nacional de Estadística) - Estadísticas Vitales 2019:

- **NoFetal2019.xlsx**: Datos de mortalidad no fetal
- **CodigosDeMuerte.xlsx**: Clasificación internacional de enfermedades
- **Divipola.xlsx**: División político-administrativa de Colombia

## Resultados y Hallazgos

### Capturas de Pantalla

#### 1. Mapa de Departamentos
![Mapa Departamentos](screenshots/mapa_departamentos.png)
*El mapa muestra la distribución geográfica de muertes por departamento, destacando las regiones con mayor concentración de mortalidad.*

#### 2. Gráfico de Líneas - Muertes por Mes
![Muertes por Mes](screenshots/muertes_mensuales.png)
*Este gráfico revela variaciones estacionales en la mortalidad, con posibles incrementos durante ciertos periodos del año.*

#### 3. Ciudades Más Violentas
![Ciudades Violentas](screenshots/ciudades_violentas.png)
*Las 5 ciudades con mayor número de homicidios, indicando áreas críticas en términos de violencia urbana.*

#### 4. Ciudades con Menor Mortalidad
![Menor Mortalidad](screenshots/ciudades_seguras.png)
*Representación de las zonas más seguras, útil para análisis comparativos de índices de mortalidad.*

#### 5. Tabla de Principales Causas
![Tabla Causas](screenshots/tabla_causas.png)
*Clasificación de las enfermedades y condiciones más letales en Colombia durante 2019.*

### Estadísticas Generales
- **Total de registros analizados**: 244,355 muertes en 2019
- **Departamentos con mayor mortalidad**: Cundinamarca, Antioquia, Valle del Cauca
- **Principales causas**: Enfermedades cardiovasculares, cáncer, accidentes
- **Distribución por género**: Análisis de diferencias entre hombres y mujeres
- **Grupos etarios más afectados**: Adultos mayores (60+ años) y población infantil

## Contribuidores

Mónica Contreras

## Licencia

Este proyecto es parte de la Maestría en Inteligencia Artificial - Aplicaciones I.