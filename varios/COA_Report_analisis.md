**SISTEMA COA-REPORT**

Ingeniería Ambiental Integral, S.A. de C.V.

*Documento de Análisis y Diseño del Sistema*

| **Campo** | **Detalle** |
| --- | --- |
| Proyecto | COA-REPORT — Sistema de Gestión de Residuos Peligrosos |
| Empresa | Ingeniería Ambiental Integral, S.A. de C.V. |
| Desarrollador | Gutiérrez García Carlos Osvaldo |
| Periodo | Enero – Abril 2026 |
| Tecnología | Java / JavaFX / SQLite |
| Versión del documento | 1.0 |

# **1. LEVANTAMIENTO DE REQUERIMIENTOS**

El levantamiento de requerimientos se realizó mediante reuniones entre el desarrollador y el personal clave de Ingeniería Ambiental Integral, S.A. de C.V., con el objetivo de identificar las necesidades operativas, expectativas funcionales y restricciones tecnológicas para el sistema COA-REPORT.

## **1.1 Contexto Organizacional**

La empresa Ingeniería Ambiental Integral, S.A. de C.V., con sede en Metepec, Estado de México, como actividades pricipales englobla recolección, transportes, coprocesamiento y dispocicion de residuos peligrosos. Como empresa regulada, está obligada a reportar anualmente sus actividades ante la SEMARNAT a través de la Cédula de Operación Anual (COA), instrumento normado por la LGEEPA y el RETC.

El proceso actual involucra el uso de múltiples archivos Excel y registros manuales administrados por un encargado y su asistente, lo que genera riesgos de inconsistencia, pérdida de información y dependencia operativa del personal.

## **1.2 Técnicas de Levantamiento Utilizadas**

* Entrevistas con el responsable del área ambiental y su asistente.
* Revisión y análisis de los archivos Excel actualmente en uso.
* Observación del flujo de trabajo durante el llenado de la COA.
* Revisión del marco normativo (LGEEPA, lineamientos SEMARNAT/RETC).

## **1.3 Requerimientos Funcionales**

Los requerimientos funcionales describen las capacidades específicas que el sistema debe ofrecer al usuario:

| **ID** | **Módulo** | **Descripción del Requerimiento** | **Prioridad** |
| --- | --- | --- | --- |
| RF-01 | Autenticación | El sistema debe permitir el inicio de sesión con usuario y contraseña, diferenciando roles: Administrador y Usuario estándar. | Alta |
| RF-02 | Gestión de Manifiestos | Registrar, consultar, actualizar y eliminar manifiestos de residuos peligrosos con todos sus campos. | Alta |
| RF-03 | Importación Excel | Importar datos de manifiestos desde archivos .xlsx con la estructura definida por la empresa. | Alta |
| RF-04 | Gestión de Empresas | CRUD de empresas generadoras, transportadoras y destinatarios finales. | Media |
| RF-05 | Gestión de Residuos | Catálogo de tipos de residuos con nombre, código y unidades de medida. | Media |
| RF-06 | Reportes COA | Generar reportes estructurados para la COA filtrables por año, empresa y tipo de residuo. | Alta |
| RF-07 | Historial | Mantener registro histórico de todos los movimientos ingresados por periodo anual. | Alta |
| RF-08 | Respaldo | Exportar respaldo de la base de datos SQLite de forma manual. | Baja |

## **1.4 Requerimientos No Funcionales**

| **ID** | **Categoría** | **Descripción** |
| --- | --- | --- |
| RNF-01 | Usabilidad | Interfaz gráfica intuitiva desarrollada con JavaFX, con formularios claros y validaciones visuales. |
| RNF-02 | Rendimiento | El sistema debe responder a consultas en menos de 2 segundos para volúmenes de hasta 10,000 registros. |
| RNF-03 | Seguridad | Contraseñas almacenadas con hash. Control de acceso por roles. Protección del archivo SQLite. |
| RNF-04 | Portabilidad | Ejecutable en Windows mediante JVM sin necesidad de instalación de servidor de base de datos. |
| RNF-05 | Mantenibilidad | Arquitectura en capas (MVC + DAO) que facilite modificaciones y extensiones futuras. |
| RNF-06 | Disponibilidad | Sistema monousuario de escritorio, disponible 100% en modo offline. |

