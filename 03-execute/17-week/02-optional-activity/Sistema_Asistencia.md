ANÁLISIS Y PROPUESTA DE MEJORAS

Sistema Web para la Optimización del Proceso de Toma de Asistencia en el SENA

Versión 1.1 — Revisión Técnica por el Equipo de Ingeniería de Software

1. NECESIDADES

DIAGNÓSTICO:

Las necesidades planteadas inicialmente describen de manera adecuada la problemática del proyecto; sin embargo, presentan algunos puntos repetitivos que pueden consolidarse para mejorar la claridad del documento. En particular, la necesidad relacionada con la reducción del tiempo de registro y la visualización de los aprendices abordan objetivos estrechamente vinculados. Asimismo, la necesidad referente a una arquitectura escalable corresponde a un aspecto técnico del sistema y no a una necesidad propia del usuario.

NECESIDADES CONSOLIDADAS Y MEJORADAS:

- Disminuir el tiempo requerido por el instructor para registrar la asistencia completa de los aprendices durante cada jornada de formación.

- Reducir la dependencia del proceso de toma de asistencia realizado exclusivamente mediante la plataforma SOFIA Plus.

- Presentar el listado completo de aprendices en una única interfaz, evitando búsquedas individuales o navegación entre diferentes pantallas.

- Garantizar que cada registro de asistencia quede almacenado de forma segura, incluyendo la fecha, la hora y el estado correspondiente, asegurando su integridad y trazabilidad.

- Evitar registros duplicados, inconsistentes o realizados de manera fraudulenta.

- Permitir la consulta y modificación de registros previamente almacenados, manteniendo evidencia de cada cambio realizado.

- Ofrecer una interfaz intuitiva y de fácil utilización que no requiera procesos de capacitación para su uso.

NOTA: La característica relacionada con una arquitectura escalable se traslada a la sección de restricciones o requerimientos técnicos, ya que constituye una decisión de diseño y no una necesidad del usuario final.

2. JUSTIFICACIÓN

DIAGNÓSTICO:

La justificación presentada inicialmente expone correctamente el propósito del proyecto; sin embargo, carece de información cuantificable que permita dimensionar el impacto del problema. Se menciona que el proceso consume tiempo, pero no se especifica cuánto representa ese tiempo dentro de la jornada de formación ni las consecuencias que genera.

MEJORA PROPUESTA:

Actualmente, el proceso de registro de asistencia mediante SOFIA Plus requiere entre ocho y quince minutos para completar el control de una ficha conformada por aproximadamente treinta aprendices. Este tiempo se descuenta directamente de las actividades académicas programadas durante la jornada.

Considerando que normalmente se realizan tres controles de asistencia al día —inicio de la jornada, regreso del receso y finalización de la formación—, el instructor puede invertir hasta cuarenta y cinco minutos diarios únicamente en el registro manual de asistencia.

Para completar este procedimiento, el instructor debe acceder a la plataforma institucional, localizar la ficha correspondiente, identificar individualmente a cada aprendiz y verificar el número total de asistentes. Esta secuencia debe repetirse en cada uno de los puntos de control establecidos durante la jornada, incrementando la probabilidad de cometer errores y dificultando la consulta inmediata de la información registrada.

Con el desarrollo de un sistema web especializado se busca optimizar este procedimiento mediante una interfaz centralizada, organizada y enfocada exclusivamente en el proceso de toma de asistencia. La solución permitirá reducir considerablemente el tiempo empleado durante cada registro, facilitar la consulta posterior de la información y mejorar la eficiencia del proceso.

Además de resolver una necesidad operativa, el proyecto constituye una oportunidad para aplicar de manera integral los conocimientos adquiridos durante el programa de Análisis y Desarrollo de Software (ADSO), incorporando competencias relacionadas con Ingeniería de Requerimientos, modelado UML, diseño de bases de datos y desarrollo de aplicaciones web.

NOTA: La justificación funcional del proyecto debe mantenerse independiente de la justificación académica, permitiendo evidenciar que el sistema responde a una problemática real y no únicamente al cumplimiento de un ejercicio formativo.

3. OBJETIVOS

DIAGNÓSTICO:

El objetivo general presenta una formulación adecuada y no requiere modificaciones sustanciales. En contraste, los objetivos específicos mezclan actividades correspondientes a distintas etapas del ciclo de desarrollo y presentan un objetivo relacionado con la arquitectura escalable que corresponde a una decisión técnica del proyecto más que a un resultado orientado al usuario o al proceso.

