**MÓDULO 1. PLANTEAMIENTO DEL PROBLEMA**

**Planteamiento del problema para el desarrollo de un asistente local de inteligencia artificial para la comercialización de productos en PVC**

# 1. Introducción

La comercialización de productos fabricados o distribuidos en policloruro de vinilo (PVC) requiere comunicar información confiable acerca de características, especificaciones, usos, condiciones de instalación, calidad y recomendaciones técnicas. En este tipo de actividad, la atención comercial no se limita a presentar un producto o gestionar una venta: también implica comprender la necesidad del cliente, identificar la referencia adecuada y ofrecer información coherente con la documentación técnica disponible. La precisión de estas respuestas contribuye a generar confianza y a reducir errores derivados de interpretaciones incompletas.

En las organizaciones, parte de este conocimiento suele encontrarse distribuido entre fichas técnicas, manuales de calidad, procedimientos internos y otros documentos. Cuando los archivos se almacenan en distintas carpetas, presentan formatos heterogéneos o no cuentan con una clasificación uniforme, localizar un dato específico puede demandar tiempo y depender de la experiencia de determinados trabajadores. Esta situación puede dificultar la continuidad de la atención, especialmente cuando se presentan consultas frecuentes o se requiere contrastar información de varias fuentes.

Los modelos de inteligencia artificial generativa ofrecen posibilidades para consultar documentos mediante lenguaje natural y sintetizar información relevante. Sin embargo, una solución basada exclusivamente en un modelo generativo puede producir respuestas plausibles que no estén respaldadas por la documentación institucional. Por ello, se propone desarrollar un asistente local que combine un modelo de lenguaje con mecanismos de recuperación de información documental, de modo que las respuestas se apoyen en fuentes autorizadas y permitan identificar su procedencia. Los sistemas de generación aumentada por recuperación (RAG) integran un modelo generativo con una fuente externa recuperable, lo que facilita consultar y actualizar conocimiento documental sin depender únicamente de la memoria paramétrica del modelo (Lewis et al., 2020).

El carácter local de la solución constituye una condición central del proyecto. La información corporativa deberá permanecer en infraestructura controlada o procesarse mediante mecanismos expresamente autorizados, evitando que documentos internos sean compartidos con servicios públicos o proveedores externos sin aprobación. Este principio no elimina por sí solo todos los riesgos de seguridad; requiere controles de acceso, administración documental, registro de actividad, evaluación de respuestas y supervisión humana. En consecuencia, el proyecto se plantea como una herramienta de apoyo a la gestión del conocimiento comercial y técnico, no como sustituto de la responsabilidad de los trabajadores.

# 2. Planteamiento del problema

La atención comercial de productos en PVC puede requerir consultar con rapidez especificaciones, condiciones de calidad, procedimientos y recomendaciones técnicas. Cuando estos contenidos se encuentran en documentos separados o su organización no facilita una búsqueda directa, el personal debe localizar manualmente los archivos, revisar distintas secciones y verificar si la información corresponde a la versión vigente. El problema no consiste necesariamente en la ausencia de conocimiento, sino en la dificultad para recuperarlo de forma oportuna, consistente y verificable.

La búsqueda manual puede incrementar el tiempo dedicado a responder preguntas y reducir el tiempo disponible para otras actividades comerciales. Además, si la respuesta depende del conocimiento de una persona experta, su disponibilidad puede convertirse en un factor limitante. La consulta informal entre compañeros puede resolver casos puntuales, pero no garantiza que todos utilicen el mismo criterio ni que la información transmitida corresponda a la documentación autorizada.

Otra dificultad se relaciona con la vigencia y exactitud de las respuestas. Una ficha técnica desactualizada, un procedimiento reemplazado o una interpretación incompleta puede llevar a comunicar características incorrectas al cliente. En un contexto comercial, estas inconsistencias pueden generar reprocesos, expectativas inadecuadas o pérdida de confianza. Por tanto, no basta con acelerar la búsqueda: también es necesario identificar la fuente consultada, conservar el contexto documental y reconocer cuándo la evidencia disponible no permite responder.

