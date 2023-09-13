# PIHenry2-Vialidad

![wink](https://github.com/ReneSebastianJoo/PIHenry2-Vialidad/blob/main/DataAnaliticsGiphy.gif)

## Índice 
<!-- TABLA DE CONTENIDO -->
<details>
  <summary>Tabla de contenido</summary>
  <ol>  
    <li><a href="#ETL">ETL</a></li>
    <li><a href="#Introducción">Introducción</a></li>
    <li><a href="#Objetivo">Objetivo</a></li>
    <li><a href="#Conjunto de Tecnologías">Conjunto de Tecnologías</a></li>
    <li><a href="#EDA">EDA</a></li>
    <li><a href="#KPIs">KPIs</a></li>
    <li><a href="#EL PRIMER KPI">KPI 1</a></li>
    <li><a href="#EL SEGUNDO KPI">KPI 2</a></li>
    <li><a href="#EL TERCER KPI">KPI 3</a></li>
    <li><a href="#Dashboard">Dashboard</a></li>
    <li><a href="#Conclusiones">Conclusiones</a></li>
  </ol>
</details>

## Introducción
En este proyecto se hizo un analisis sobre las victimas mortales en accidentes viales en la Ciudad Autonoma de Buenos Aires (CABA), por medio de un dataset oficial del govierno de Argentina en donde se encuentra toda la información. En los datos hay información acerca de los siniestros viales que ocurrieron en el lapso comprendido entre los años 2016 y 2021, además de información útil para llevar a cabo el análisis sin poner en peligro la identidad de los involucrados.

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados, esto último es en lo que nos fijaremos.

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Esta sigue siendo la principal causa de muertes violentas en el país. Los informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito. Ademáslos expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.

En el contexto de una ciudad como Buenos Aires, los siniestros viales son una preocupación importante debido al alto volumen de tráfico y la densidad poblacional. Por lo que es importante su análisis.

El análisis se llevo acabo en python utilizando varias librerias como pandas, mathplotlib, seaborn entre otras.

Para el proceso primero se realizo un ETL en el que se observo que la mayoria de los datos estaban limpios, luego se hizo un Analisis exploratorio de datos del cual se extrajeron varias concluisones. Despues de analizar se contrasto con algunos KPIs. Finalmente toda la informacíon obtenida se llevo a un dashboard.

Se obtuvieron varias conclusiones pero entre las más destacadas son que las motos son el vehiculo más peligroso, la comuna 1 es la más letal y la calle más peligrosa es la avenida General Paz.

## Objetivo

1. Analizar detalladamente los datasets para entender problematica de manera correcta, para poder obtener información valiosa.
2. Crear un dashboard para la presentación de la información obtenida del analisis y que ayude a transmitir de forma efectiva.

## Conjunto de Tecnologías

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![PowerBI]( https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![Geopandas](geopandas_logo.png)


## ETL 

Se realizo el proceso de ETL (Carga, Limpiza y Transformación) de los datos. en el que se encontro que el conjunto de datos se encontraba casi listo para trabajar, con pocos datos nulos o faltantes y ningún registro duplicado. Se hicieron algunas tablas para facilitar los analisis como la segmentación por semestres por ejemplo, asi como la eliminación de la columna "Altura" que no aportaba mucha información.

## EDA

Despues del proceso de ETL se realizo el EDA el cual empezo con un analisis temporal para observar las variaciones de victimas entre cada año, encontrandose un total de 714 victimas entre los años 2016 a 2021.

Despues se hizo un analisis geografico con ayuda de geopandas, en donde se exploraron los siniestros viales por cada una de las 15 comunas de CABA. En este análisis se encontro la calle más peligrosa y el efecto que tienen los cruces en la cantidad de homicidios en siniestros viales. Se encontro que la comuna 1 era la más letal y se busco su tamaño el cual no era tan grande por lo cual se ve que esta comuna realmente es peligrosa.
Además se encontro que el tipo de calle más peligroso son las avenidas.

Despues se hizo un analisis sobre el tipo de victima, donde se encontro que la mayoria son hombres, ademas que cerca de la mitad de los fallecidos fueron en moto seguidos por los peatones y entre ambos son los más propensos a morir en un accidente vial.

Se decidio refinar el analisis cronologico utilizando las edades de las victimas y la diferencia de fechas entre el suceso y su muerte, donde se determino que la mayoria de las victimas eran adultos jovenes de 20-39 años, de estos la mayoria de las muertes inmediatas fue en accidentes en moto, donde más se tardaban en morir era en accidentes de auto y algunos peatones.

Se busco a la mayoria de los acusados y los mayoritarios fueron automoviles, vehiculos de pasajeros y vehiculos de cargas.

Despues de finalizado este analisis se prosiguío a la comparación con diferentes KPIs.

*El desarrollo de este proceso se puede ver aquí:* [EDA Link](https://github.com/ReneSebastianJoo/PIHenry2-Vialidad/blob/main/EDA.ipynb)

## KPIs

Para este trabajo se solicitaron 3 KPIs (Indicadores clave de proceso), de los cuales 2 fueron entrengados y el tercero se planteo con la información adquirida en este trabajo. A continuación se enlistan los KPIs utilizados.

1 Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.

2 Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.

3 Reducir en un 15% la cantidad de homicidios en siniestros viales en la Comuna 1, en CABA, respecto al año anterior.

Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Estas tasas se calculan, generalmente, como el número de muertes por cada cierto número de habitantes o por cada cierta cantidad de vehículos registrados. Reducir estas tasas es un objetivo clave para mejorar la seguridad vial y proteger la vida de las personas en la ciudad. Esta información es la que se utilizó para los KPIs.

## EL PRIMER KPI

La tasa de homicidios en siniestros viales es el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000.

Se encontro segun el Censo más reciente la población es de 3.317.463 habitantes.

Este primer KPI nos indica principalmente como varia la cantidad de victimas cada semestre lo que nos da idea si las medidas tomadas estan siendo de utilidad y la tendencia que se tiene.

De los 12 semestres que se tienen datos se puede ver que en solo 5 se logro el KPI. Se puede ver que del 2016 al 2018 hay poco cambio, siendo el primer semestre del 2020 el cual hubo una mayor disminución de siniestros aunque esto es atribuible a la pandemia por COVID más que porque hayan mejorado las condiciones viales.

## EL SEGUNDO KPI: 

La cantidad de accidentes mortales de motociclistas en siniestros viales se define como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100.

Se puede observar que los primeros años desde que se tienen mediciones (2016-2019) el valor no ha variado mucho, el porque el no se ve tanta variación en 2019 puede deberse que aunque estaba la pandemia por COVID muchos viajaban en motocicleta como servicios de delivery. Despues el 2020 donde se llevo un confinamiento más estricto se ve una gran disminución de eventos. Lo preocupante de la medición de este KPI es que se puede ver que tiene una tendencia a la alza los últimos años por lo que se deben tomar medidas para empezar a disminuir el numero de estos incidentes.

## EL TERCER KPI: 

La tasa de homicidios en siniestros viales es el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000.

Se encontro segun el Censo más reciente la población de la comuna 1 es de 205,886 habitantes.

Se puede ver claramente que el KPI se cumplio solamente en 2019 y 2020 los años en los que estuvo la pandemia por COVID, siendo el 2019 el año donde se alcanzo una menor cifra de homicidios en siniestros viales. En estos años se llego a un cambio de -40% de la tasa de homicidios en siniestros viales lo cual es muy bueno.

Lo preocupante de este KPI es que nos indica que tiene una tendencia a la alta y en un futuro cercano puede llegar a volver a los números previos a la pandemia.

## Dashboard 

Se genero un dashboard en power BI para poder reumir la información obtenida de forma visual y así poder explicar de forma más facil lo que se llego a conocer de este proyecto.

En el dashboard vienen integrados elementos visules interactivos por lo que se pueden apreciar los cambios cuando se da click en cada uno de los elementos.

## Conclusiones

La totalidad de concluisones se encuentran en el archivo del EDA pero las 5 más importantes son las siguientes.

La gran mayoria de las victimas son hombres.

LA comuna más letal es la comuna 1 lo cual es extraño ya que esta no es la más grande ni la más poblada segun datos oficiales.

La gran mayoria de las muertes ocurren en accidentes relacionados con motocicletas, por lo que se puede ver que es el medio de transporte más inseguro.

La gran mayoria de las victimas tienen entre 20 a 39,  por lo que no se descarta que la condución imprudente sea una de las causas más probables de muerte en los siniestros viales.

Se ve que hay una influencia directa en la cantidad de siniestros viales cuando hay cruces y que esta del 75.4 %, lo cual es una cantidad muy alta.