OBJETIVO GENERAL

Desarrollar un sistema web que optimice el proceso de toma de asistencia de los aprendices de la ficha ADSO 3413974, disminuyendo el tiempo requerido por el instructor mediante una interfaz sencilla, ágil y organizada.

OBJETIVOS ESPECÍFICOS

OE01. Analizar el proceso actual de registro de asistencia en SOFIA Plus con el fin de identificar las dificultades existentes, los tiempos involucrados y las necesidades funcionales del sistema.

OE02. Definir los requerimientos funcionales y no funcionales del sistema a partir de la información obtenida durante el análisis.

OE03. Diseñar la arquitectura de la aplicación y el modelo de datos necesario para soportar el proceso de registro de asistencia.

OE04. Diseñar una interfaz de usuario que permita registrar la asistencia de todos los aprendices desde una única pantalla, incorporando flujos diferenciados para instructores y aprendices.

OE05. Desarrollar los módulos correspondientes al registro manual, registro mediante código QR, consulta de información, modificación de registros y generación de reportes.

OE06. Verificar el correcto funcionamiento del sistema mediante pruebas que contemplen escenarios normales de uso, casos límite y situaciones de error.
4. INGENIERÍA DE REQUERIMIENTOS — DESCRIPCIÓN

DIAGNÓSTICO:

La descripción original presenta correctamente el propósito general del sistema; sin embargo, asume que el instructor es el único actor involucrado en el proceso. La incorporación del registro mediante código QR introduce un segundo actor, el aprendiz, quien interactúa con el sistema a través de un flujo independiente. Por ello, resulta conveniente establecer esta diferenciación desde el inicio de la descripción funcional.

DESCRIPCIÓN:

El proyecto consiste en el desarrollo de una aplicación web especializada en el proceso de toma de asistencia para el entorno de formación del SENA, diseñada inicialmente para atender las necesidades de la ficha ADSO 3413974.

La aplicación contará con dos flujos de operación claramente diferenciados, de acuerdo con el tipo de usuario que interactúe con el sistema.

- Flujo del Instructor: permitirá administrar los checkpoints de asistencia (apertura y cierre), visualizar en tiempo real el estado de los registros, realizar modificaciones manuales cuando sea necesario, consultar el historial de asistencias y generar reportes.

- Flujo del Aprendiz: permitirá registrar la asistencia mediante el escaneo de un código QR, validar su identidad utilizando el nombre completo y el número de documento, y confirmar el registro mediante un código numérico temporal.

El sistema funcionará como una herramienta de apoyo para las jornadas de formación, operando de manera independiente y sin integración directa con las plataformas institucionales existentes.

ACTORES DEL SISTEMA:

Actor 1 — Instructor:

Es responsable de administrar los checkpoints de asistencia, consultar los registros almacenados, generar reportes y efectuar modificaciones manuales cuando sea necesario, garantizando la trazabilidad de cada cambio realizado.

Actor 2 — Aprendiz:

Registra su asistencia escaneando el código QR correspondiente al checkpoint activo, suministra su información de identificación y confirma el proceso mediante el código de verificación temporal generado por el sistema.

5. INSTRUMENTOS DE RECOLECCIÓN DE INFORMACIÓN

DIAGNÓSTICO:

Los instrumentos definidos inicialmente son apropiados para obtener la información necesaria; sin embargo, su descripción resulta demasiado general y no especifica con claridad qué datos se pretenden recopilar mediante cada técnica. Una definición más detallada facilita la aplicación de la metodología y mejora la trazabilidad de la información obtenida.

INSTRUMENTOS:

IR01. Observación directa del proceso actual:

Registrar el procedimiento utilizado por el instructor durante la toma de asistencia en SOFIA Plus, midiendo el tiempo requerido para completar cada uno de los tres controles diarios (inicio de la jornada, regreso del receso y finalización). Asimismo, identificar la cantidad de acciones manuales involucradas y documentar los puntos donde se presentan demoras o errores.

IR02. Revisión del procedimiento en SOFIA Plus:

Documentar detalladamente el flujo actual del proceso de registro de asistencia, incluyendo el número de pantallas involucradas, las acciones necesarias para localizar a cada aprendiz y los tiempos de respuesta de la plataforma. Además, identificar las limitaciones funcionales y técnicas que afectan la eficiencia del proceso.

IR03. Entrevista con el instructor:

Recopilar información sobre las dificultades más frecuentes durante el registro de asistencia, los datos que requiere consultar durante la jornada, la frecuencia con la que accede al historial de registros y los reportes que utiliza para el seguimiento de la asistencia.

IR04. Análisis del listado oficial de aprendices:

Examinar la información oficial correspondiente a los aprendices de la ficha, identificando la estructura y los datos necesarios (nombre completo, número de documento y estado dentro de la ficha), con el propósito de definir adecuadamente el modelo de datos del sistema.
6. REQUERIMIENTOS FUNCIONALES (REORGANIZADOS POR MÓDULOS)

DIAGNÓSTICO:

La organización original de los requerimientos funcionales integra en una única lista procesos correspondientes a dos actores diferentes: el instructor y el aprendiz. Esta estructura dificulta la comprensión del comportamiento esperado del sistema y genera inconsistencias entre el registro manual y el registro mediante código QR. Asimismo, algunos requerimientos, como las copias de seguridad y el soporte para múltiples fichas, representan características técnicas o evolutivas que deberían documentarse fuera de la lista principal de funcionalidades.

ORGANIZACIÓN PROPUESTA:

MÓDULO A — GESTIÓN DE CHECKPOINTS (Actor: Instructor)

RF-A01. El sistema deberá permitir al instructor abrir un checkpoint indicando el tipo correspondiente: Inicio de jornada, Regreso de receso o Finalización de jornada.

RF-A02. El sistema deberá generar automáticamente un código QR único al momento de crear cada checkpoint.

RF-A03. El código QR permanecerá activo mientras el checkpoint se encuentre abierto.

RF-A04. Al abrir un checkpoint, el sistema deberá generar un código numérico de verificación y renovarlo automáticamente cada veinte segundos.

RF-A05. El sistema deberá mostrar al instructor el código numérico vigente junto con un contador visual que indique el tiempo restante antes de su actualización.

RF-A06. El sistema deberá permitir al instructor cerrar un checkpoint, impidiendo nuevos registros de asistencia una vez finalizado el proceso.

RF-A07. Antes de cerrar un checkpoint, el sistema deberá informar cuántos aprendices aún no registran asistencia y solicitar una confirmación explícita para completar el cierre.

RF-A08. Cada tipo de checkpoint únicamente podrá abrirse y cerrarse una vez durante la misma jornada de formación.

MÓDULO B — REGISTRO DE ASISTENCIA POR QR (Actor: Aprendiz)

RF-B01. Después de escanear el código QR, el sistema deberá presentar un formulario solicitando el nombre completo y el número de documento del aprendiz.

RF-B02. El sistema deberá validar que el nombre y el documento ingresados correspondan al mismo aprendiz registrado en la ficha activa.

RF-B03. Una vez validada correctamente la identidad, el sistema deberá solicitar el código numérico de verificación vigente.

RF-B04. El sistema deberá comprobar que el código ingresado continúe vigente al momento de realizar la validación.

RF-B05. El sistema deberá impedir el registro cuando el aprendiz ya haya registrado su asistencia en el checkpoint activo.

RF-B06. Al confirmar la asistencia, el sistema deberá almacenar la fecha, la hora exacta, el tipo de checkpoint y el identificador del dispositivo desde el cual se realizó el registro.

RF-B07. El sistema deberá mostrar un mensaje de confirmación que incluya el nombre del aprendiz, el tipo de checkpoint registrado y la hora en que se efectuó el registro.

RF-B08. Ante cualquier error de validación, el sistema deberá presentar mensajes descriptivos que indiquen claramente la causa del problema y la acción que debe realizar el aprendiz.

MÓDULO C — GESTIÓN MANUAL (Actor: Instructor)

RF-C01. El sistema deberá presentar el listado completo de aprendices de la ficha en una única pantalla, mostrando el estado de asistencia correspondiente al checkpoint activo.

RF-C02. El sistema deberá permitir al instructor asignar o modificar manualmente el estado de asistencia de cada aprendiz entre las opciones: Asistió, Tarde y Ausente.

RF-C03. El sistema deberá diferenciar los registros creados o modificados manualmente por el instructor de aquellos registrados mediante código QR.

RF-C04. El sistema deberá permitir modificar el estado de asistencia de un aprendiz después del cierre del checkpoint, conservando un registro auditable de la modificación realizada.

RF-C05. El sistema deberá permitir localizar aprendices mediante búsquedas por nombre completo o número de documento.

MÓDULO D — CONSULTA Y REPORTES (Actor: Instructor)