El uso de herramientas públicas de inteligencia artificial introduce un riesgo adicional cuando se copian en ellas documentos internos, información de clientes, condiciones comerciales u otros datos sensibles. Dependiendo de las condiciones del servicio y de su configuración, el contenido podría salir del entorno controlado por la organización. Por esa razón, la solución debe priorizar la ejecución local y establecer restricciones verificables para impedir transferencias no autorizadas. La protección de la información requiere abordar conjuntamente tecnología, procedimientos y responsabilidades, de acuerdo con un enfoque de gestión de riesgos como el promovido por NIST (Tabassi, 2023).

En este contexto, se identifica la necesidad de una herramienta que centralice el acceso al conocimiento documental autorizado, permita formular consultas en lenguaje natural y genere respuestas sustentadas en las fuentes disponibles. El asistente deberá reconocer los límites de la evidencia, indicar los documentos utilizados y facilitar la actualización o retiro de contenidos obsoletos. Su implementación debe acompañarse de controles de seguridad y criterios de evaluación que permitan comprobar si realmente mejora la consulta sin comprometer la confidencialidad.

# 3. Formulación del problema

¿Cómo puede un asistente local de inteligencia artificial facilitar la consulta segura de manuales de calidad, procedimientos y fichas técnicas para apoyar la comercialización de productos en PVC, sin exponer información interna de la organización?

A partir de esta pregunta central, se plantean las siguientes preguntas secundarias:

- ¿Qué mecanismos de recuperación y presentación de fuentes permiten que los asesores comerciales localicen información pertinente y verifiquen su origen?

- ¿Cómo se puede evaluar la precisión, integridad y vigencia de las respuestas generadas a partir de documentos autorizados?

- ¿Qué controles de acceso, registro y operación local son necesarios para reducir el riesgo de exposición de información interna?

- ¿Qué criterios de usabilidad y desempeño permitirían determinar si el asistente reduce el esfuerzo de búsqueda y resulta útil para los usuarios?

- ¿Cómo deben identificarse y gestionarse los riesgos asociados con alucinaciones, documentos obsoletos, accesos indebidos y dependencia excesiva del sistema?

# 4. Justificación

Desde la perspectiva técnica, el proyecto permite integrar modelos de lenguaje, recuperación documental y una interfaz de consulta en una aplicación orientada a una necesidad concreta. La arquitectura propuesta deberá separar el motor de inferencia, la base de conocimiento y la interfaz, de forma que cada componente pueda evaluarse y mantenerse. La recuperación aumentada por generación puede apoyar respuestas fundamentadas en fragmentos documentales relevantes, aunque su desempeño dependerá de la calidad de los documentos, la estrategia de fragmentación, la recuperación y la validación de las respuestas (Lewis et al., 2020).

En el plano operativo, se espera reducir el tiempo necesario para localizar datos técnicos y disminuir la dependencia de búsquedas manuales o consultas reiteradas a personal especializado. El asistente podría servir como primer punto de consulta para asesores comerciales, manteniendo la posibilidad de escalar preguntas complejas al personal técnico o de calidad. La herramienta debe presentar sus resultados como apoyo y no como autorización automática para emitir compromisos comerciales o recomendaciones que requieran aprobación experta.

En el ámbito comercial, la disponibilidad de respuestas consistentes y acompañadas de referencias documentales puede favorecer una comunicación más clara con clientes y prospectos. El sistema podría ayudar a identificar las características de un producto, consultar especificaciones y orientar al asesor hacia el documento pertinente. Estos beneficios son esperados y deberán comprobarse mediante pruebas con consultas representativas y evaluación de usuarios; no se asume de antemano una reducción cuantificada del tiempo ni un aumento de ventas.

En materia de seguridad, la operación local y el control sobre las fuentes documentales buscan limitar la exposición de información interna. La norma ISO/IEC 27001:2022 presenta un marco de requisitos para establecer y mejorar un sistema de gestión de seguridad de la información, incluyendo la evaluación y tratamiento de riesgos (International Organization for Standardization & International Electrotechnical Commission, 2022). El proyecto no implica afirmar que la solución estará certificada bajo esta norma; se adopta como referencia general para considerar confidencialidad, integridad, disponibilidad y gestión de riesgos.

