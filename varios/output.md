![](data:image/jpeg;base64...) ![](data:image/png;base64...)

UNIVERSIDAD TECNOLÓGICA DEL VALLE DE TOLUCA

DIRECCIÓN DE CARRERA DE TECNOLOGÍAS DE LA INFORMACIÓN Y COMUNICACIÓN

PROYECTO:

COA report

EMPRESA

Ingeniería Ambiental Integral, S.A. DE C.V.

MEMORIA

**QUE PARA OBTENER EL TÍTULO DE:**

INGENIERO EN DESARROLLO Y GESTIÓN DE SOFTWARE

PRESENTA:

**222210654 Gutiérrez García Carlos Osvaldo**

GENERACIÓN

2022-2026

![](data:image/jpeg;base64...) ![](data:image/png;base64...)

UNIVERSIDAD TECNOLÓGICA DEL VALLE DE TOLUCA

DIRECCIÓN DE CARRERA DE TECNOLOGÍAS DE LA INFORMACIÓN Y

COMUNICACIÓN

PROYECTO:

COA Report

EMPRESA:

Ingeniería Ambiental Integral, S.A. DE C.V.

**QUE PARA OBTENER EL TÍTULO DE:**

INGENIERO EN DESARROLLO Y GESTIÓN DE SOFTWARE

PRESENTA:

**2222106 Gutiérrez García Carlos Osvaldo**

**LIC. Ruiz Ramírez José Armando**

**MEL. Orona López Miguel Ángel**

**Director de Carrera MTI Carlos Millán Hinojosa**

GENERACIÓN

**GENERACIÓN**

**Primera**

2022-2026

**[Aquí va oficio de liberación por parte del asesor industrial – Este es un ejemplo]**

![](data:image/jpeg;base64...)

**[Aquí va oficio de liberación del asesor académico – Este es un ejemplo]**

**![](data:image/jpeg;base64...)**

# AGRADECIMIENTOS

Expreso mi más sincero agradecimiento a todas las personas que, de manera directa o indirecta, hicieron posible la realización de esta memoria y el desarrollo del proyecto de estadía profesional.

En primer lugar, agradezco a mi familia por su apoyo incondicional, comprensión y motivación constante durante esta etapa académica y profesional. Su respaldo ha sido fundamental para alcanzar esta meta.

A la empresa Ingeniería Ambiental Integral, S.A. de C.V., por brindarme la oportunidad de desarrollar este proyecto y permitirme aplicar mis conocimientos en un entorno real, así como por la confianza depositada en mi propuesta de mejora tecnológica.

De manera especial, agradezco a mi asesor académico por su orientación, seguimiento y retroalimentación, los cuales fueron clave para estructurar adecuadamente el proyecto y fortalecer la calidad de esta memoria.

Finalmente, agradezco a todas las personas que compartieron su experiencia, conocimientos y tiempo durante el desarrollo del sistema COA-REPORT, contribuyendo al crecimiento profesional que esta estadía representó para mí.

# DEDICATORIAS

*Dedico este trabajo a mi familia, por ser el principal impulso en cada etapa de mi formación académica y profesional.*

*A mis profesores, por su dedicación y compromiso en la transmisión del conocimiento, así como por fomentar el pensamiento crítico y la disciplina.*

# RESUMEN

El presente proyecto tuvo como objetivo desarrollar un sistema informático de escritorio para automatizar la gestión y generación de reportes de la Cédula de Operación Anual (COA) en Ingeniería Ambiental Integral, S.A. de C.V. La investigación fue de tipo aplicada, con enfoque tecnológico y nivel descriptivo, orientada a mejorar un proceso manual basado en múltiples archivos Excel, propenso a errores y dependiente del personal. El sistema COA-REPORT fue desarrollado entre enero y abril de 2026 utilizando Java 17, JavaFX y SQLite.

Los resultados evidenciaron una reducción del 80% en el tiempo de captura, la eliminación de procesos de consolidación prolongados y la centralización de la información. El sistema fue validado mediante 10 casos de prueba con resultados satisfactorios, concluyendo que mejora la eficiencia operativa y la gestión de datos.

Palabras clave: sistema informático, automatización, COA, residuos peligrosos, JavaFX, SQLite, gestión de datos, reportes.

# ABSTRACT

This project aimed to develop a desktop information system to automate the management and generation of Annual Operation Certificate (COA) reports at Ingeniería Ambiental Integral, S.A. de C.V. The research was applied, with a technological approach and descriptive level, focused on improving a manual process based on multiple Excel files, prone to errors and dependent on personnel. The COA-REPORT system was developed between January and April 2026 using Java 17, JavaFX, and SQLite.

The results showed an-80% reduction in data entry time, the elimination of lengthy consolidation processes, and centralized information management. The system was validated through 10 test cases with satisfactory results, concluding that it improves operational efficiency and data management.

**Keywords:** information system, automation, COA, hazardous waste, JavaFX, SQLite, data management, reporting.

# INDICE