RF-D01. El sistema deberá permitir consultar los registros de asistencia filtrándolos por fecha y tipo de checkpoint.

RF-D02. El sistema deberá generar un resumen por jornada que indique la cantidad de aprendices asistentes, tardíos y ausentes.

RF-D03. El sistema deberá permitir consultar el historial completo de asistencia correspondiente a un aprendiz específico.

RF-D04. El sistema deberá permitir exportar la información de asistencia en formatos Excel y PDF.

RF-D05. El sistema deberá conservar un historial de todas las modificaciones realizadas sobre los registros de asistencia, indicando el estado anterior, el nuevo estado, la fecha y la hora de la modificación.

RF-D06. El sistema deberá registrar todos los intentos fallidos de autenticación o validación, almacenando la fecha, la hora, el tipo de error y los datos ingresados con fines de auditoría.

RF-D07. Los registros modificados manualmente deberán identificarse visualmente mediante un indicador que informe que fueron editados dentro del panel de consulta.
7. REQUERIMIENTOS NO FUNCIONALES

DIAGNÓSTICO:

La versión original del documento no incorpora una sección dedicada a los Requerimientos No Funcionales. Esta ausencia representa una limitación importante dentro de un documento SRS basado en el estándar IEEE 830, ya que estos requisitos establecen los criterios técnicos que permitirán evaluar la calidad y aceptación del sistema una vez finalizado su desarrollo.

REQUERIMIENTOS NO FUNCIONALES:

RENDIMIENTO

RNF01. El sistema deberá cargar el listado completo de aprendices en un tiempo inferior a dos segundos bajo condiciones normales de funcionamiento de la red.

RNF02. El proceso de validación de identidad del aprendiz deberá completarse en menos de un segundo después del envío del formulario.

RNF03. El código numérico de verificación deberá actualizarse automáticamente con una precisión de un segundo, admitiendo una desviación máxima de quinientos milisegundos.

DISPONIBILIDAD

RNF04. El sistema deberá permanecer disponible durante toda la jornada de formación. Como medida recomendada, su funcionamiento deberá ser posible dentro de una red local (LAN), evitando la dependencia de una conexión permanente a Internet.

RNF05. Si durante un registro ocurre una pérdida temporal de conexión, el sistema deberá informar la situación al usuario y permitir reintentar la operación sin perder la información previamente ingresada.

SEGURIDAD

RNF06. Los códigos numéricos de verificación deberán generarse de forma impredecible y no podrán repetirse durante una misma jornada de formación.

RNF07. La información de identificación de los aprendices no deberá quedar expuesta ni codificada dentro de la URL generada por el código QR.

RNF08. Los registros de auditoría correspondientes a intentos fallidos y modificaciones deberán mantenerse como información de solo lectura para todos los usuarios y no podrán eliminarse.

RNF09. Después de tres intentos consecutivos de validación fallida desde un mismo dispositivo dentro del mismo checkpoint, el sistema deberá aplicar un tiempo de espera de treinta segundos antes de permitir un nuevo intento.

USABILIDAD

RNF10. El proceso completo de registro del aprendiz, desde el escaneo del código QR hasta la confirmación de la asistencia, no deberá superar tres pantallas consecutivas.

RNF11. Todos los mensajes de error deberán describir claramente la causa del problema e indicar la acción que debe realizar el usuario. No se admitirán mensajes genéricos o códigos sin explicación.

RNF12. La interfaz destinada al aprendiz deberá visualizarse correctamente en dispositivos móviles con pantallas de cinco pulgadas o superiores, permitiendo la lectura del contenido sin necesidad de ampliar la pantalla.

ESCALABILIDAD

RNF13. La arquitectura del sistema y el modelo de datos deberán permitir incorporar soporte para múltiples fichas de formación en versiones futuras sin requerir un rediseño estructural.

MANTENIBILIDAD

RNF14. El código fuente deberá contener comentarios suficientes que faciliten su comprensión y mantenimiento por parte de otros aprendices del programa ADSO.

RNF15. La aplicación deberá organizarse mediante módulos independientes según su responsabilidad (gestión de checkpoints, registro de asistencia, consultas y reportes), favoreciendo su mantenimiento y evolución.

8. SEGURIDAD DEL SISTEMA

MODELO DE SEGURIDAD ACTUAL:

- El instructor genera un código QR único para cada checkpoint.

- El código QR permanece disponible mientras el checkpoint se encuentre abierto.