Finalmente, la pertinencia académica radica en aplicar principios de ingeniería de software e inteligencia artificial responsable a un problema delimitado. La definición inicial de usuarios, requisitos, métricas y riesgos facilita orientar el diseño posterior y evita reducir el proyecto a una interfaz conversacional sin evaluación. El NIST AI RMF propone organizar la gestión del riesgo mediante las funciones Govern, Map, Measure y Manage, que pueden incorporarse desde la concepción hasta la operación del sistema (Tabassi, 2023).

# 5. Usuarios y partes interesadas

| **Usuario o parte interesada**   | **Rol en el sistema**                                                   | **Necesidad principal**                                                        | **Beneficio esperado**                                                             |
|----------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Asesores comerciales             | Usuarios principales; consultan información para orientar al cliente.   | Obtener respuestas rápidas, claras y respaldadas por documentos autorizados.   | Menor esfuerzo de búsqueda y mayor consistencia en la atención.                    |
| Clientes o prospectos            | Beneficiarios indirectos; reciben información comunicada por el asesor. | Recibir información técnica comprensible y coherente.                          | Orientación más clara; la respuesta final seguirá bajo responsabilidad del asesor. |
| Personal técnico o de calidad    | Valida documentos, especificaciones y respuestas críticas.              | Mantener fuentes vigentes y resolver consultas que requieren criterio experto. | Menos consultas repetitivas y mayor control documental.                            |
| Área administrativa              | Apoya la gestión de documentos y procesos internos.                     | Contar con reglas para aprobar, actualizar y retirar archivos.                 | Mejor organización y trazabilidad del conocimiento autorizado.                     |
| TI y seguridad de la información | Administra infraestructura, permisos, respaldos y controles.            | Evitar accesos indebidos y transferencias no autorizadas.                      | Mayor control técnico, registros y capacidad de respuesta ante incidentes.         |
| Dirección comercial              | Patrocina y evalúa la utilidad del sistema.                             | Conocer el aporte operativo y los límites de la solución.                      | Información para decidir sobre adopción, mejora y continuidad.                     |

# 6. Alcance del proyecto

## 6.1 Dentro del alcance

- Consulta mediante lenguaje natural de manuales de calidad, procedimientos y fichas técnicas previamente autorizados.

- Procesamiento e indexación de documentos seleccionados, con procedimientos para actualizar, reemplazar o retirar versiones.

- Recuperación de fragmentos pertinentes y generación de respuestas basadas en el contenido documental disponible.

- Presentación de la fuente utilizada, como nombre del documento y ubicación o sección identificable cuando el formato lo permita.

- Operación local o en infraestructura controlada, con medidas que impidan enviar información sensible a servicios externos sin autorización.

- Control de acceso por roles o perfiles, registro básico de consultas relevantes y documentación de controles.

- Evaluación del sistema mediante un conjunto de preguntas de prueba, revisión de respuestas y retroalimentación de usuarios.

## 6.2 Fuera del alcance

- Automatización de pedidos, facturación, pagos, despacho o administración de inventarios.

- Reemplazo del personal comercial, técnico, de calidad o de seguridad de la información.

- Acceso a documentos o sistemas para los que el usuario no tenga autorización.

- Envío de documentos confidenciales a modelos públicos en la nube sin aprobación expresa y controles formales.

- Integración con CRM, ERP, correo, plataformas de terceros u otros sistemas externos no aprobados.

- Emisión autónoma de compromisos contractuales, precios definitivos o dictámenes técnicos que requieran validación humana.

Se asume, para la formulación inicial, que la organización podrá seleccionar un conjunto de documentos digitales autorizados y designar responsables para validar su vigencia. Esta suposición deberá confirmarse durante el levantamiento de requisitos. La disponibilidad de hardware, formatos documentales y perfiles definitivos de acceso se determinará en una fase posterior.

# 7. Requisitos del sistema

## 7.1 Requisitos funcionales

