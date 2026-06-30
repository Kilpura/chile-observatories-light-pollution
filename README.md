# Contaminación Lumínica en Observatorios Chilenos
## *Light Pollution Around Chilean Astronomical Observatories*

Análisis y predicción de tendencias de contaminación lumínica en observatorios chilenos usando datos VIIRS y Google Earth Engine.

> **Estado / Status:** En desarrollo — recopilación de datos activa  
> **Datos / Data:** VIIRS DNB (NOAA) via Google Earth Engine · 2012–2026  
> **Herramientas / Stack:** Python · Google Earth Engine · Pandas · Plotly · Streamlit  

### Contexto
 
Chile es el capital astronómico del mundo. Actualmente concentra cerca del **40% de la capacidad de observación astronómica global**, cifra que se proyecta supere el **60% hacia 2030** con la entrada en operaciones del Vera C. Rubin Observatory (Cerro Pachón, 2025) y el Extremely Large Telescope (Cerro Armazones, en construcción). En el desierto de Atacama se ubican algunos de los instrumentos más avanzados de la humanidad: el Very Large Telescope (VLT/ESO), ALMA, el Cerro Tololo Inter-American Observatory (CTIO), Las Campanas, La Silla y Gemini Sur, entre otros.
 
Esta condición privilegiada existe gracias a la convergencia de factores únicos: cielos excepcionalmente oscuros, más de 300 noches despejadas al año, baja humedad y estabilidad atmosférica que no tiene equivalente en el mundo.

### El problema
 
A pesar de esas condiciones naturales, los cielos del norte de Chile **están siendo amenazados**. Estudios recientes (Falchi et al. 2023, publicado en *MNRAS*) confirman que la contaminación lumínica ya es detectable incluso en zonas remotas del Atacama, y que las fuentes artificiales ya alteran el cielo nocturno alrededor de observatorios antes considerados prístinos.
 
Las presiones concretas que motivan este proyecto son varias:
 
- **Expansión urbana sostenida** en La Serena, Coquimbo y Antofagasta, ciudades cercanas a múltiples observatorios de clase mundial, cuyo brillo nocturno crece año a año según datos VIIRS.
- **Proyectos industriales de gran escala**: el caso más documentado y urgente es el proyecto INNA de AES Andes, un megacomplejo industrial de más de 3.000 hectáreas —puertos, plantas de hidrógeno y amoniaco verde, miles de fuentes de luz— proyectado a entre 5 y 11 km del Observatorio Paranal. Según análisis técnicos de ESO (2025), su construcción aumentaría la contaminación lumínica sobre el VLT en **al menos un 35%** y sobre el sitio del CTAO-Sur en más de un **50%**, niveles incompatibles con las condiciones requeridas para observaciones astronómicas de primer nivel.
- **Transición a tecnología LED**: la penetración de iluminación LED de amplio espectro en ciudades del norte —con emisiones en la parte azul del espectro que se dispersan mucho más en la atmósfera que el sodio de baja presión— ha acelerado el deterioro del cielo nocturno incluso donde la normativa vigente (DS043/2012) en principio se cumple.
- **Vacío regulatorio**: el propio Ministerio de Ciencias reconoció en 2025–2026 que los lineamientos técnicos vigentes son insuficientes para proteger sitios de observación extrema frente a megaproyectos, y comenzó un proceso de actualización. Esto hace que la evidencia cuantitativa sea urgente.
La preocupación es tal que en 2025 un grupo de astrónomos de fama mundial —incluyendo premios Nobel de Física como Reinhard Genzel, Michel Mayor, Didier Queloz y Adam Riess— firmaron una carta abierta al Gobierno de Chile exigiendo protección para los cielos de Paranal.

### Objetivos de este proyecto
 
Este proyecto tiene tres capas:
 
**1. Análisis descriptivo y temporal**  
Extraer y analizar la serie de tiempo de brillo nocturno artificial (radiancia VIIRS DNB) alrededor de 8 observatorios chilenos entre 2012 y 2026, comparando la evolución por sitio y por radio de influencia (5, 25, 50 y 100 km).
 
**2. Visualización pública e interactiva**  
Construir un dashboard web que muestre la evolución de la contaminación lumínica alrededor de cada observatorio, con mapas, gráficos de tendencia y comparaciones entre sitios — haciendo la evidencia accesible no solo para la comunidad científica sino también para tomadores de decisiones y público general.
 
**3. Modelo predictivo (en desarrollo)**  
Desarrollar un modelo de proyección que estime la evolución futura del brillo nocturno bajo distintos escenarios: crecimiento urbano tendencial, materialización de proyectos industriales como INNA, y escenarios de mitigación con regulación más estricta. La idea es responder: *¿qué le ocurre a los cielos de Paranal si no se detiene la tendencia actual?* y traducir esa respuesta en algo visual y cuantificable.