## **1.5 Requerimientos Técnicos**

| **Componente** | **Especificación** |
| --- | --- |
| Sistema Operativo | Windows 10 / 11 (64 bits) |
| Lenguaje de programación | Java 17 (LTS) |
| Framework UI | JavaFX 17 |
| Base de datos | SQLite 3.x (embebida, sin servidor) |
| IDE de desarrollo | Eclipse IDE |
| Gestión de dependencias | Apache Maven |
| Diseño de interfaces | SceneBuilder |
| Hardware mínimo | 4 GB RAM, procesador dual-core, 500 MB de almacenamiento |

## **1.6 Requerimientos Humanos**

* 1 desarrollador de software (estadía profesional) para diseño, desarrollo y pruebas.
* 1 encargado ambiental como usuario principal y fuente de requerimientos del negocio.
* 1 asistente administrativo como usuario secundario y validador de flujos de datos.

## **1.7 Estudio de Factibilidad**

| **Dimensión** | **Análisis** | **Resultado** |
| --- | --- | --- |
| Técnica | Uso de Java/JavaFX/SQLite, tecnologías dominadas por el desarrollador. Herramientas de código abierto disponibles. | Factible |
| Económica | Sin costo de licencias (software libre). Inversión: tiempo del desarrollador en periodo de estadía. | Factible |
| Operativa | El personal actual puede operar el sistema tras una breve capacitación. Mejora del flujo existente. | Factible |
| Temporal | El periodo enero–abril 2026 es suficiente para un sistema modular con entregas incrementales. | Factible |

# **2. ANÁLISIS DEL PROCESO ACTUAL COA**

El análisis del proceso actual permite identificar con precisión los puntos de dolor, ineficiencias y oportunidades de mejora que el sistema COA-REPORT debe resolver.

## **2.1 Descripción del Proceso Actual**

El proceso de elaboración de la COA en Ingeniería Ambiental Integral se puede describir en las siguientes etapas:

| **Etapa** | **Actividad** | **Responsable** | **Herramienta** |
| --- | --- | --- | --- |
| 1 | Recopilación de manifiestos de residuos de clientes durante el año. | Asistente | Archivos físicos / correo |
| 2 | Captura manual de datos en hojas de cálculo Excel por manifiesto. | Asistente | Microsoft Excel |
| 3 | Verificación y validación de datos por el encargado ambiental. | Encargado | Microsoft Excel |
| 4 | Consolidación de datos en un archivo Excel maestro anual. | Encargado | Microsoft Excel |
| 5 | Generación del reporte COA según formato SEMARNAT/RETC. | Encargado | Excel / Formato manual |
| 6 | Revisión final y envío a SEMARNAT en los plazos establecidos. | Encargado | Sistema SEMARNAT |

## **2.2 Diagrama del Flujo Actual (AS-IS)**

El flujo actual presenta una estructura lineal y altamente dependiente de intervención manual en cada etapa:

| **Paso** | **Acción** | **Problema Identificado** |
| --- | --- | --- |
| 1. Recepción | El asistente recibe manifiestos en papel o digital. | No existe un repositorio centralizado. Los documentos pueden extraviarse. |
| 2. Captura | Datos transcritos manualmente a Excel. | Alto tiempo invertido. Errores tipográficos frecuentes. Sin validaciones automáticas. |
| 3. Consolidación | Un archivo Excel acumula todos los registros del año. | Archivos de gran tamaño, lentos y propensos a corrupción. |
| 4. Reporte | El encargado compila el reporte COA manualmente. | Proceso repetitivo y susceptible a omisiones. Sin trazabilidad de cambios. |
| 5. Archivo | Documentos guardados en carpetas locales por año. | Sin respaldo sistemático. Acceso limitado a una sola persona. |

## **2.3 Problemáticas Identificadas**