| **Código** | **Requisito**                                                                                                                                                   |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RF-01      | El sistema permitirá formular consultas sobre los documentos autorizados mediante lenguaje natural.                                                             |
| RF-02      | El sistema permitirá recuperar información de manuales de calidad, procedimientos y fichas técnicas incorporados a la base de conocimiento.                     |
| RF-03      | El sistema generará respuestas fundamentadas en los fragmentos recuperados y evitará presentar como confirmados datos que no estén respaldados por las fuentes. |
| RF-04      | El sistema mostrará la fuente documental asociada a cada respuesta, siempre que exista evidencia recuperada suficiente.                                         |
| RF-05      | El sistema permitirá a usuarios autorizados cargar, actualizar, reemplazar o retirar documentos de la base de conocimiento.                                     |
| RF-06      | El sistema facilitará la consulta de especificaciones de productos en PVC presentes en las fichas técnicas aprobadas.                                           |
| RF-07      | El sistema registrará consultas relevantes y metadatos mínimos para auditoría, respetando las políticas de privacidad aplicables.                               |
| RF-08      | El sistema restringirá las funciones y documentos disponibles según el perfil de acceso asignado.                                                               |

## 7.2 Requisitos no funcionales

| **Código** | **Requisito**                                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RNF-01     | Seguridad y confidencialidad: los documentos y consultas se procesarán en infraestructura aprobada y no se enviarán a servicios externos sin autorización. |
| RNF-02     | Disponibilidad: el sistema deberá estar disponible durante los periodos de uso definidos, sujeto a la capacidad del equipo y mantenimiento.                |
| RNF-03     | Usabilidad: la interfaz deberá permitir formular preguntas, revisar respuestas y localizar las fuentes sin conocimientos especializados de IA.             |
| RNF-04     | Trazabilidad: las respuestas deberán permitir identificar el documento de respaldo y conservar registros de operación conforme a la política definida.     |
| RNF-05     | Control de acceso: la autenticación y autorización deberán limitar el acceso a usuarios y documentos permitidos.                                           |
| RNF-06     | Escalabilidad razonable: la base documental podrá crecer mediante procesos controlados de ingestión e indexación.                                          |
| RNF-07     | Mantenibilidad: los documentos deberán tener metadatos de versión, fecha de actualización y responsable cuando esta información esté disponible.           |
| RNF-08     | Cumplimiento: el tratamiento de datos, licencias y propiedad intelectual deberá respetar las políticas organizacionales y las normas aplicables.           |

# 8. Criterios de éxito

Los siguientes valores son metas iniciales propuestas para orientar la evaluación del prototipo, no resultados ya obtenidos ni datos históricos de la organización. Deberán revisarse después de construir una línea base con consultas reales autorizadas y acordarse con las partes interesadas.

| **Criterio**              | **Indicador o métrica**                                                                             | **Meta inicial propuesta**                             | **Método de verificación**                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------------------------|
| Respuestas sustentadas    | Porcentaje de respuestas correctas respaldadas por documentos autorizados.                          | Al menos 85 % en un conjunto de prueba aprobado.       | Evaluación experta de preguntas y respuestas contra la documentación.    |
| Tiempo de búsqueda        | Tiempo promedio para resolver una consulta, comparado con búsqueda manual.                          | Reducción de al menos 30 % frente a la línea base.     | Prueba cronometrada con tareas equivalentes y participantes comparables. |
| Satisfacción de usuarios  | Valoración de utilidad y facilidad de uso en escala de 1 a 5.                                       | Promedio igual o superior a 4/5.                       | Encuesta posterior a pruebas de uso.                                     |
| Identificación de fuentes | Porcentaje de respuestas con referencia documental verificable cuando la respuesta está sustentada. | Al menos 95 %.                                         | Revisión de enlaces, nombres de documentos y fragmentos citados.         |
| Exposición de información | Número de incidentes confirmados de transferencia no autorizada de información interna.             | Cero incidentes durante las pruebas controladas.       | Revisión de configuración, tráfico, registros y pruebas de seguridad.    |
| Acceso según rol          | Porcentaje de pruebas de autorización superadas correctamente.                                      | 100 % de los casos definidos en la matriz de permisos. | Pruebas positivas y negativas con perfiles de usuario.                   |
| Vigencia documental       | Porcentaje de documentos del conjunto piloto con estado y versión identificables.                   | Al menos 95 % antes de la evaluación final.            | Auditoría del inventario documental y revisión por responsables.         |