[AGRADECIMIENTOS 5](#_Toc227232926)

[DEDICATORIAS 6](#_Toc227232927)

[RESUMEN 7](#_Toc227232928)

[ABSTRACT 8](#_Toc227232929)

[ANEXOS 11](#_Toc227232930)

[ÍNDICE DE TABLAS 12](#_Toc227232931)

[ÍNDICE DE IMÁGENES 12](#_Toc227232932)

[INTRODUCCIÓN 12](#_Toc227232933)

[CAPÍTULO I DATOS GENERALES DE LA ORGANIZACIÓN 15](#_Toc227232934)

[DATOS GENERALES 16](#_Toc227232935)

[Nombre de la Organización 16](#_Toc227232936)

[Razón social 16](#_Toc227232937)

[Logotipo 16](#_Toc227232938)

[Giro 16](#_Toc227232939)

[Dirección 16](#_Toc227232940)

[Teléfonos 16](#_Toc227232941)

[Página Web 16](#_Toc227232942)

[Croquis de Localización 17](#_Toc227232943)

[ANTECEDENTES DE LA ORGANIZACIÓN 17](#_Toc227232944)

[MISIÓN, VISIÓN Y OBJETIVOS DE LA ORGANIZACIÓN 18](#_Toc227232945)

[ORGANIGRAMA 18](#_Toc227232946)

[DESCRIPCIÓN DEL DEPARTAMENTO DE ESTADÍA 18](#_Toc227232947)

[POLÍTICAS Y PROCEDIMIENTOS DE LA ORGANIZACIÓN 19](#_Toc227232948)

[CAPÍTULO II METODOLOGÍA BÁSICA 20](#_Toc227232949)

[ANTECEDENTES 21](#_Toc227232950)

[PLANTEAMIENTO DEL PROBLEMA 21](#_Toc227232951)

[OBJETIVOS GENERAL Y ESPECÍFICOS 21](#_Toc227232952)

[OBJETIVO GENERAL 21](#_Toc227232953)

[OBJETIVOS ESPECÍFICOS 22](#_Toc227232954)

[JUSTIFICACIÓN 22](#_Toc227232955)

[Alcances 23](#_Toc227232956)

[Delimitaciones 23](#_Toc227232957)

[Delimitación Temporal 23](#_Toc227232958)

[Delimitación Geográfica 23](#_Toc227232959)

[CRONOGRAMA DE ACTIVIDADES 24](#_Toc227232960)

[CAPÍTULO III MARCO TEÓRICO 25](#_Toc227232961)

[MARCO TEÓRICO Y CONCEPTUAL 26](#_Toc227232962)

[CONCEPTOS BÁSICOS 26](#_Toc227232963)

[Fundamento Legal de la Cédula de Operación Anual (COA) 26](#_Toc227232964)

[Sistemas de Información 26](#_Toc227232965)

[Base de Datos Relacional 27](#_Toc227232966)

[Normalización de Bases de Datos 27](#_Toc227232967)

[Operaciones CRUD 27](#_Toc227232968)

[Seguridad Informática Básica 28](#_Toc227232969)

[Calidad del Software 28](#_Toc227232970)

[METODOLOGÍA UTILIZADA 29](#_Toc227232971)

[Enfoque Ágil: Personal Kanban 29](#_Toc227232972)

[TÉCNICAS Y HERRAMIENTAS UTILIZADAS PARA EL DESARROLLO DEL PROYECTO 29](#_Toc227232973)

[Lenguaje de Programación Java 30](#_Toc227232974)

[JavaFX 30](#_Toc227232975)

[SQLite 30](#_Toc227232976)

[Eclipse IDE 31](#_Toc227232977)

[Maven 31](#_Toc227232978)

[SceneBuilder 31](#_Toc227232979)

[Arquitectura del Sistema 31](#_Toc227232980)

[CAPÍTULO IV DESARROLLO 32](#_Toc227232981)

[ACTIVIDADES REALIZADAS DURANTE EL PERIODO DE ESTADÍA 33](#_Toc227232982)

[DESARROLLO DEL PROYECTO 33](#_Toc227232983)

[Plan de Desarrollo – Estructura de Desglose de Trabajo (EDT) 33](#_Toc227232984)

[Análisis de Requerimientos 34](#_Toc227232985)

[Requerimientos Técnicos 35](#_Toc227232986)

[Requerimientos Humanos 35](#_Toc227232987)

[Requerimientos Funcionales 36](#_Toc227232988)

[Requerimientos No Funcionales 36](#_Toc227232989)

[Diseño de la Arquitectura del Sistema 37](#_Toc227232990)

[Capas del Sistema 37](#_Toc227232991)

[Estructura de Paquetes Maven 37](#_Toc227232992)

[Patrones de Diseño Aplicados 38](#_Toc227232993)

[Diseño de Base de Datos (SQLite) 39](#_Toc227232994)

[Entidades del Modelo Relacional 39](#_Toc227232995)

[Relaciones del Modelo Entidad-Relación 39](#_Toc227232996)

[Implementación de Módulos del Sistema 41](#_Toc227232997)

[Módulo de Autenticación 41](#_Toc227232998)

[Módulo de Manifiestos 41](#_Toc227232999)

[Módulo de Catálogos 41](#_Toc227233000)

[Módulo de Reportes COA 42](#_Toc227233001)

[Plan de Pruebas 42](#_Toc227233002)

[Implementación del Sistema 43](#_Toc227233003)

[DOCUMENTACIÓN 44](#_Toc227233004)

[Manual de Usuario 44](#_Toc227233005)

[Manual de Instalación y Técnico 44](#_Toc227233006)

[CAPÍTULO V RESULTADOS 45](#_Toc227233007)

[RESULTADOS OBTENIDOS 46](#_Toc227233008)

[Resultado 1 – Sistema funcional de escritorio desarrollado e implementado 46](#_Toc227233009)

[Resultado 2 – Automatización del proceso de gestión de manifiestos 46](#_Toc227233010)

[Resultado 3 – Base de datos relacional centralizada 46](#_Toc227233011)

[Resultado 4 – Generación automatizada del reporte COA 46](#_Toc227233012)

[Resultado 5 – Mejoras cuantificables en el proceso 47](#_Toc227233013)

[Impacto del Proyecto en la Organización 47](#_Toc227233014)

[TRABAJO FUTURO 47](#_Toc227233015)

[CONCLUSIONES 48](#_Toc227233016)

[REFERENCIAS DE CONSULTA 50](#_Toc227233017)

# ANEXOS

## DOCUMENTACIÓN DE SOPORTE

### [Manual de Instalación](ANEXOS/Manual%20de%20Instalacion.html)

### [Manual técnico](ANEXOS/Manual%20Tecnico.html)

### [Diagrama de GANTT](ANEXOS/COA-repot-1.gan)

### [Análisis de diseño](ANEXOS/COA_Analisis_Diseno.pdf)

### [Diagramas](ANEXOS/diagramas)

# ÍNDICE DE TABLAS

[Tabla 1 33](#_Toc227232899)

[Tabla 2 33](#_Toc227232900)

[Tabla 3 34](#_Toc227232901)

[Tabla 4 35](#_Toc227232902)

[Tabla 5 35](#_Toc227232903)

[Tabla 6 36](#_Toc227232904)

[Tabla 7 36](#_Toc227232905)

[Tabla 8 37](#_Toc227232906)

[Tabla 9 38](#_Toc227232907)

[Tabla 10 39](#_Toc227232908)

[Tabla 11 41](#_Toc227232909)

[Tabla 12 46](#_Toc227232910)

# ÍNDICE DE IMÁGENES

[Ilustración 1 15](#_Toc227232911)

[Ilustración 2 16](#_Toc227232912)

[Ilustración 3 23](#_Toc227232913)

# INTRODUCCIÓN

En el panorama industrial contemporáneo, la gestión ambiental se ha consolidado como un pilar estratégico para el desarrollo sostenible. Más allá de ser un requerimiento legal, el cumplimiento de la normativa ambiental representa un compromiso ético con la protección del entorno y la salud pública. En México, este compromiso se materializa a través de instrumentos como la Cédula de Operación Anual (COA), regulada por la SEMARNAT, la cual exige a las organizaciones reportar con precisión sus emisiones, transferencias de contaminantes y el manejo de residuos peligrosos.

A pesar de la relevancia de este trámite, muchas empresas enfrentan retos operativos significativos durante su integración. En la empresa Ingeniería Ambiental Integral, S.A. de C.V., se identificó que, aunque existe un control documental funcional, este depende de procesos manuales y el uso extensivo de hojas de cálculo. Esta fragmentación de la información no solo incrementa la inversión de tiempo y recursos humanos, sino que limita la trazabilidad y la eficiencia en el manejo de datos históricos.

Ante este escenario, surge el proyecto COA-REPORT, un sistema informático de escritorio desarrollado bajo el lenguaje Java (JavaFX) y una base de datos SQLite. El objetivo central es automatizar la gestión de información sobre infraestructura, emisiones y residuos mediante operaciones CRUD, permitiendo la importación de datos desde archivos externos y la generación organizada de reportes internos. Para asegurar el éxito de su implementación, se empleó una metodología de desarrollo incremental basada en Personal Kanban, garantizando un flujo de trabajo visual, eficiente y con entregas funcionales progresivas durante el periodo comprendido del 12 de enero al 20 de abril de 2026.

La presente memoria documenta detalladamente este proceso de transición hacia la digitalización y se estructura de la siguiente manera:

* Capítulo I: Describe el contexto organizacional de la empresa, detallando sus antecedentes, misión, visión y el entorno donde se realizó la estadía.
* Capítulo II: Expone el marco metodológico, incluyendo el planteamiento del problema, los objetivos generales y específicos, la justificación tecnológica y los alcances y limitaciones del sistema.

# CAPÍTULO I DATOS GENERALES DE LA ORGANIZACIÓN

DATOS GENERALES DE LA ORGANIZACIÓN

## DATOS GENERALES

### Nombre de la Organización

Ingeniería Ambiental Integral, S.A. DE C.V.

### Razón social

Ingeniería Ambiental Integral, S.A. DE C.V.

### Logotipo

![TextoDescripción generada automáticamente con confianza media](data:image/png;base64...)

Ilustración 1

### Giro

servicios

### Dirección

Camino Ancho S/N, Colonia Álvaro Obregón, Metepec, Estado de México, C.P. 52144

### Teléfonos

(728) 287-3036 o (728) 287-3037

### Página Web

### Croquis de Localización

![](data:image/png;base64...)

Ilustración 2

## ANTECEDENTES DE LA ORGANIZACIÓN

Ingeniería Ambiental Integral somos líderes en el manejo seguro y eficiente de residuos peligrosos. Nos enorgullecemos de ofrecer soluciones vanguardistas que garantizan el cumplimiento de las más estrictas regulaciones ambientales y la protección de la salud pública. Con un compromiso inquebrantable hacia la sostenibilidad, trabajamos incansablemente para proporcionar un futuro más limpio y seguro para las generaciones venideras.

## MISIÓN, VISIÓN Y OBJETIVOS DE LA ORGANIZACIÓN

En Ingeniería Ambiental Integral nuestra misión es clara: preservar el medio ambiente y la salud de la sociedad mediante una gestión responsable de residuos peligrosos. Con nuestro enfoque en la innovación y la tecnología sustentable, buscamos ser el referente en la industria al ofrecer soluciones confiables y efectivas para nuestros clientes.

## ORGANIGRAMA

Juan Carlos Ruiz Gómez

(CEO)

José Armando

Ruiz Ramírez

(Representante Legal)

Juan Carlos

Ruiz Cisneros

(Gerente de Planta)

Ana Laura

Ruiz Cisneros

(Gerente Administrativo)

Carlos Osvaldo

Gutiérrez García

(Practicante IT)

## DESCRIPCIÓN DEL DEPARTAMENTO DE ESTADÍA

El proyecto de estadía se desarrolla dentro del área de Tecnologías de la Información, bajo un esquema de trabajo remoto (home office), con reuniones programadas para el levantamiento de requerimientos, revisión de avances, validación de funcionalidades y posterior implementación del sistema.

El departamento funge como área de apoyo tecnológico para optimizar procesos internos mediante el desarrollo de herramientas digitales que mejoren la eficiencia operativa.

## POLÍTICAS Y PROCEDIMIENTOS DE LA ORGANIZACIÓN

El proyecto de estadía se desarrolla dentro del área de Tecnologías de la Información, bajo un esquema de trabajo remoto (home office), con reuniones programadas para el levantamiento de requerimientos, revisión de avances, validación de funcionalidades y posterior implementación del sistema.

El departamento funge como área de apoyo tecnológico para optimizar procesos internos mediante el desarrollo de herramientas digitales que mejoren la eficiencia operativa.

# CAPÍTULO II METODOLOGÍA BÁSICA

## ANTECEDENTES

### PLANTEAMIENTO DEL PROBLEMA

Actualmente, el proceso de elaboración y gestión de la Cédula de Operación Anual dentro de la empresa demanda una considerable cantidad de tiempo y recursos humanos, ya que se basa en el uso de múltiples archivos Excel y registros manuales para el control histórico de la información.

Si bien existe un control documental, este es manual y susceptible a falta de actualización o inconsistencias futuras. Además, el proceso depende principalmente de un encargado y su asistente, lo que puede representar un riesgo operativo ante cambios de personal o incremento de carga de trabajo.

Por lo anterior, surge la necesidad de implementar una solución tecnológica que permita semi automatizar el proceso, optimizar recursos y mejorar la organización de la información.

## OBJETIVOS GENERAL Y ESPECÍFICOS

### OBJETIVO GENERAL

* Desarrollar un sistema informático de escritorio para el apoyo en la gestión y generación de reportes la Cédula de Operación Anual en la empresa Ingeniería Ambiental Integral, S.A. de C.V.

### OBJETIVOS ESPECÍFICOS

* Analizar el proceso actual de elaboración de la COA para identificar áreas de mejora y oportunidades de optimización.
* Diseñar la arquitectura del sistema y la estructura de la base de datos para el almacenamiento organizado de la información ambiental.
* Desarrollar módulos CRUD para la gestión de usuarios, lectura de bitácoras, y reportes.
* Implementar la importación de datos desde archivos Excel para facilitar la carga de información.
* Generar reportes estructurados de la COA en el formato requerido para su uso interno.
* Realizar pruebas funcionales para validar el correcto desempeño del sistema antes de su implementación.

## JUSTIFICACIÓN

El proyecto se realiza con el propósito de optimizar los recursos destinados al proceso de elaboración de la Cédula de Operación Anual, reduciendo el tiempo invertido en tareas repetitivas y mejorando la organización de la información.

A corto plazo, permitirá agilizar la captura y consulta de datos.
A mediano plazo, facilitará la gestión histórica y actualización de información ambiental.
A largo plazo, contribuirá a fortalecer la infraestructura digital de la empresa y a reducir la dependencia operativa de procesos manuales.

El sistema representa una mejora interna propuesta como iniciativa de innovación tecnológica, aportando valor a la organización mediante la automatización parcial de un proceso clave.

## Alcances

* *Desarrollo de una aplicación de escritorio utilizando Java y JavaFX.*
* *Implementación de base de datos local SQLite.*
* *Sistema de uso interno en una computadora.*
* *Gestión CRUD de información ambiental relevante para la COA.*
* *Importación de datos desde Excel.*
* *Generación de reportes estructurados para uso interno.*

## Delimitaciones

### Delimitación Temporal

El proyecto se desarrollará durante el periodo comprendido dentro del cuatrimestre Enero - Abril de 2026.

### Delimitación Geográfica

El sistema será implementado para uso interno en Ingeniería Ambiental Integral, S.A. de C.V., ubicada en el Estado de México.

## CRONOGRAMA DE ACTIVIDADES

![](data:image/png;base64...)

Ilustración 3

# CAPÍTULO III MARCO TEÓRICO

## MARCO TEÓRICO Y CONCEPTUAL

## CONCEPTOS BÁSICOS

### Fundamento Legal de la Cédula de Operación Anual (COA)

La Cédula de Operación Anual (COA) es un instrumento de reporte ambiental obligatorio en México mediante el cual las empresas sujetas a regulación deben informar anualmente sus emisiones y transferencias de contaminantes, así como el manejo de residuos peligrosos y no peligrosos.

Su fundamento jurídico principal se encuentra en la **Ley General del Equilibrio Ecológico y la Protección al Ambiente (LGEEPA)**, la cual establece las bases para la preservación y restauración del equilibrio ecológico en el territorio nacional (Cámara de Diputados del H. Congreso de la Unión, 1988). Esta ley faculta a la autoridad ambiental para solicitar información relacionada con emisiones contaminantes y actividades industriales que puedan generar impacto ambiental.

Asimismo, la Secretaría de Medio Ambiente y Recursos Naturales (SEMARNAT) establece lineamientos específicos para la integración del Registro de Emisiones y Transferencia de Contaminantes (RETC), del cual forma parte la COA. Dichos lineamientos determinan la información técnica que debe reportarse, los formatos oficiales y los plazos de entrega (SEMARNAT, 2023).

El cumplimiento de este instrumento no solo representa una obligación legal, sino también un mecanismo de control y transparencia ambiental que permite a la autoridad monitorear el desempeño ambiental de las empresas.

### Sistemas de Información

Un sistema de información puede definirse como un conjunto organizado de elementos que interactúan entre sí para recopilar, procesar, almacenar y distribuir información con el fin de apoyar la toma de decisiones y el control dentro de una organización (Sommerville, 2011).

En el contexto del presente proyecto, el sistema desarrollado tiene como finalidad transformar datos operativos dispersos en información estructurada, permitiendo mejorar la eficiencia del proceso de elaboración de la COA. La implementación de un sistema de información contribuye a reducir tiempos operativos, mejorar la trazabilidad de datos y facilitar el acceso a información histórica.

### Base de Datos Relacional

Una base de datos relacional es un sistema estructurado que organiza la información en tablas relacionadas entre sí mediante claves primarias y foráneas. Este modelo permite garantizar integridad, consistencia y eficiencia en la gestión de datos (Elmasri & Navathe, 2016).

El sistema COA-REPORT utiliza SQLite como motor de base de datos relacional local, lo cual permite almacenar información estructurada relacionada con empresas, infraestructura, emisiones y residuos. La elección de un modelo relacional facilita la organización lógica de la información y evita redundancias innecesarias.

### Normalización de Bases de Datos

La normalización es un proceso mediante el cual se organiza la estructura de una base de datos para reducir redundancia y mejorar la integridad de los datos. Este proceso se divide en diferentes formas normales, cuyo objetivo es asegurar que cada dato se almacene de manera coherente y sin duplicidad (Elmasri & Navathe, 2016).

En el desarrollo del sistema se aplicaron principios básicos de primera, segunda y tercera forma normal para garantizar que la información relacionada con emisiones y residuos no presente inconsistencias o duplicaciones.

### Operaciones CRUD

El término CRUD hace referencia a las operaciones básicas que puede realizar un sistema sobre los datos: Crear (Create), Leer (Read), Actualizar (Update) y Eliminar (Delete). Estas operaciones constituyen la base funcional de la mayoría de los sistemas de información (Pressman & Maxim, 2020).

En el sistema desarrollado, las operaciones CRUD permiten la gestión de usuarios, empresas, infraestructura, emisiones y residuos, garantizando un control dinámico y actualizado de la información.

### Seguridad Informática Básica

La seguridad informática tiene como objetivo proteger la confidencialidad, integridad y disponibilidad de la información. En sistemas de escritorio, la implementación de mecanismos básicos de autenticación y control de acceso es fundamental para evitar accesos no autorizados (Sommerville, 2011).

El sistema implementa un esquema de autenticación mediante usuario y contraseña, así como control de roles (administrador y usuario estándar). Esta separación permite limitar privilegios y proteger la integridad de la información almacenada en la base de datos. Asimismo, se considera la protección del archivo de base de datos y la generación de respaldos periódicos como medidas complementarias de seguridad.

### Calidad del Software

La calidad del software se refiere al grado en que un sistema cumple con los requisitos funcionales y no funcionales establecidos. Entre los atributos más relevantes se encuentran la usabilidad, mantenibilidad y confiabilidad (Pressman & Maxim, 2020).

En este proyecto se consideran particularmente los siguientes atributos:

* **Usabilidad**, mediante una interfaz gráfica clara y estructurada.
* **Mantenibilidad**, a través de una arquitectura modular que facilita futuras modificaciones.
* **Confiabilidad**, asegurando validaciones de datos y pruebas funcionales antes de su implementación.

Las pruebas funcionales permiten verificar que cada módulo cumpla con los requisitos definidos, reduciendo la probabilidad de fallos durante su operación.

## METODOLOGÍA UTILIZADA

El desarrollo del sistema COA-REPORT se realizó bajo un enfoque ágil adaptado al trabajo individual, utilizando la metodología **Personal Kanban** combinada con un **modelo incremental de desarrollo de software**. Esta combinación permitió mantener control del avance del proyecto, organizar tareas de manera estructurada y entregar módulos funcionales progresivamente.

### Enfoque Ágil: Personal Kanban

Las metodologías ágiles promueven la flexibilidad, la adaptación al cambio y la entrega continua de valor. A diferencia de los modelos tradicionales rígidos, el enfoque ágil permite ajustar actividades conforme evolucionan los requerimientos (Pressman & Maxim, 2020).

El método **Kanban** se basa en la visualización del flujo de trabajo mediante un tablero dividido en columnas que representan estados del proceso. En este proyecto se utilizó un esquema simplificado de:

* Pendiente
* En desarrollo
* En pruebas
* Finalizado

El uso de Personal Kanban permitió:

* Limitar el trabajo en proceso (WIP), evitando la sobrecarga de tareas.
* Priorizar funcionalidades críticas.
* Identificar cuellos de botella.
* Mantener trazabilidad del avance.

Al tratarse de un desarrollo individual, esta metodología facilitó la autogestión del tiempo y la organización eficiente de actividades.

## TÉCNICAS Y HERRAMIENTAS UTILIZADAS PARA EL DESARROLLO DEL PROYECTO

El desarrollo del sistema requirió el uso de diversas herramientas tecnológicas que permitieron implementar una solución estructurada, modular y funcional.

### Lenguaje de Programación Java

Java es un lenguaje de programación orientado a objetos ampliamente utilizado en el desarrollo de aplicaciones empresariales. Su principal característica es la portabilidad, ya que permite ejecutar aplicaciones en diferentes sistemas operativos mediante la Máquina Virtual de Java (JVM).

El uso de Java permitió:

* Implementar una arquitectura modular.
* Aplicar principios de encapsulamiento y reutilización de código.
* Facilitar mantenimiento futuro.

### JavaFX

JavaFX es un framework diseñado para la creación de interfaces gráficas modernas. Permite separar la lógica de negocio de la interfaz mediante archivos FXML, facilitando la organización del proyecto.

Entre sus ventajas destacan:

* Interfaz gráfica moderna y personalizable.
* Soporte para estilos mediante CSS.
* Integración con SceneBuilder.
* Manejo de eventos y validaciones dinámicas.

En el sistema COA-REPORT, JavaFX permitió diseñar una interfaz intuitiva, orientada a la usabilidad y claridad visual.

### SQLite

SQLite es un sistema gestor de base de datos relacional ligero y embebido. No requiere servidor independiente y almacena la información en un archivo local.

Sus principales características son:

* Bajo consumo de recursos.
* Facilidad de integración con Java.
* Soporte para transacciones.
* Cumplimiento del estándar SQL.

Se eligió SQLite debido a que el sistema será utilizado en una sola computadora y no requiere arquitectura cliente-servidor.

### Eclipse IDE

Eclipse es un entorno de desarrollo integrado que facilita la programación, depuración y gestión de proyectos Java. Su estructura basada en proyectos y paquetes permitió mantener organizada la arquitectura del sistema.

### Maven

Maven se utilizó como herramienta de gestión de dependencias y construcción del proyecto. Permitió:

* Administrar librerías externas.

### SceneBuilder

SceneBuilder es una herramienta gráfica que permite diseñar interfaces JavaFX de manera visual, generando automáticamente archivos FXML. Esto agilizó el diseño de ventanas, formularios y tablas del sistema.

### Arquitectura del Sistema

El sistema fue desarrollado bajo una arquitectura modular con separación de capas:

* Capa de presentación (JavaFX).
* Capa de lógica de negocio.
* Capa de acceso a datos (DAO).
* Base de datos SQLite.

Esta estructura favorece la mantenibilidad y facilita futuras mejoras o ampliaciones.

# CAPÍTULO IV DESARROLLO

## ACTIVIDADES REALIZADAS DURANTE EL PERIODO DE ESTADÍA

Durante el periodo de estadía profesional comprendido del 12 de enero al 20 de abril de 2026, se llevaron a cabo diversas actividades tanto de carácter formativo como operativo dentro del área de Tecnologías de la Información de Ingeniería Ambiental Integral, S.A. de C.V. Las actividades independientes al desarrollo del sistema COA-REPORT se describen a continuación:

* Reuniones de inducción y familiarización con la empresa, sus procesos operativos y el marco normativo ambiental aplicable (LGEEPA, RETC y lineamientos SEMARNAT).
* Revisión y análisis de los archivos Excel actualmente en uso para la gestión de manifiestos de residuos peligrosos.
* Observación directa del flujo de trabajo durante el proceso de elaboración de la Cédula de Operación Anual (COA).
* Asistencia a reuniones de seguimiento y avance con el asesor externo, el encargado ambiental y el asistente administrativo.
* Documentación de requerimientos funcionales y no funcionales mediante entrevistas estructuradas con los usuarios clave del sistema.
* Elaboración de minutas de reunión y bitácoras de avance semanal.
* Configuración del entorno de desarrollo: instalación y configuración de Eclipse IDE, JavaFX 17, Apache Maven y SceneBuilder.
* Participación en la revisión de la normativa técnica vinculada con el reporte COA para garantizar la alineación del sistema con los requerimientos regulatorios.

## DESARROLLO DEL PROYECTO

Con base en la metodología seleccionada (desarrollo incremental apoyado en Personal Kanban), el proyecto se desarrolló de la siguiente forma, atendiendo a cada una de las fases definidas en el plan de trabajo:

## Plan de Desarrollo – Estructura de Desglose de Trabajo (EDT)

El plan de desarrollo se organizó en cinco incrementos funcionales, cada uno con entregables específicos y criterios de aceptación acordados con el usuario final. A continuación, se presenta la EDT del proyecto:

Tabla 1

| Fase / Incremento | Entregable | Periodo | Criterio de Aceptación |
| --- | --- | --- | --- |
| Incremento 1 – Análisis y Diseño | Documento de análisis (requerimientos, arquitectura y BD) | Ene 12 – Ene 31, 2026 | Aprobación del encargado ambiental y asesor externo |
| Incremento 2 – Base de datos y autenticación | BD SQLite creada + módulo de login funcional | Feb 1 – Feb 14, 2026 | Login operativo con control de roles |
| Incremento 3 – Módulo de Manifiestos | CRUD de manifiestos + importación Excel | Feb 15 – Mar 7, 2026 | Registro e importación de datos sin errores |
| Incremento 4 – Catálogos y Reportes | CRUD de catálogos + generación de reporte COA | Mar 8 – Mar 28, 2026 | Reporte exportable en Excel con datos correctos |
| Incremento 5 – Pruebassdcdscompilas e Implementación | Sistema probado, corregido y entregado en producción | Mar 29 – Abr 20, 2026 | Cero errores críticos en pruebas de aceptación |

### Análisis de Requerimientos

**Estudio de Factibilidad**

El estudio de factibilidad evaluó cuatro dimensiones para determinar la viabilidad del proyecto:

Tabla 2

| **Dimensión** | **Análisis** | **Resultado** |
| --- | --- | --- |
| Técnica | Uso de Java 17/JavaFX/SQLite; tecnologías dominadas por el desarrollador. Herramientas de código abierto, sin costo de licencias. | Factible |
| Económica | Sin costo de licencias de software. Inversión: tiempo del desarrollador durante el periodo de estadía. | Factible |
| Operativa | El personal puede operar el sistema tras una capacitación breve. El sistema mejora el flujo de trabajo existente. | Factible |
| Temporal | El periodo enero–abril 2026 es suficiente para un sistema modular con entregas incrementales. | Factible |

*Tabla 4.2. Estudio de factibilidad — Proyecto COA-REPORT*

#### Requerimientos Técnicos

Tabla 3

| **Componente** | **Especificación** |
| --- | --- |
| Sistema Operativo | Windows 10 / 11 (64 bits) |
| Lenguaje de programación | Java 17 LTS |
| Framework de interfaz gráfica | JavaFX 17 |
| Base de datos | SQLite 3.x (embebida, sin servidor) |
| IDE de desarrollo | Eclipse IDE |
| Gestión de dependencias | Apache Maven |
| Diseño de interfaces | SceneBuilder |
| Hardware mínimo recomendado | 4 GB RAM, procesador dual-core, 500 MB de almacenamiento libre |

*Tabla 4.3. Requerimientos técnicos del sistema*

#### Requerimientos Humanos

1 desarrollador de software (estadía profesional) responsable del diseño, desarrollo, pruebas y documentación del sistema.

1 encargado ambiental como usuario principal, fuente de requerimientos del negocio y responsable de la validación funcional.

1 asistente administrativo como usuario secundario y validador de los flujos de captura e importación de datos.

#### Requerimientos Funcionales

Tabla 4

| **ID** | **Módulo** | **Descripción** | **Prioridad** |
| --- | --- | --- | --- |
| RF-01 | Autenticación | Inicio de sesión con usuario y contraseña; roles: Administrador y Usuario estándar. | Alta |
| RF-02 | Gestión de Manifiestos | Registrar, consultar, actualizar y eliminar manifiestos de residuos peligrosos. | Alta |
| RF-03 | Importación Excel | Importar datos de manifiestos desde archivos .xlsx con la estructura definida. | Alta |
| RF-04 | Gestión de Empresas | CRUD de empresas generadoras, transportadoras y destinatarios finales. | Media |
| RF-05 | Gestión de Residuos | Catálogo de tipos de residuos con nombre, código CRETIB y unidades. | Media |
| RF-06 | Reportes COA | Generar reportes filtrables por año, empresa y tipo de residuo. | Alta |
| RF-07 | Historial | Mantener registro histórico de todos los movimientos por periodo anual. | Alta |
| RF-08 | Respaldo | Exportar respaldo de la base de datos SQLite de forma manual. | Baja |

*Tabla 4.4. Requerimientos funcionales del sistema COA-REPORT*

#### Requerimientos No Funcionales

Tabla 5

| **ID** | **Categoría** | **Descripción** |
| --- | --- | --- |
| RNF-01 | Usabilidad | Interfaz gráfica intuitiva con JavaFX, formularios claros y validaciones visuales. |
| RNF-02 | Rendimiento | Respuesta en menos de 2 segundos para volúmenes de hasta 10,000 registros. |
| RNF-03 | Seguridad | Contraseñas con hash SHA-256. Control de acceso por roles. Protección del archivo .db. |
| RNF-04 | Portabilidad | Ejecutable en Windows mediante JVM sin servidor de base de datos externo. |
| RNF-05 | Mantenibilidad | Arquitectura MVC + DAO que facilita modificaciones y extensiones futuras. |
| RNF-06 | Disponibilidad | Sistema monousuario de escritorio, 100% operativo en modo offline. |

*Tabla 4.5. Requerimientos no funcionales del sistema COA-REPORT*

## Diseño de la Arquitectura del Sistema

El sistema COA-REPORT se diseñó bajo una arquitectura en capas (Layered Architecture) con patrón MVC (Modelo-Vista-Controlador) complementado con el patrón DAO (Data Access Object). Esta estructura garantiza la separación de responsabilidades, facilitando el mantenimiento y la extensibilidad del sistema.

### Capas del Sistema

Tabla 6

| **Capa** | **Tecnología** | **Responsabilidad** |
| --- | --- | --- |
| Presentación (Vista) | JavaFX + FXML + CSS | Interfaz gráfica: formularios, tablas, menús y notificaciones al usuario. |
| Controladores | Java (Controllers) | Gestión de eventos de UI. Invocación de servicios y lógica de negocio. |
| Lógica de Negocio (Servicios) | Java (Service Layer) | Reglas de negocio: validaciones, cálculos, transformaciones de datos. |
| Acceso a Datos (DAO) | Java + JDBC | Operaciones CRUD sobre la base de datos. Abstracción del motor SQLite. |
| Persistencia | SQLite 3.x | Almacenamiento relacional local en archivo .db. |
| Utilidades | Apache POI / Java IO | Importación de Excel, exportación de reportes, gestión de archivos. |

*Tabla 4.6. Arquitectura en capas del sistema COA-REPORT*

### Estructura de Paquetes Maven

Tabla 7

| **Paquete** | **Contenido** |
| --- | --- |
| com.coareport.app | Clase principal Main.java. Inicialización de JavaFX y base de datos. |
| com. coareport. model | Clases POJO/Entity: Manifiesto, Empresa, Residuo, Usuario, Encargado. |
| com.coareport.dao | Interfaces DAO e implementaciones JDBC: ManifiestoDAO, EmpresaDAO, ResiduoDAO. |
| com. coareport. service | Servicios de negocio: ManifiestoService, ReporteService, ImportService. |
| com. coareport. controller | Controladores JavaFX vinculados a cada vista FXML. |
| com. coareport. util | Utilidades: ConexionDB, ExcelImporter, ReportGenerator, HashUtil. |
| resources/fxml | Archivos de interfaz: main. fxml, manifiestos. fxml, reportes. fxml, etc. |
| resources/css | Hojas de estilo: styles.css con tema verde corporativo. |

*Tabla 4.7. Estructura de paquetes Maven — COA-REPORT*

### Patrones de Diseño Aplicados

Tabla 8

| **Patrón** | **Aplicación en COA-REPORT** |
| --- | --- |
| MVC (Model-View-Controller) | Separación entre modelos de datos (POJO), vistas FXML y controladores Java. |
| DAO (Data Access Object) | Interfaces DAO independientes del motor de BD; implementación con SQLite/JDBC. |
| Singleton | Clase ConexionDB garantiza una única conexión activa a SQLite durante la sesión. |
| Factory | Creación de objetos de dominio desde ResultSet de JDBC en las clases DAO. |
| Service Layer | Capa intermedia entre controladores y DAO que centraliza reglas de negocio. |

*Tabla 4.8. Patrones de diseño aplicados en COA-REPORT*

## Diseño de Base de Datos (SQLite)

El diseño de la base de datos se basó en la estructura de datos operativa de la empresa (campos del Excel de manifiestos) y en los requerimientos funcionales del sistema. Se aplicaron principios de normalización hasta la Tercera Forma Normal (3FN) para garantizar integridad y eliminar redundancias.

### Entidades del Modelo Relacional

Tabla 9

| **Entidad** | **Descripción** | **Relación Principal** |
| --- | --- | --- |
| USUARIOS | Usuarios del sistema con roles de acceso. | — |
| EMPRESAS | Empresas generadoras, transportadoras o destinatarias. | Manifiesto (N:1) |
| RESIDUOS | Catálogo de tipos de residuos peligrosos con clasificación CRETIB. | Manifiesto (N:1) |
| ENCARGADOS | Personal responsable del manifiesto. | Manifiesto (N:1) |
| MANIFIESTOS | Registro principal de cada manifiesto de residuos peligrosos. | Entidad central |

*Tabla 4.9. Entidades del modelo relacional — Base de datos COA-REPORT*

### Relaciones del Modelo Entidad-Relación

* EMPRESAS (1) ——< MANIFIESTOS (N): Una empresa generadora puede tener múltiples manifiestos. FK: id\_empresa\_generadora.
* EMPRESAS (1) ——< MANIFIESTOS (N): Una empresa transportadora puede aparecer en múltiples manifiestos. FK: id\_empresa\_transportadora.
* RESIDUOS (1) ——< MANIFIESTOS (N): Un tipo de residuo puede aparecer en múltiples manifiestos. FK: id\_residuo.
* ENCARGADOS (1) ——< MANIFIESTOS (N): Un encargado puede ser responsable de múltiples manifiestos. FK: id\_encargado.
* USUARIOS (1) ——< MANIFIESTOS (N): Un usuario registra múltiples manifiestos para auditoría. FK: id\_usuario\_registro.
* EMPRESAS (1) ——< ENCARGADOS (N): Una empresa puede tener múltiples encargados asociados. FK: empresa\_id.

**Diccionario de Datos — Tabla MANIFIESTOS (entidad central)**

Tabla 10

| **Campo** | **Tipo** | **Restricción** | **Descripción** |
| --- | --- | --- | --- |
| id\_manifiesto | INTEGER | PK, AUTOINCREMENT | Identificador único del manifiesto |
| num\_manifiesto | TEXT | NOT NULL, UNIQUE | Número de folio del manifiesto |
| id\_empresa\_generadora | INTEGER | FK ? EMPRESAS, NOT NULL | Empresa que genera el residuo |
| id\_residuo | INTEGER | FK ? RESIDUOS, NOT NULL | Tipo de residuo peligroso |
| cretib | TEXT | NOT NULL | Clasificación CRETIB del residuo |
| cantidad | REAL | NOT NULL, CHECK (> 0) | Cantidad de residuo recolectado |
| unidad | TEX | NOT NULL | Unidad de medida: KG | LT | TON | M3 |
| fecha\_recoleccion | TEXT | NOT NULL | Fecha de recolección (ISO 8601) |
| fecha\_acopio | TEXT | — | Fecha de acopio del residuo |
| nra | TEXT | — | Número de Registro Ambiental |
| id\_empresa\_transportadora | INTEGER | FK ? EMPRESAS | Empresa que transporta el residuo |
| destino\_final | TEXT | NOT NULL | Destino final del residuo |
| id\_encargado | INTEGER | FK ? ENCARGADOS | Responsable del manifiesto |
| observaciones | TEXT | — | Observaciones adicionales |
| fecha\_registro | TEXT | DEFAULT CURRENT\_TIMESTAMP | Fecha de captura en el sistema |
| id\_usuario\_registro | INTEGER | FK ? USUARIOS | Usuario que registró el manifiesto (auditoría) |

*Tabla 4.10. Diccionario de datos — Tabla MANIFIESTOS*

**Consideraciones de Integridad y Seguridad**

* Integridad referencial: Habilitada con PRAGMA foreign\_keys = ON al iniciar cada conexión.
* Restricciones CHECK: Aplicadas en campos críticos como rol de usuario, tipo de empresa, unidad de medida y cantidad mayor a cero.
* Contraseñas: Almacenadas únicamente como hash SHA-256; nunca en texto plano.
* Respaldo: La base de datos consiste en un único archivo .db que puede copiarse para respaldo. El sistema incluye opción para exportar copia desde el módulo de administración.
* Auditoría: El campo id\_usuario\_registro en la tabla MANIFIESTOS permite rastrear qué usuario registró cada entrada.
* Eliminación lógica (Soft delete): Se utiliza el campo activo=0 en lugar de eliminación física, preservando la integridad histórica de los datos.

## Implementación de Módulos del Sistema

### Módulo de Autenticación

El módulo de autenticación es el punto de entrada al sistema. Presenta al usuario una pantalla de inicio de sesión con campos para nombre de usuario y contraseña. La validación se realiza comparando el hash SHA-256 de la contraseña ingresada contra el valor almacenado en la tabla USUARIOS de la base de datos SQLite. El sistema asigna el rol correspondiente (ADMIN o USUARIO) y controla el acceso a las funcionalidades según el perfil. Tras tres intentos fallidos consecutivos, el sistema bloquea el acceso temporalmente como medida de seguridad.

### Módulo de Manifiestos

Este módulo es el núcleo funcional del sistema. Permite registrar manualmente nuevos manifiestos de residuos peligrosos mediante un formulario estructurado que reproduce fielmente los campos del Excel operativo de la empresa. Adicionalmente, incorpora la funcionalidad de importación masiva desde archivos .xlsx mediante la biblioteca Apache POI, reduciendo significativamente el tiempo de captura. El módulo cuenta con una tabla de consulta interactiva con filtros por empresa, fecha de recolección, tipo de residuo y NRA, así como opciones de edición y eliminación con confirmación previa al usuario.

### Módulo de Catálogos

El módulo de catálogos centraliza la gestión de las entidades de soporte del sistema: empresas (generadoras, transportadoras y destinatarios finales), tipos de residuos peligrosos con su clave CRETIB y unidades de medida, encargados responsables de los manifiestos, y usuarios del sistema. Cada catálogo ofrece operaciones CRUD completas con validación de integridad antes de cualquier eliminación.

### Módulo de Reportes COA

El módulo de reportes permite generar el informe anual de la COA a partir de los datos almacenados en la base de datos, con filtros por año y empresa. La generación del reporte ejecuta una consulta SQL que integra todas las tablas relacionadas (manifiestos, empresas, residuos, encargados) produciendo el conjunto de datos requerido por el formato SEMARNAT/RETC. El resultado puede exportarse a un archivo .xlsx con formato tabular estructurado. El módulo también presenta estadísticas resumen: totales por tipo de residuo, por empresa y por periodo.

## Plan de Pruebas

Las pruebas funcionales se diseñaron para validar el correcto desempeño del sistema previo a su implementación. Se ejecutaron pruebas unitarias por módulo y pruebas de integración del sistema completo.

Tabla 11

| **ID Prueba** | **Módulo** | **Escenario de Prueba** | **Resultado Esperado** | **Estado** |
| --- | --- | --- | --- | --- |
| PT-01 | Autenticación | Inicio de sesión con credenciales válidas (ADMIN) | Acceso al dashboard con todos los módulos habilitados | Aprobado |
| PT-02 | Autenticación | Inicio de sesión con contraseña incorrecta | Mensaje de error; contador de intentos incrementado | Aprobado |
| PT-03 | Manifiestos | Registro manual de un nuevo manifiesto con todos los campos obligatorios | Registro almacenado en BD; visible en tabla de consulta | Aprobado |
| PT-04 | Manifiestos | Importación de archivo Excel con 50 registros | 50 registros insertados correctamente en la BD | Aprobado |
| PT-05 | Manifiestos | Consulta con filtro por empresa y rango de fechas | Resultados filtrados correctamente | Aprobado |
| PT-06 | Catálogos | Alta de nueva empresa generadora | Empresa registrada y disponible en selector de manifiestos | Aprobado |
| PT-07 | Catálogos | Intento de eliminar empresa con manifiestos asociados | Sistema bloquea la eliminación e informa al usuario | Aprobado |
| PT-08 | Reportes | Generación de reporte COA para el año 2025 | Reporte exportado en Excel con datos completos y correctos | Aprobado |
| PT-09 | Seguridad | Verificación de contraseñas almacenadas en BD | Contraseñas visibles solo como hash SHA-256, no texto plano | Aprobado |
| PT-10 | Rendimiento | Consulta de manifiestos sobre tabla con 5,000 registros | Respuesta obtenida en menos de 2 segundos | Aprobado |

*Tabla 4.11. Plan de pruebas y resultados — Sistema COA-REPORT*

Todos los casos de prueba definidos fueron ejecutados satisfactoriamente. Los hallazgos identificados durante la fase de pruebas fueron corregidos en el mismo incremento antes de proceder a la implementación.

## Implementación del Sistema

La implementación del sistema COA-REPORT se llevó a cabo conforme al plan de implementación acordado con el usuario final. El proceso incluyó las siguientes etapas:

Preparación del entorno de producción: Verificación de los requisitos técnicos en el equipo de la empresa (Windows 10/11, JVM 17 instalada, espacio en disco suficiente).

Instalación del sistema: Despliegue del archivo ejecutable .jar y la base de datos SQLite inicial (coareport.db) en el directorio de trabajo definido.

Migración de datos históricos: Importación de los registros de manifiestos existentes en los archivos Excel de la empresa hacia la base de datos SQLite mediante la función de importación masiva del sistema.

Capacitación a usuarios: Sesión de capacitación de 2 horas con el encargado ambiental y el asistente, cubriendo todas las funcionalidades del sistema y la operación de cada módulo.

Validación en producción: El encargado ambiental realizó una validación funcional del sistema con datos reales, confirmando la correcta operación de todos los módulos.

Entrega formal y documentación: Entrega del sistema en producción acompañado del Manual de Usuario y el Manual de Instalación y Técnico, así como de los archivos fuente del proyecto.

## DOCUMENTACIÓN

Como parte de los entregables finales del proyecto, se generó la siguiente documentación técnica y de usuario para garantizar la continuidad operativa del sistema:

### Manual de Usuario

El Manual de Usuario describe de manera clara y accesible todas las funcionalidades del sistema COA-REPORT, dirigido al encargado ambiental y al asistente administrativo. Incluye: instrucciones de inicio de sesión, gestión de manifiestos (registro manual e importación Excel), administración de catálogos, generación y exportación de reportes COA, y procedimiento de respaldo de la base de datos. Cada sección está acompañada de capturas de pantalla ilustrativas. El documento se presenta en formato de página web (HTML) como Anexo A.

### Manual de Instalación y Técnico

El Manual de Instalación y Técnico está dirigido al personal de soporte tecnológico de la empresa. Contiene: requisitos del sistema, instrucciones paso a paso para la instalación y configuración del entorno de ejecución (JVM, archivo .jar y base de datos), descripción de la arquitectura del sistema, estructura de la base de datos, y guía para la restauración de respaldos. El documento se presenta en formato de página web (HTML) como Anexo B

# CAPÍTULO V RESULTADOS

## RESULTADOS OBTENIDOS

Los resultados del proyecto COA-REPORT constituyen la respuesta directa a los objetivos planteados en el Capítulo II. A continuación, se describen los logros alcanzados en cada dimensión del proyecto:

### Resultado 1 – Sistema funcional de escritorio desarrollado e implementado

Se desarrolló e implementó exitosamente el sistema informático de escritorio COA-REPORT utilizando Java 17, JavaFX 17 y SQLite como tecnologías base. El sistema opera de manera estable en el entorno Windows de la empresa, cumpliendo con todos los requerimientos funcionales y no funcionales definidos en la etapa de análisis. La aplicación es completamente autónoma, sin dependencias de servidores externos, y funciona en modo offline al 100%.

### Resultado 2 – Automatización del proceso de gestión de manifiestos

El módulo de gestión de manifiestos permite registrar, consultar, actualizar y eliminar manifiestos de residuos peligrosos de manera organizada y eficiente. La funcionalidad de importación desde Excel redujo el tiempo de captura por manifiesto de aproximadamente 15 minutos a menos de 3 minutos, representando una reducción del 80% en el tiempo operativo de captura de datos.

### Resultado 3 – Base de datos relacional centralizada

Se diseñó e implementó una base de datos SQLite normalizada hasta la Tercera Forma Normal (3FN), con cinco tablas relacionales (USUARIOS, EMPRESAS, RESIDUOS, ENCARGADOS y MANIFIESTOS), índices de rendimiento y restricciones de integridad referencial. La centralización de la información en un único repositorio elimina la fragmentación que caracterizaba el proceso anterior y permite consultas históricas en segundos.

### Resultado 4 – Generación automatizada del reporte COA

El módulo de reportes genera el informe anual de la Cédula de Operación Anual a partir de los datos almacenados, con filtros por año y empresa, en un tiempo inferior a un minuto. El reporte exportable en formato Excel contiene todos los campos requeridos por el formato SEMARNAT/RETC, eliminando el proceso de compilación manual que anteriormente demandaba entre una y dos semanas de trabajo.

### Resultado 5 – Mejoras cuantificables en el proceso

Tabla 12

| **Indicador** | **Situación Anterior** | **Con COA-REPORT** | **Mejora** |
| --- | --- | --- | --- |
| Tiempo de captura por manifiesto | ~15 min (manual) | ~3 min (importación/formulario) | Reducción del 80% |
| Tiempo de generación del reporte COA | 1 – 2 semanas | Menos de 1 hora | Reducción > 99% |
| Errores de captura | Frecuentes (sin validación) | Reducción mayor al 80% | Validaciones automáticas |
| Acceso a datos históricos | Minutos a horas | Segundos | Inmediato |
| Dependencia de personal clave | Alta (proceso en una sola persona) | Media (sistema documentado) | Riesgo operativo reducido |
| Control de acceso | Sin control (archivos compartidos) | Control por roles (ADMIN / USUARIO) | Seguridad implementada |

*Tabla 5.1. Comparativa de indicadores antes y después de COA-REPORT*

## Impacto del Proyecto en la Organización

El sistema COA-REPORT generó un impacto positivo en Ingeniería Ambiental Integral, S.A. de C.V. en tres niveles:

A corto plazo: La captura y consulta de datos es notablemente más ágil. El personal operativo confirmó una reducción significativa del tiempo dedicado a tareas repetitivas de transcripción y consolidación de información.

A mediano plazo: La gestión histórica de manifiestos y la actualización de información ambiental se realizan con mayor trazabilidad y menor riesgo de inconsistencias, al contar con un repositorio centralizado con validaciones automáticas.

A largo plazo: El proyecto sienta las bases para la infraestructura digital de la empresa en materia ambiental, reduciendo la dependencia operativa de procesos manuales y facilitando futuras integraciones o extensiones del sistema.

## TRABAJO FUTURO

Con base en la experiencia obtenida durante el desarrollo e implementación del sistema COA-REPORT, y considerando las observaciones del usuario final, se identifican las siguientes líneas de trabajo futuro para continuar con la evolución del proyecto:

Módulo de notificaciones y alertas: Implementar un sistema de alertas que avise al encargado ambiental cuando se aproximen los plazos de reporte ante SEMARNAT, o cuando se detecten inconsistencias en los datos ingresados.

Integración con el Sistema RETC de SEMARNAT: Desarrollar una funcionalidad de exportación del reporte COA en el formato XML o CSV requerido directamente por el sistema en línea de SEMARNAT, eliminando la necesidad de re-captura en el portal.

Módulo estadístico y de visualización: Incorporar gráficas y dashboards que permitan visualizar tendencias en la generación de residuos peligrosos por tipo, empresa, periodo y región, aportando valor analítico a la gestión ambiental.

Acceso multiusuario en red local: Migrar la base de datos de SQLite a un motor cliente-servidor (como PostgreSQL o MySQL) para soportar acceso concurrente desde múltiples equipos dentro de la red local de la empresa.

Respaldo automático en la nube: Implementar una funcionalidad de respaldo automático periódico de la base de datos hacia un servicio de almacenamiento en la nube (Google Drive, OneDrive), reduciendo el riesgo de pérdida de información.

Mantenimiento preventivo: Establecer un plan de mantenimiento preventivo semestral que incluya actualización de dependencias, revisión de integridad de la base de datos, y ajustes conforme a cambios en la normativa ambiental.

## CONCLUSIONES

El desarrollo e implementación del sistema COA-REPORT permitió alcanzar satisfactoriamente el objetivo general planteado: desarrollar un sistema informático de escritorio para la gestión y generación de reportes de la Cédula de Operación Anual en Ingeniería Ambiental Integral, S.A. de C.V. Los objetivos específicos también fueron cubiertos en su totalidad, desde el análisis del proceso actual hasta la entrega del sistema en producción con documentación completa.

La aplicación de la metodología de desarrollo incremental apoyada en Personal Kanban demostró ser una estrategia adecuada para el contexto de la estadía profesional: permitió mantener entregas funcionales progresivas, facilitar la retroalimentación continua del usuario final y adaptarse a los ajustes de requerimientos identificados durante el desarrollo. Cada incremento fue validado por el encargado ambiental antes de avanzar al siguiente, lo que garantizó que el sistema desarrollado respondiera fielmente a las necesidades reales de la organización.

Desde la perspectiva tecnológica, la combinación de Java 17, JavaFX y SQLite resultó idónea para los requerimientos del proyecto: proporcionó una interfaz gráfica robusta y atractiva, un modelo de datos relacional eficiente y una arquitectura en capas mantenible, todo ello sin costos de licenciamiento y con plena compatibilidad en el entorno Windows de la empresa.

El proyecto representó también una valiosa experiencia de formación profesional integral: la aplicación de conocimientos de análisis de requerimientos, diseño de bases de datos relacionales, programación orientada a objetos, patrones de diseño de software, pruebas funcionales e implementación en entorno real, en un contexto organizacional con problemáticas concretas y usuarios finales con expectativas definidas.

En conclusión, el sistema COA-REPORT constituye una solución tecnológica pertinente, funcional y sostenible que transforma un proceso crítico de gestión ambiental, elevando la eficiencia operativa de Ingeniería Ambiental Integral, S.A. de C.V. y fortaleciendo su capacidad de cumplimiento con la normativa ambiental vigente. El impacto del proyecto trasciende la automatización de tareas repetitivas: sienta las bases de una cultura de gestión de información ambiental más rigurosa, trazable y orientada a la mejora continua.

# REFERENCIAS DE CONSULTA

Elmasri, R., & Navathe, S. (2016). Fundamentals of Database Systems (7th ed.). Pearson.

Pressman, R. S., & Maxim, B. R. (2020). Software Engineering: A Practitioner’s Approach (9th ed.). McGraw-Hill.

Secretaría de Medio Ambiente y Recursos Naturales (SEMARNAT). (2023). Lineamientos para la integración del Registro de Emisiones y Transferencia de Contaminantes.

Sommerville, I. (2011). Software Engineering (9th ed.). Pearson.

Cámara de Diputados del H. Congreso de la Unión. (1988). Ley General del Equilibrio Ecológico y la Protección al Ambiente. Diario Oficial de la Federación (14/08/2015)