* Fragmentación de la información: Los datos se distribuyen en múltiples archivos sin un esquema relacional, dificultando la trazabilidad.
* Dependencia del personal clave: El proceso recae principalmente en el encargado, representando un riesgo operativo ante ausencias.
* Ausencia de validaciones: Los datos se capturan sin reglas de integridad, generando inconsistencias detectadas tardíamente.
* Dificultad para consultas históricas: Recuperar información de años anteriores requiere abrir y revisar múltiples archivos Excel.
* Alto tiempo operativo: La elaboración de la COA implica semanas de trabajo manual de consolidación y verificación.
* Sin control de versiones: Los cambios en los archivos no quedan registrados, dificultando auditorías o correcciones.

## **2.4 Proceso Propuesto (TO-BE)**

El sistema COA-REPORT transforma el flujo de trabajo de la siguiente manera:

| **Etapa** | **Proceso Actual** | **Proceso con COA-REPORT** |
| --- | --- | --- |
| Captura de datos | Transcripción manual a Excel por cada manifiesto. | Importación directa desde Excel o registro en formulario estructurado. |
| Almacenamiento | Archivos Excel dispersos en carpetas locales. | Base de datos SQLite centralizada con estructura relacional. |
| Validación | Revisión visual manual sin reglas automáticas. | Validaciones en formulario y restricciones de integridad en BD. |
| Consultas | Apertura de archivos Excel, búsqueda manual. | Búsqueda y filtrado dinámico por múltiples criterios. |
| Reportes COA | Compilación manual en formato Excel. | Generación automática de reportes estructurados por periodo. |
| Historial | Carpetas por año, acceso lento. | Consulta integrada de históricos desde la aplicación. |

## **2.5 Indicadores de Mejora Esperados**

| **Indicador** | **Situación Actual** | **Meta con COA-REPORT** |
| --- | --- | --- |
| Tiempo de captura por manifiesto | ~15 min (manual) | ~3 min (importación / formulario) |
| Tiempo de generación de reporte COA | 1–2 semanas | < 1 hora |
| Errores de captura | Frecuentes (sin validación) | Reducción > 80% (validaciones automáticas) |
| Acceso a datos históricos | Minutos-horas | Segundos |
| Dependencia de personal | Alta (1 encargado) | Media (sistema documentado y multiusuario) |

# **3. DISEÑO DE ARQUITECTURA DEL SISTEMA**

El sistema COA-REPORT se diseña bajo una arquitectura en capas (Layered Architecture) con patrón MVC (Modelo-Vista-Controlador) complementado con el patrón de acceso a datos DAO (Data Access Object). Esta estructura garantiza la separación de responsabilidades, facilitando el mantenimiento y la extensibilidad del sistema.

## **3.1 Visión General de la Arquitectura**

| **Capa** | **Tecnología** | **Responsabilidad** |
| --- | --- | --- |
| Presentación (Vista) | JavaFX + FXML + CSS | Interfaz gráfica. Formularios, tablas, menús y notificaciones al usuario. |
| Controladores | Java (Controllers) | Gestión de eventos de UI. Invocación de servicios y lógica de negocio. |
| Lógica de Negocio (Servicios) | Java (Service Layer) | Reglas de negocio: validaciones, cálculos, transformaciones de datos. |
| Acceso a Datos (DAO) | Java + JDBC | Operaciones CRUD sobre la base de datos. Abstracción del motor SQLite. |
| Persistencia | SQLite 3.x | Almacenamiento relacional local en archivo .db. |
| Utilidades | Apache POI / Java IO | Importación de Excel, exportación de reportes, gestión de archivos. |

## **3.2 Estructura de Paquetes (Maven / Java)**

La organización de paquetes sigue las convenciones de Maven con arquitectura modular:

| **Paquete** | **Contenido** |
| --- | --- |
| com.coareport.app | Clase principal Main.java. Inicialización de JavaFX y base de datos. |
| com.coareport.model | Clases POJO/Entity: Manifiesto, Empresa, Residuo, Usuario, etc. |
| com.coareport.dao | Interfaces DAO y sus implementaciones JDBC: ManifiestoDAO, EmpresaDAO, etc. |
| com.coareport.service | Servicios de negocio: ManifiestoService, ReporteService, ImportService. |
| com.coareport.controller | Controladores JavaFX vinculados a cada vista FXML. |
| com.coareport.util | Utilidades: ConexionDB, ExcelImporter, ReportGenerator, HashUtil. |
| resources/fxml | Archivos de interfaz: main.fxml, manifiestos.fxml, reportes.fxml, etc. |
| resources/css | Hojas de estilo: styles.css con tema verde corporativo. |

## **3.3 Componentes Principales del Sistema**

### **3.3.1 Módulo de Autenticación**

* Pantalla de login con campos usuario/contraseña.
* Validación contra tabla USUARIOS en SQLite (contraseña con hash SHA-256).
* Control de sesión activa con rol asignado (ADMIN / USUARIO).
* Bloqueo tras 3 intentos fallidos consecutivos.

### **3.3.2 Módulo de Manifiestos**

* Formulario de registro con todos los campos del Excel de la empresa.
* Importación masiva desde archivo .xlsx mediante Apache POI.
* Tabla de consulta con filtros por empresa, fecha, tipo de residuo y NRA.
* Edición y eliminación con confirmación de usuario.

### **3.3.3 Módulo de Catálogos**

* CRUD de Empresas (generadoras, transportadoras, destinatarios).
* CRUD de Tipos de Residuos con clave CRETIB y unidades de medida.
* CRUD de Encargados y Usuarios del sistema.

### **3.3.4 Módulo de Reportes**

* Generación de reporte anual COA filtrado por año y empresa.
* Exportación a Excel (.xlsx) con formato tabular estructurado.
* Vista previa de datos antes de exportar.
* Estadísticas: totales por tipo de residuo, empresa y periodo.

## **3.4 Flujo de Navegación del Sistema**

| **Vista** | **Acceso desde** | **Funcionalidad Principal** |
| --- | --- | --- |
| Login | Inicio del sistema | Autenticación de usuario |
| Dashboard / Menú principal | Post-login | Navegación a todos los módulos |
| Manifiestos | Menú principal | Registro, importación y consulta de manifiestos |
| Empresas | Menú > Catálogos | Gestión de empresas generadoras y transportadoras |
| Residuos | Menú > Catálogos | Catálogo de tipos de residuos (CRETIB) |
| Reportes COA | Menú principal | Generación y exportación de reportes |
| Usuarios | Menú > Administración (solo ADMIN) | Gestión de accesos al sistema |
| Respaldo | Menú > Administración (solo ADMIN) | Exportar copia de base de datos |

## **3.5 Patrones de Diseño Aplicados**

| **Patrón** | **Aplicación en COA-REPORT** |
| --- | --- |
| MVC (Model-View-Controller) | Separación entre modelos de datos (POJO), vistas FXML y controladores Java. |
| DAO (Data Access Object) | Interfaces DAO independientes del motor de BD; implementación concreta con SQLite/JDBC. |
| Singleton | Clase ConexionDB garantiza una única conexión activa a SQLite durante la sesión. |
| Factory | Creación de objetos de dominio desde ResultSet de JDBC en las clases DAO. |
| Service Layer | Capa intermedia entre controladores y DAO que centraliza reglas de negocio y validaciones. |

# **4. DISEÑO DE BASE DE DATOS (SQLite)**

El diseño de la base de datos se basa en la estructura de datos operativa de la empresa (campos del Excel de manifiestos) y en los requerimientos funcionales del sistema. Se aplican principios de normalización hasta la Tercera Forma Normal (3FN) para garantizar integridad y eliminar redundancias.

## **4.1 Entidades del Modelo Relacional**

A partir de los campos del Excel definido (N° de manifiesto, empresa, residuo, CRETIB, cantidad, unidad volumen/peso, fecha de recolección, fecha de acopio, NRA, empresa transportadora, destino final, encargado) se identifican las siguientes entidades:

| **Entidad** | **Descripción** | **Relación Principal** |
| --- | --- | --- |
| USUARIOS | Usuarios del sistema con roles de acceso. | — |
| EMPRESAS | Empresas generadoras, transportadoras o destinatarias. | Manifiesto (N:1) |
| RESIDUOS | Catálogo de tipos de residuos peligrosos con clasificación CRETIB. | Manifiesto (N:1) |
| ENCARGADOS | Personal responsable del manifiesto. | Manifiesto (N:1) |
| MANIFIESTOS | Registro principal de cada manifiesto de residuos peligrosos. | Entidad central |

## **4.2 Diccionario de Datos**

### **Tabla: USUARIOS**

| **Campo** | **Tipo** | **Restricción** | **Descripción** |
| --- | --- | --- | --- |
| id\_usuario | INTEGER | PK, AUTOINCREMENT | Identificador único del usuario |
| nombre\_usuario | TEXT | NOT NULL, UNIQUE | Nombre de inicio de sesión |
| contrasena\_hash | TEXT | NOT NULL | Contraseña cifrada con SHA-256 |
| rol | TEXT | NOT NULL, CHECK (ADMIN|USUARIO) | Rol del usuario en el sistema |
| activo | INTEGER | DEFAULT 1 | Estado: 1=activo, 0=inactivo |
| fecha\_creacion | TEXT | NOT NULL | Fecha de registro (ISO 8601) |

### **Tabla: EMPRESAS**

| **Campo** | **Tipo** | **Restricción** | **Descripción** |
| --- | --- | --- | --- |
| id\_empresa | INTEGER | PK, AUTOINCREMENT | Identificador único de la empresa |
| nombre | TEXT | NOT NULL | Razón social o nombre comercial |
| rfc | TEXT | UNIQUE | RFC de la empresa |
| tipo | TEXT | NOT NULL | Tipo: GENERADORA | TRANSPORTADORA | DESTINO\_FINAL |
| contacto | TEXT |  | Nombre del contacto principal |
| telefono | TEXT |  | Teléfono de contacto |
| direccion | TEXT |  | Dirección completa |
| activo | INTEGER | DEFAULT 1 | Estado del registro |

### **Tabla: RESIDUOS**

| **Campo** | **Tipo** | **Restricción** | **Descripción** |
| --- | --- | --- | --- |
| id\_residuo | INTEGER | PK, AUTOINCREMENT | Identificador único del tipo de residuo |
| nombre | TEXT | NOT NULL | Nombre descriptivo del residuo peligroso |
| clave\_cretib | TEXT | NOT NULL | Clasificación CRETIB (Ej: C, R, E, T, I, B) |
| unidad\_medida | TEXT | NOT NULL | Unidad: KG | LT | TON | M3 |
| descripcion | TEXT |  | Descripción adicional del residuo |
| activo | INTEGER | DEFAULT 1 | Estado del registro en catálogo |

### **Tabla: ENCARGADOS**

| **Campo** | **Tipo** | **Restricción** | **Descripción** |
| --- | --- | --- | --- |
| id\_encargado | INTEGER | PK, AUTOINCREMENT | Identificador único del encargado |
| nombre\_completo | TEXT | NOT NULL | Nombre completo del encargado responsable |
| cargo | TEXT |  | Puesto o cargo dentro de la empresa |
| empresa\_id | INTEGER | FK -> EMPRESAS(id\_empresa) | Empresa a la que pertenece el encargado |
| activo | INTEGER | DEFAULT 1 | Estado del registro |

### **Tabla: MANIFIESTOS (Tabla central)**

Esta tabla concentra todos los campos del Excel operativo de la empresa:

| **Campo** | **Tipo** | **Restricción** | **Campo Excel Origen** |
| --- | --- | --- | --- |
| id\_manifiesto | INTEGER | PK, AUTOINCREMENT | — |
| num\_manifiesto | TEXT | NOT NULL, UNIQUE | N° de manifiesto |
| id\_empresa\_generadora | INTEGER | FK -> EMPRESAS(id\_empresa), NOT NULL | Empresa |
| id\_residuo | INTEGER | FK -> RESIDUOS(id\_residuo), NOT NULL | Residuo |
| cretib | TEXT | NOT NULL | CRETIB |
| cantidad | REAL | NOT NULL, CHECK (> 0) | Cantidad |
| unidad | TEXT | NOT NULL | Unidad volumen/peso |
| fecha\_recoleccion | TEXT | NOT NULL | Fecha de recolección |
| fecha\_acopio | TEXT |  | Fecha de acopio |
| nra | TEXT |  | NRA |
| id\_empresa\_transportadora | INTEGER | FK -> EMPRESAS(id\_empresa) | Empresa transportadora |
| destino\_final | TEXT | NOT NULL | Destino final |
| id\_encargado | INTEGER | FK -> ENCARGADOS(id\_encargado) | Encargado |
| observaciones | TEXT |  | (campo adicional del sistema) |
| fecha\_registro | TEXT | NOT NULL, DEFAULT CURRENT\_TIMESTAMP | (generado por sistema) |
| id\_usuario\_registro | INTEGER | FK -> USUARIOS(id\_usuario) | (auditoría del sistema) |

## **4.3 Relaciones del Modelo (Diagrama Entidad-Relación)**

Las relaciones entre entidades son las siguientes:

* EMPRESAS (1) ----< MANIFIESTOS (N): Una empresa generadora puede tener múltiples manifiestos. FK: id\_empresa\_generadora.
* EMPRESAS (1) ----< MANIFIESTOS (N): Una empresa transportadora puede aparecer en múltiples manifiestos. FK: id\_empresa\_transportadora.
* RESIDUOS (1) ----< MANIFIESTOS (N): Un tipo de residuo puede aparecer en múltiples manifiestos. FK: id\_residuo.
* ENCARGADOS (1) ----< MANIFIESTOS (N): Un encargado puede ser responsable de múltiples manifiestos. FK: id\_encargado.
* USUARIOS (1) ----< MANIFIESTOS (N): Un usuario registra múltiples manifiestos (auditoría). FK: id\_usuario\_registro.
* EMPRESAS (1) ----< ENCARGADOS (N): Una empresa puede tener múltiples encargados. FK: empresa\_id.

## **4.4 Scripts DDL de Creación (SQLite)**

A continuación se presentan los scripts SQL para la creación de las tablas en SQLite:

| **Script DDL — Base de datos: coareport.db** |
| --- |
| CREATE TABLE IF NOT EXISTS USUARIOS ( id\_usuario INTEGER PRIMARY KEY AUTOINCREMENT, nombre\_usuario TEXT NOT NULL UNIQUE, contrasena\_hash TEXT NOT NULL, rol TEXT NOT NULL CHECK (rol IN ('ADMIN','USUARIO')), activo INTEGER NOT NULL DEFAULT 1, fecha\_creacion TEXT NOT NULL DEFAULT (datetime('now','localtime')) ); |
| CREATE TABLE IF NOT EXISTS EMPRESAS ( id\_empresa INTEGER PRIMARY KEY AUTOINCREMENT, nombre TEXT NOT NULL, rfc TEXT UNIQUE, tipo TEXT NOT NULL CHECK (tipo IN ('GENERADORA','TRANSPORTADORA','DESTINO\_FINAL')), contacto TEXT, telefono TEXT, direccion TEXT, activo INTEGER NOT NULL DEFAULT 1 ); |
| CREATE TABLE IF NOT EXISTS RESIDUOS ( id\_residuo INTEGER PRIMARY KEY AUTOINCREMENT, nombre TEXT NOT NULL, clave\_cretib TEXT NOT NULL, unidad\_medida TEXT NOT NULL CHECK (unidad\_medida IN ('KG','LT','TON','M3')), descripcion TEXT, activo INTEGER NOT NULL DEFAULT 1 ); |
| CREATE TABLE IF NOT EXISTS ENCARGADOS ( id\_encargado INTEGER PRIMARY KEY AUTOINCREMENT, nombre\_completo TEXT NOT NULL, cargo TEXT, empresa\_id INTEGER REFERENCES EMPRESAS(id\_empresa), activo INTEGER NOT NULL DEFAULT 1 ); |
| CREATE TABLE IF NOT EXISTS MANIFIESTOS ( id\_manifiesto INTEGER PRIMARY KEY AUTOINCREMENT, num\_manifiesto TEXT NOT NULL UNIQUE, id\_empresa\_generadora INTEGER NOT NULL REFERENCES EMPRESAS(id\_empresa), id\_residuo INTEGER NOT NULL REFERENCES RESIDUOS(id\_residuo), cretib TEXT NOT NULL, cantidad REAL NOT NULL CHECK (cantidad > 0), unidad TEXT NOT NULL, fecha\_recoleccion TEXT NOT NULL, fecha\_acopio TEXT, nra TEXT, id\_empresa\_transportadora INTEGER REFERENCES EMPRESAS(id\_empresa), destino\_final TEXT NOT NULL, id\_encargado INTEGER REFERENCES ENCARGADOS(id\_encargado), observaciones TEXT, fecha\_registro TEXT NOT NULL DEFAULT (datetime('now','localtime')), id\_usuario\_registro INTEGER REFERENCES USUARIOS(id\_usuario) ); |
| -- Índices para mejorar rendimiento de consultas frecuentes CREATE INDEX IF NOT EXISTS idx\_manifest\_fecha ON MANIFIESTOS(fecha\_recoleccion); CREATE INDEX IF NOT EXISTS idx\_manifest\_empresa ON MANIFIESTOS(id\_empresa\_generadora); CREATE INDEX IF NOT EXISTS idx\_manifest\_residuo ON MANIFIESTOS(id\_residuo); CREATE INDEX IF NOT EXISTS idx\_manifest\_num ON MANIFIESTOS(num\_manifiesto); |