Las metas deberán interpretarse junto con el tamaño y representatividad del conjunto de pruebas. Una cifra agregada no sustituye el análisis de errores críticos: por ejemplo, una respuesta técnicamente incorrecta sobre una especificación relevante debe registrarse y tratarse incluso si el promedio general es satisfactorio.

# 9. Matriz de riesgos basada en NIST AI RMF

El NIST AI Risk Management Framework (AI RMF 1.0) organiza la gestión del riesgo en cuatro funciones: Govern (Gobernar), que establece responsabilidades, políticas y tolerancia al riesgo; Map (Mapear), que caracteriza el contexto, los usuarios, los datos y los impactos posibles; Measure (Medir), que evalúa y monitorea desempeño y riesgos; y Manage (Gestionar), que prioriza riesgos y aplica tratamientos. Estas funciones se complementan y deben considerarse durante todo el ciclo de vida del sistema (Tabassi, 2023). La siguiente matriz constituye una valoración preliminar cualitativa. La probabilidad y el impacto deberán revisarse con evidencia del entorno real.

| **ID** | **Riesgo identificado**                                                       | **Función NIST AI RMF** | **Categoría**             | **Impacto** | **Probabilidad** | **Nivel** | **Estrategia**   | **Control o mitigación propuesta**                                                                                                                                 |
|--------|-------------------------------------------------------------------------------|-------------------------|---------------------------|-------------|------------------|-----------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1     | Exposición de información interna o confidencial.                             | Govern / Manage         | Seguridad y privacidad    | Alto        | Media            | Alto      | Mitigar          | Ejecutar localmente; bloquear telemetría o conexiones no autorizadas; revisar tráfico y configuración; aprobar formalmente cualquier salida de datos.              |
| R2     | Respuestas incorrectas, incompletas o desactualizadas.                        | Measure / Manage        | Calidad y confiabilidad   | Alto        | Media            | Alto      | Mitigar          | Conjunto de pruebas validado por expertos; recuperación de fuentes vigentes; mostrar fecha/versión; permitir abstención y escalamiento.                            |
| R3     | Alucinación o invención de información técnica.                               | Measure / Manage        | Confiabilidad del modelo  | Alto        | Media            | Alto      | Mitigar          | Instrucciones para responder con evidencia; citas verificables; umbral de recuperación; respuesta explícita de insuficiencia; pruebas adversariales.               |
| R4     | Acceso no autorizado a documentos sensibles.                                  | Govern / Map / Manage   | Control de acceso         | Alto        | Baja             | Medio     | Mitigar          | Autenticación, permisos por rol, separación de colecciones, pruebas de acceso negativo y revisión periódica de usuarios.                                           |
| R5     | Falta de trazabilidad del origen de una respuesta.                            | Measure / Manage        | Auditoría y transparencia | Medio       | Media            | Medio     | Mitigar          | Registrar identificadores de documentos y fragmentos recuperados; conservar metadatos de versión y vincular la respuesta con su fuente.                            |
| R6     | Dependencia excesiva del asistente sin validación humana.                     | Govern / Map            | Factor humano y operación | Alto        | Media            | Alto      | Mitigar          | Definir casos que requieren revisión experta; capacitar usuarios; comunicar límites; no permitir que el sistema apruebe compromisos técnicos o comerciales.        |
| R7     | Documentos obsoletos, duplicados o mal categorizados.                         | Map / Measure / Manage  | Gestión documental        | Alto        | Media            | Alto      | Mitigar          | Asignar responsable documental; controlar versiones; detectar duplicados; definir proceso de retiro y verificar vigencia antes de indexar.                         |
| R8     | Baja aceptación o adopción por parte de los usuarios.                         | Map / Measure / Manage  | Usabilidad y cambio       | Medio       | Media            | Medio     | Mitigar          | Involucrar asesores en pruebas; realizar capacitación breve; medir satisfacción; ajustar interfaz y flujo de consulta a partir de retroalimentación.               |
| R9     | Interrupción del servicio o indisponibilidad técnica.                         | Map / Manage            | Disponibilidad            | Medio       | Media            | Medio     | Mitigar          | Monitorear recursos; documentar instalación y recuperación; mantener copias de seguridad de documentos e índices; definir procedimiento manual alternativo.        |
| R10    | Incumplimiento de políticas de seguridad, privacidad o propiedad intelectual. | Govern / Map / Manage   | Cumplimiento y gobernanza | Alto        | Baja             | Medio     | Evitar / Mitigar | Autorizar fuentes y licencias; minimizar datos personales; documentar finalidad y permisos; revisar políticas internas antes de incorporar documentos.             |
| R11    | Inyección de instrucciones maliciosas en documentos o consultas.              | Map / Measure / Manage  | Seguridad de IA           | Alto        | Media            | Alto      | Mitigar          | Tratar documentos como datos, no instrucciones; limitar herramientas; filtrar entradas; probar prompt injection; exigir aprobación humana para acciones sensibles. |

