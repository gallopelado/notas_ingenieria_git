# Unidad I
## Elabora un ensayo académico sobre la historia de la ingeniería de software. Mínimamente consultando 3 autores, ya sea libros o artículos científicos
## Introducción
La historia de la ingeniería de software es amplia, de ella se ha escrito bastante desde distintas perspectivas, apoyando con fuerza la importancia de esta disciplina al momento de diseñar software. Pero no ha sido fácil porque debió se validada por mulitud de ingenierías y disciplinas científicas que velaban por un espectro estricto de normas y principios. A medida que transcurría el tiempo se hacía necesaria, ante el progreso tecnológico. Por medio de la opinión experta hemos traido conceptos sobre la historia de la misma para enriquecer el discurso académico de la disciplina.

## Planteamiento
### Según Albert Endres en "A Synopsis of Software Engineering History: The Industrial Perspective" páginas 20-24
Tal documento(paper) condensa un estudio de la historia de la ingeniería de software desde 1956 hasta la actualidad. Donde estructuró cuarenta años en tres eras en dos periodos de tiempo. Cada periodo se caracterizó por un conjunto de objetivos, métodos y herramientas inadvertidas, lecciones aprendidas e identificación de problemas.

#### Era I "Dominando la máquina"
Esta era comprende 12 años desde 1956 hasta 1967. Esta es una era donde el término "ingeniería de software" no fue acuñada aún. Los dos periodos son considerados ambos fuertemente influenciados por fuerzas externas. Esto es también el periodod de formación de la industria computacional.

##### El periodo de los lotes
Las primeras computadoras lograron un uso significativo en la industria, ya sean aplicaciones comerciales o científicas, era sistemas orientados a lotes "batch-oriented systems". Este modo de operación resultó del I/0 y storage media, estas son las tarjetas perforadas y cintas magnéticas. El objetivo principal era explotar los limitados recursos de hardware (almacenamiento y poder de cómputo). Cualquier uso menos óptimo duplicaría o triplicaría los tiempos de procesamiento, medidos en horas, o haciendo el trabajo totalmente inviable. También fue el periodo de los codigos, principalmente escritos en ensamblador, resultando en altos tiempos de compilación, estas se hacían en la noche. Ejemplos COBOL y FORTRAN.

##### El periodo interactivo
Durante la segunda mitad del los 60' el interés por los problemas de los lenguajes se alejó para otra cuestión general de las herramientas de desarrollo. El objetivo principal se redujo a aspectos de codificación y eliminación de la necesidad de modificar el objeto del código.
El entorno de hardware que soportaba este objetivo era la disponibilidad no volátil y de acceso aleatorio.
La tecnología de software desarrollada en este periodo fue la compilación incremental, edición de fuentes por niveles y debugging y la automatización de tests. También se desarrollaron los llamados lower CASE tools.
El objetivo de este periodo y la lección aprendida fue la conveniencia en el mantenimiento de programas del código fuente, en vez del código objeto. Es más, las personas empezaron a reconocer que desarrollar software es más que sólo codificar.

#### Era II "Dominando el proceso"
En esta era fue establecida la ingeniería de software como campo de estudio. Aproximadamente los finales del 1968 a 1982. También en esta era fue introducido el costeo de software por los vendedores de hardware.

##### El periodo de proceso
Es común asociar este periodo con el reconocimiento de las crisis de software. Algunas personas insisten que tal crisis aún sigue vigente. La crisis inicial convirtió las herramientas de codificación para el estudio de procesos de desarrollo, fue reconocido primero en la industria. Luego de eso, el asunto fue discutido fuertemente en los círculos académicos y de apropiado currículo, conferencias y revistas fueron establecidas.
El objetivo final deseado de este periodo fue la de reducir los riesgos y mejorar la calidad y productividad. Esto lideró estudios, identificando las causas por las que fallan los proyectos, recolectando información sobre los costos perdidos gastados por actividad y para el error en el análisis de software. Cada organización creo su propio conjunto de guías de estilo, expresando alguna fase aproximada al desarrollo. El principio de la verificación y balance fue aplicado donde fuese viable.
La clave de la lección aprendida durante este periodo fue que la calidad del producto no puede asegurarse solamente mirando el producto final, por ejemplo el resultado del ciclo de desarrollo. Asegurar la calidad tiene un direccionamiento entero en procesos de desarrollo particularmente en las fases iniciales.