## **4.5 Consultas SQL Clave**

| **Consulta** | **Descripción** |
| --- | --- |
| SELECT M.num\_manifiesto, EG.nombre AS empresa, R.nombre AS residuo, M.cretib, M.cantidad, M.unidad, M.fecha\_recoleccion, M.fecha\_acopio, M.nra, ET.nombre AS transportadora, M.destino\_final, EN.nombre\_completo AS encargado FROM MANIFIESTOS M JOIN EMPRESAS EG ON M.id\_empresa\_generadora = EG.id\_empresa JOIN RESIDUOS R ON M.id\_residuo = R.id\_residuo LEFT JOIN EMPRESAS ET ON M.id\_empresa\_transportadora = ET.id\_empresa LEFT JOIN ENCARGADOS EN ON M.id\_encargado = EN.id\_encargado WHERE strftime('%Y', M.fecha\_recoleccion) = ? ORDER BY M.fecha\_recoleccion; | Reporte COA completo por año: obtiene todos los campos del manifiesto con nombres descriptivos para exportación. |
| SELECT R.nombre, R.clave\_cretib, SUM(M.cantidad) AS total, M.unidad FROM MANIFIESTOS M JOIN RESIDUOS R ON M.id\_residuo = R.id\_residuo WHERE strftime('%Y', M.fecha\_recoleccion) = ? GROUP BY M.id\_residuo, M.unidad ORDER BY total DESC; | Resumen estadístico: totales de residuo por tipo para el año seleccionado. |

## **4.6 Consideraciones de Integridad y Seguridad**

* Integridad referencial: Habilitada con PRAGMA foreign\_keys = ON al iniciar conexión.
* Restricciones CHECK: Aplicadas en campos críticos como rol, tipo de empresa, unidad de medida y cantidad.
* Contraseñas: Almacenadas únicamente como hash SHA-256, nunca en texto plano.
* Respaldo: La base de datos es un único archivo .db que puede copiarse para respaldo. El sistema incluirá opción de exportar copia.
* Auditoría: El campo id\_usuario\_registro en MANIFIESTOS permite rastrear qué usuario registró cada entrada.
* Soft delete: Uso del campo activo=0 en lugar de eliminación física, preservando integridad histórica.

*Documento elaborado para el proyecto COA-REPORT — Ingeniería Ambiental Integral, S.A. de C.V. — 2026*