La priorización propuesta presta especial atención a la confidencialidad, la exactitud técnica y la dependencia del sistema, debido a que pueden afectar directamente la atención comercial. La valoración no constituye una certificación ni reemplaza un análisis formal de amenazas. Antes del despliegue deberán asignarse responsables, fechas de tratamiento, evidencia de control y criterios de aceptación para cada riesgo. Cualquier incidente deberá registrarse, analizarse y utilizarse para ajustar el diseño o restringir funciones cuando sea necesario.

# 10. Conclusiones del módulo

1.  El problema identificado se relaciona con la dificultad de recuperar de forma rápida, consistente y verificable información técnica que puede estar distribuida en manuales, procedimientos y fichas técnicas. Un asistente documental local constituye una alternativa pertinente para facilitar esa consulta, siempre que su utilidad sea demostrada mediante pruebas.

2.  La incorporación de recuperación documental y referencias a las fuentes puede mejorar la verificabilidad de las respuestas, pero no garantiza por sí sola su exactitud. La calidad depende de la vigencia de los documentos, la recuperación, el modelo y los mecanismos de evaluación y abstención.

3.  La operación local responde a la necesidad de mantener el conocimiento corporativo bajo control, aunque debe complementarse con permisos, gestión de versiones, registros, controles de red y prácticas de seguridad. La localización del modelo no elimina todos los riesgos.

4.  El alcance propuesto prioriza la consulta documental y el apoyo a los asesores, excluyendo la automatización de transacciones y las decisiones que requieren aprobación humana. Esta delimitación permite construir un prototipo evaluable y reducir complejidad innecesaria.

5.  La aplicación de las funciones Govern, Map, Measure y Manage del NIST AI RMF desde la fase inicial permite identificar responsables, contextualizar impactos, evaluar desempeño y tratar riesgos de manera continua. Las metas cuantitativas propuestas deberán validarse con una línea base y con la participación de los usuarios y responsables técnicos.

# 11. Referencias

International Organization for Standardization, & International Electrotechnical Commission. (2022). ISO/IEC 27001:2022 Information security, cybersecurity and privacy protection—Information security management systems—Requirements. https://www.iso.org/standard/27001.html

Lewis, P., Perez, E., Piktus, A., Petroni, F., Karpukhin, V., Goyal, N., Küttler, H., Lewis, M., Yih, W.-t., Rocktäschel, T., Riedel, S., & Kiela, D. (2020). Retrieval-augmented generation for knowledge-intensive NLP tasks. In Advances in Neural Information Processing Systems (Vol. 33, pp. 9459–9474). https://proceedings.neurips.cc/paper/2020/hash/6b493230205f780e1bc26945df7481e5-Abstract.html

Tabassi, E. (2023). Artificial intelligence risk management framework (AI RMF 1.0) (NIST AI 100-1). National Institute of Standards and Technology. https://doi.org/10.6028/NIST.AI.100-1
