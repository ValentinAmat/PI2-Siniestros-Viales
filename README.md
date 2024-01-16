<h1 align="center">Proyecto Data Analytics: Siniestros Viales</h1>
<p align="center">
  <img src="https://elonce-media.elonce.com/fotos-nuevo/2022/01/03/o_1641194393_1.jpg" alt="Logo de Steam" width=auto height="400" style="border-radius: 10px;">
</p>
<p align="center">
  <img src="https://assets.soyhenry.com/logoOG.png" alt="Logo de Henry" width=200 height="auto" style="border-radius: 5px;">
</p>

<hr/>

<h3>Contexto e introducción al proyecto:</h3>

Los siniestros viales fatales son accidentes de tráfico que resultan en la pérdida de vidas humanas. Estos constituyen una preocupación significativa en la Ciudad Autónoma de Buenos Aires (CABA), afectando la seguridad y bienestar de sus residentes. Este proyecto busca abordar esta problemática mediante un análisis detallado de los factores que contribuyen a estos incidentes, y poder comprender mejor la problemática. El proyecto no se centrará en proponer soluciones, sino en proporcionar una base analítica sólida que pueda orientar futuras intervenciones y políticas de seguridad vial en la ciudad.

El **Observatorio de Movilidad y Seguridad Vial** (OMSV), centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, nos proporciona el dataset "homicidios.xlsx" y nos solicita la elaboración de un proyecto de anális de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales.

Este proyecto consiste en realizar un **EDA** (Análisis Exploratorio de los Datos) sobre los datasets proporciondos por el **OMSV**. Este análisis debe estar acompañado de un **Dashboard** (panel visual) que muestre de manera resumida y fácil de entender datos, métricas o información clave.


<h3>Pasos del proyecto:</h3>

**1°**  
Comenzamos realizando el proceso de **ETL** (Extracción, Transformación y Carga) en el que extrajimos datos de diferentes fuentes, los transformamos según las necesidades del proyecto y los cargamos en un destino final para su análisis y uso posterior. El archivo utilizado para la carga fue "homicidios.xlsx" del directorio "Datasets". Este proceso se llevó a cabo en los notebooks "ETL_hechos_homicidios.ipynb" (se produjo el archivo "hechos_homicidios.csv") y "ETL_victimas_homicidios.ipynb" (se produjo el archivo "victimas_homicidios.csv"), dentro del deirectorio "ETL".  

**2°**  
En segundo lugar, realizamos el **EDA** con el objetivo de obtener insights, identificar patrones, tendencias y relaciones, y así tomar decisiones fundamentadas en base a la información obtenida. Este proceso se llevó a cabo en el notebook "EDA.ipynb".  

**3°**  
A continuación filtramos los datos que utilizaremos en los **KPIs** (Indicadores Clave de Rendimiento). Este proceso lo llevamos a cabo en el notebook "KPIs.ipynb" dentro del directorio "ETL". Los tres KPIs a desarrollar fueron:

- KPI 1: Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.
- KPI 2: Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.
- KPI 3: Reducir en un 10% la cantidad de accidentes nocturnos fatales de jóvenes en el último semestre, en CABA, respecto al semestre anterior.

El tercer KPI fue elegido debido a que, según la Organización Mundial de la salud, las lesiones causadas por accidentes de tránsito son la primera causa de muerte entre los jóvenes de 15 a 29 años. En Argentina se produjo un aumento del consumo de alcohol especialmente por parte de esta franja de edad, constituyendo una de las principales causas de los siniestros viales. En el artículo "[Los accidentes de tránsito son la primera causa de muerte juvenil](https://aval.com.ar/los-jovenes-la-previa-y-el-transito/)", se aborda esta conexión de manera detallada.  
Cabe destacar que para el desarrollo de la tasa en el primer KPI, se tomó como población total de CABA la cifra de 3121707 habitantes, información del censo de 2022.

**4°**  
Por último llevamos a cabo la creación del **Dashboard**. Para trabajar de manera más cómoda se optó por fusionar los archivos creados en el proceso de ETL, en un nuevo archivo "homicidios_fusion.csv". Este proceso se llevó a cabo en el notebook "Fusion_de_tablas.ipynb" dentro del deirectorio "ETL". Luego pasamos a PowerBI donde creamos un Dashboard que cuenta con 8 páginas:
- Inicio: se plantea el objetivo del proyecto, se aclara la procedencia de los datos utilizados y de qué años son dichos datos.
- Tiempo: mostramos información sobre medidas de tiempo: tendencia de fatalidades através de los años, cantidad de fatalidades en cada mes, porcentaje de accidentes en cada día de la semana.
- KPI 1: se enseña la primer medida KPI, se muestra la reducción (o aumento) de fatalidades que hubo en cada semestre, y la tasa de homicidios en siniestros viales (número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes).
- KPI 2: se dispone la segunda medida KPI, se muestra información sobre los siniestros viales fatales, en los que las víctimas son motociclistas: la reducción (o aumento) de fatalidades de motociclistas que hubo en cada año y los principales vehículos acusados de los accidentes de motociclitas, entre otros.
- KPI 3: la tercera medida KPI muestra información sobre fatalidades nocturnas juveniles, es decir, siniestros viales fatales en los que la víctima tenía entre 15 y 29 años de edad, que ocurrieron en horario nocturno (entre 22:00 y 7:00).
- Mapa: se muestra información geográfica, como un mapa de la ubicación de cada siniestro, una lista de las calles con más fatalidades registradas y el porcentaje de estos accidentes en cada tipo de calle.
- Conclusión: aquí se encuentran los insights, es decir, las percepciones, entendimientos o conclusiones significativas obtenidas a partir de la interpretación de datos.
- Fin: saludo y cierre del proyecto.


<h3>Insights:</h3>

- El 71,81% del total de accidentes fatales se produce en avenidas. De este 71,81%, hay un 8,53% que se produce únicamente en Avenida General Paz.
- La tendencia de fatalidades tuvo su pico más bajo en julio de 2020. Esto puede haber sido causa de la cuarentena por COVID-19. A su vez, el pico más alto se obtuvo en diciembre de ese mismo año.
- Las principales víctimas de siniestros viales fatales son motociclistas, con un 42,21% de los accidentes, y peatones, con un 37,54%.
- Siendo las motos las principales víctimas, el 30,26% de estos accidentes son producidos por autos, y el 26,57% son producidos por vehículos de carga (camiones, pick-ups, furgonetas, etc.).


<h3>Herramientas utilizadas:</h3> 

ETL: Python, Pandas.  
EDA: Python, Pandas, Matplotlib, Seaborn.  
Dashboard: PowerBI.  
(El filtrado de la información para los KPIs y la fusión de las tablas se considera parte del ETL)
 
<hr/>
<h3>Proyecto elaborado por Valentín Amat.</h3>
<h3>Contacto:</h3>

Linkedin: https://www.linkedin.com/in/valent%C3%ADn-amat-45b6b1252/

Mail: amatgil5@gmail.com