- El aprendiz escanea el código QR e ingresa su nombre completo y número de documento.

- El sistema valida que ambos datos correspondan al mismo aprendiz registrado en la ficha activa.

- Una vez validada la identidad, el sistema solicita el código numérico de verificación vigente.

- El código numérico se renueva automáticamente cada veinte segundos.

- Los códigos que hayan expirado dejan de ser válidos para el proceso de autenticación.

- Cada aprendiz únicamente podrá registrar una asistencia por cada checkpoint.

- La jornada de formación contempla únicamente tres checkpoints: Inicio, Regreso de receso y Finalización.

- Todos los intentos de validación y las modificaciones realizadas sobre los registros quedarán almacenados para fines de auditoría.

ESCENARIOS DE RIESGO Y MITIGACIONES PROPUESTAS:

Escenario 1 — Compartición del código numérico entre aprendices

RIESGO:

Un aprendiz ausente comunica el código numérico vigente a otro compañero, quien intenta registrar la asistencia utilizando los datos del aprendiz ausente desde su propio dispositivo.

MITIGACIÓN:

El sistema deberá registrar el identificador del dispositivo (por ejemplo, dirección IP o user-agent) utilizado durante cada registro. Cuando dos aprendices diferentes registren asistencia desde el mismo dispositivo dentro del mismo checkpoint, el sistema marcará automáticamente ambos registros dentro del historial de auditoría para su posterior revisión por parte del instructor. Esta situación no generará un bloqueo automático, evitando así posibles falsos positivos, pero conservará la evidencia correspondiente.

Escenario 2 — Uso del código QR desde fuera del aula

RIESGO:

Al permanecer activo durante todo el checkpoint, el código QR puede ser fotografiado y utilizado desde un dispositivo ubicado fuera del salón de formación.

ANÁLISIS:

La combinación de un código QR fijo, un código numérico temporal con vigencia de veinte segundos y la validación de identidad proporciona un nivel de seguridad adecuado para el alcance del proyecto. Para realizar un registro fraudulento sería necesario disponer simultáneamente del código QR, de la información personal del aprendiz y del código numérico vigente. La incorporación de mecanismos como geolocalización o autenticación biométrica incrementaría considerablemente la complejidad del sistema y supera los objetivos establecidos para esta versión.

DECISIÓN:

No se considera necesaria la implementación de medidas adicionales para este escenario en la versión actual del sistema.

Escenario 3 — Modificaciones no identificadas por el instructor

RIESGO:

Los registros de asistencia pueden modificarse posteriormente sin que el instructor pueda identificar fácilmente que la información fue alterada.

MITIGACIÓN:

Todo registro modificado manualmente deberá mostrar un indicador visual de "Editado" dentro del panel de consulta. Además, deberá conservar la fecha, la hora y el estado anterior del registro. Esta información permanecerá disponible de forma permanente y no podrá eliminarse, garantizando la integridad del historial de cambios.

Escenario 4 — Cierre accidental del checkpoint

RIESGO:

El instructor puede cerrar un checkpoint antes de que todos los aprendices hayan registrado su asistencia.

MITIGACIÓN:

Antes de completar el cierre, el sistema deberá informar el número de aprendices que aún no cuentan con registro y solicitar una confirmación explícita. Después del cierre, el instructor conservará la posibilidad de registrar manualmente la asistencia pendiente, identificando dichos registros como "Registro tardío manual".

Escenario 5 — Múltiples intentos fallidos de autenticación

RIESGO:

Un aprendiz o un tercero intenta descubrir los datos de otro aprendiz realizando múltiples combinaciones de nombre y documento.

MITIGACIÓN:

Después de tres intentos consecutivos fallidos desde el mismo dispositivo dentro del mismo checkpoint, el sistema aplicará un tiempo de espera de treinta segundos antes de permitir un nuevo intento. Todos los intentos quedarán registrados en el historial de auditoría junto con la fecha, la hora, los datos ingresados y la información del dispositivo utilizado.

Escenario 6 — Checkpoint abierto sin supervisión del instructor

RIESGO:

El instructor abre un checkpoint y posteriormente abandona el aula, dejando visible el código QR y el código numérico de verificación.

MITIGACIÓN:

La responsabilidad de cerrar el checkpoint corresponde al instructor. Para esta versión del sistema no se recomienda implementar un cierre automático por tiempo, ya que podría interrumpir el proceso normal de registro de asistencia. Este escenario deberá documentarse como una responsabilidad operativa del usuario encargado del sistema.