##### El periodo formal
El objetivo principal de este periodo es la de incrementar la integridad del software y mejorar la productividad a través de la automatización de logros. Esto explica porque muchos practicantes ponen grandes esperanzas en estos métodos. Los métodos formales aplicados a la especificación de software, transformación y verificación. En la mayoría de casos, los proponentes tienen la espectativa que una especificación formal fue encontrada en el proceso de desarrollo restante y puede ser automatizado a través de series de correcciones preservando las transformaciones. Una menor demanda de soluciones es probado en el caso de verificación. Aquí hay una especificación formal que serviría como criterio para una implementación manual derivada que provea consistencia con la especificación original.
Para grandes proyectos, usualmente resultaban que ninguno de los requerimientos ni el diseño podían ser expresados en un modelo matemático. Para cada especificación pertenecen todo un conjunto no funcional de requerimientos para el cual las diferentes formas de expresión son relevantes.

#### Era III "Dominando la complejidad"
Esta era es desde 1983. El evento que causó el hito fue la llegada del PC. El primero de los dos periodos pueden ser considerados historia, el segundo periodo es el contemporáneo. Durante esta era la tradicional dominancia del hardware sobre el software finalizó. El hardware se convirtió en un subordinado del software, también ejemplificado por el tropiezo de algunas compañías(IBM, DEC) que eran formalmente grandes vendedores de hardware.
Esta compuesto por dos periodos, el estructurado y el orientado a objetos.
##### El periodo estructurado
Los metodos estructurados tienen su origen realmente precedidos de la era (Dijkstra, Mills, Wirth), en particular tan lejos como sus aplicaciones para el código y diseño. Que hicieron métodos estructurados penetrantes en la industria fue su aplicación para el análisis de requerimientos. Ayudó fuertemente la propagación de los monitores CRT, esto abrió a la computadoras como herramientas para ingenieros que se dedican a diseñar gráficos. Esto a su vez trajo a las GUI (Graphical User Interface). Esto trajo a su vez sorpresas porque los usuarios podía diseñar sus propias herramientas case, pero la empresa no estaba preparada para dicho cambio en cuanto a diseño y análisis. Si el diseño cambiaba el código debe cambiar también(the dichotomy) o viceversa. Si el código cambiaba el diseño debe ser actualizado, un problema aún peor.
##### El periodo de la orientación a objetos
En la era de la orientación a objetos, el potencial de la reusabilidad fue, así como conocemos, señalado por un visionario (McIlroy) hacia 1968. Aparecían conceptos como la modularización, encapsulamiento, portabilidad, mecanismos adicionales de herencia, polimorfismo.
Los problemas identificados en esta generación de métodos desarrollados principalmente relacionados con el aumento de la demanda sobre el testing y entendimiento del software. También el ciclo de tiempo aparece para converir un importante problema, particularmente si un mercado esta expandiéndose porque personas creativas ven oportunidades para innovar productos y servicios.

#### Conceptos de otros autores
##### Engineering/scientific software(Ingeniería de software) según "Software Engineering: A practitioner's Approach" by Roger S. Pressman
Formalmente definido como *number crunching* algoritmos, aplicaciones de ingeniería, ciencia del rango de astronomía hasta vulcanología, de análisis de estres automotor a lanzar orbital dinámico. Sin embargo, las modernas aplicaciones dentro de la ingeniería/ciencia están moviendo lejos de los algoritmos convencionales numéricos.

##### Diseño según "Encyclopedia of Software Engineering"
Diseñar consiste en la identificación de componentes mayores del sistema, especificando que debe realizar, y estableciendo las interfaces en medio de ellos. El diseño es el primer paso para la transformación de los requerimientos(un enunciado de qué debe ser terminado) dentro del software funcional(como los requerimientos son realizados)

#### ¿Qué es ingeniería? ¿Es un tema sensible hablar de ingeniería de software? by Stuart Shapiro páginas 45-46
Respondiendo estas preguntas ha sido una dificultad y un proceso tempestuoso el cual continua a día de hoy. Esto se vuelve claro cuando examinamos el discurso el cual toma un lugar en un número prominente profesionales, revistas, artículos de computación y software. Los participantes en este discurso representan un amplio rango de nacionalidades y educaciones y experiencias laborales. Este discurso sigiere que el software también en general tiene características el cual lo dibuja fundamentalmente diferentes de otras tecnologías. Como el campo de la ingeniería química, debería la computación y profesionales de software perseguir ese profesionalismo.
Historiadores y sociólogos han desacreditado la noción de la ingeniería es aplicada a la ciencia, pero esto no es sorprendente, estos mitos tienen un probado atractivo para la computación y otras tecnologías. 

## Conclusión
Consideramos la historia de la ingeniería de software como un conocimiento necesario para todo practicante, profesional debido a que gracias a esos momentos de dificultades y necesidades tecnológicas, surgieron soluciones que fueron cerrando la brecha del desconocimiento sobre esta disciplina, creando un principios, métodos probados y válidos aplicados a nivel tecnológicos y científicos.