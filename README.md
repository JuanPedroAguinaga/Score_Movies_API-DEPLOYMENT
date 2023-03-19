<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº1** </h1>

# Score Movies

## Enfoque del Proyecto

El proyecto se enfoca en el rol de MLOps Enginner, donde se pide el desarrollo de una API utilizando el framework FastApi
para comunicar y disponibilizar datos para el equipo de análisis de datos de una empresa. 
El objetivo principal es realizar transformaciones 
específicas en los datos y disponibilizarlos a través de endpoints accesibles mediante la API que finalmente debe ser desplegada en Render.
Una vez terminado el proceso y echo el deployment, realizamos un proceso de análisis exploratorio de los datos para luego, poder entrenar un modelo de machine
learning para armar un sistema de recomendacion de peliculas para usuarios.

[Ver mas sobre el proyecto y sus requerimientos](https://github.com/HX-PRomero/PI_ML_OPS/blob/main/Readme.md)

## Objetivos

Se lograron cumplir la gran mayoria de los objetivos propuestos, de forma especifica estos son ellos:

- [x] Tranformaciones en las bases de datos: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_API-DEPLOYMENT/blob/master/tranformation.ipynb)

- [x] Desarrollo de la API

- [x] Deployment: [Link](https://score-movies-prueba8.onrender.com/docs)

- [x] Video: [Link]()

- [x] Exploraty Data Analysis-EDA: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_EDA_SistemaDeRecomendacion/blob/main/EDA.ipynb)

- [x] Sistema de recomendación: [Link](https://github.com/JuanPedroAguinaga/Score_Movies_EDA_SistemaDeRecomendacion/blob/main/SistemaDeRecomendacion.ipynb)

- [ ] Deployment: 

- [x] Video: [Link]


## Requerimientos

1. Generar campo id: Cada id se compondrá de la primera letra del nombre de la plataforma, seguido del show_id ya presente en los datasets (ejemplo para títulos de Amazon = as123)
2. Los valores nulos del campo rating deberán reemplazarse por el string “G” (corresponde al maturity rating: “general for all audiences”
3. De haber fechas, deberán tener el formato AAAA-mm-dd
4. Los campos de texto deberán estar en minúsculas, sin excepciones
5. El campo duration debe convertirse en dos campos: duration_int y duration_type. El primero será un integer y el segundo un string indicando la unidad de medición de duración: min (minutos) o season (temporadas)

## Endpoints de la API

La API cuenta con los siguientes endpoints:

* Cantidad de veces que aparece una keyword en el título de peliculas/series, por plataforma.
  
* Cantidad de películas por plataforma con un puntaje mayor a XX en determinado año.
  
* La segunda película con mayor score para una plataforma determinada, según el orden alfabético de los títulos.
  
* Película que más duró según año, plataforma y tipo de duración
  
* Cantidad de series y películas por rating


## Deployment

Para realizar el deploy se utilizo [Render](https://render.com/)

Intrucciones: 

- Clonar el repositorio con (git clone https://github.com/JuanPedroAguinaga/Score_Movies_API-DEPLOYMENT)
- Acceder a la carpeta mediante linea de comandos (cd/ruta/hasta/el/proyecto/Score_Movies_API-DEPLOYMENT) una vez clonada o descargada
- Crear un ambiente virtual en la carpeta principal usando en comando (python -m venv venv --upgrade-deps) para que gestione un entorno de ambiente con las dependencias
- Activar el ambiente virtual creado con (source venv/Scripts/activate) o (./venv/Scripts/activate)
- Instalar las dependencias del proyecto mediante la ejecución de (pip install -r requirements.txt)
- Ejecutar el proyecto mediante el comando (uvicorn main:app --reload) asegurandose que tenemos instalado uvicorn mediante el comando pip install uvicorn
 para poder probar el proyecto en local accediendo al navegador en (localhots:8000)


