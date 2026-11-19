# Propuesta de Proyecto – Programación Orientada a Objetos

**Carrera:** Ingeniería de Software  
**Materia:** Programación II  
**Periodo:** Segundo Parcial / Proyecto Final  
**Estudiante(s):** Leonardo Feeney Camacho  
**Fecha de entrega:** 2026-11-21

------------------------------------------------------------------------

## 1. Datos Generales del Proyecto

| Campo                             | Descripción                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre del proyecto:              | BusReserva UCB                                                                                                                                  |
| Tipo de aplicación:               | ☐ Escritorio ☑ Web ☐ Móvil ☐ Otro: \_\_\_\_\_\_\_\_\_\_                                                                                         |
| Lenguaje / entorno de desarrollo: | Java 21 con Javalin (framework web), Visual Studio Code y Ubuntu mediante WSL. Almacenamiento temporal en memoria mediante colecciones de Java. |
| Repositorio Git (URL):            | <https://github.com/Leonardorso/Progra_2.git>                                                                                                   |
| Uso de Inteligencia Artificial:   | ☐ No ☑ Sí (describir a continuación)                                                                                                            |

**Si usas IA, explica brevemente cómo y en qué etapa contribuye:**

Se utilizarán ChatGPT (OpenAI) y Claude (Anthropic) como herramientas de
apoyo durante la planificación, comprensión de conceptos, elaboración y
revisión de diagramas, organización de la propuesta y resolución de
dudas o errores durante el desarrollo. El estudiante revisará, probará,
adaptará y comprenderá la implementación final, y deberá poder explicar
las clases, los métodos y las decisiones de diseño del proyecto.

------------------------------------------------------------------------

## 2. Descripción del Proyecto

### Resumen breve

BusReserva UCB es una aplicación web desarrollada en Java con Javalin,
pensada para los estudiantes de la Universidad Católica Boliviana (UCB),
sede Santa Cruz, que utilizan el servicio gratuito de buses entre la
Iglesia La Santa Cruz y el campus universitario.

Actualmente, en determinados horarios la cantidad de estudiantes supera
los asientos disponibles. Esto provoca filas de espera que pueden durar
aproximadamente entre 30 minutos y una hora, además de incomodidad por
el calor, las aglomeraciones y los problemas que se producen cuando
algunas personas intentan adelantarse en la fila. En ocasiones, algunos
estudiantes no alcanzan a subir y deben buscar otro medio de transporte,
lo que implica gastar dinero adicional. El servicio busca acercarlos a
sus hogares y facilitar su movilidad, por lo que perder tiempo esperando
sin saber si podrán abordar afecta su propósito.

La aplicación permitirá consultar los horarios publicados por la
universidad, reservar o cancelar un cupo para una salida específica y
conocer la disponibilidad antes de dirigirse a la parada. El personal de
transporte cumplirá también el rol de administrador del sistema: podrá
consultar la lista de reservas de cada salida, verificar presencialmente
el carnet universitario del estudiante y marcar su abordaje.

### Objetivos principales

**Objetivo general:** desarrollar una aplicación web en Java, aplicando
programación orientada a objetos, que permita gestionar reservas de
cupos para el servicio gratuito de buses de la UCB y organizar el
abordaje de los estudiantes, con el propósito de reducir las filas, los
tiempos de espera y la incertidumbre de no conseguir asiento.

**Objetivos específicos:**

1.  Disponer de un listado previo de estudiantes autorizados, con su
    nombre y código universitario. En el prototipo no habrá registro
    público de estudiantes.
2.  Cargar y consultar los horarios de ida y vuelta publicados por la
    UCB, incluyendo los días y la cantidad de buses asignados a cada
    salida.
3.  Registrar la capacidad de cada bus, considerando que puede variar
    aproximadamente entre 23 y 29 asientos, y calcular los cupos
    disponibles para cada salida.
4.  Permitir que un estudiante previamente registrado reserve o cancele
    un cupo para una salida específica, sin superar la capacidad
    disponible ni permitir reservas activas duplicadas.
5.  Permitir que el administrador, que representa al personal de
    transporte presente en la parada, consulte las reservas y compare
    los datos del estudiante con su carnet universitario físico.
6.  Registrar el abordaje de cada estudiante una vez verificada su
    identidad, evitando que una misma reserva se utilice más de una vez.
7.  Almacenar temporalmente los estudiantes, horarios, viajes y reservas
    en memoria mediante colecciones de Java, para simplificar el
    desarrollo y demostrar los conceptos de POO.
8.  Manejar errores mediante validaciones y excepciones propias, por
    ejemplo: estudiante no registrado, cupo agotado, reserva duplicada o
    reserva inexistente.
9.  Aplicar encapsulamiento, constructores, herencia, polimorfismo e
    interfaces o clases abstractas en una estructura organizada.

### Alcance del prototipo y posible ampliación futura

**Alcance del prototipo académico:**

- Los estudiantes autorizados estarán cargados previamente en el
  sistema. Para las pruebas se utilizarán datos de demostración.
- El estudiante se identificará mediante su código universitario, que
  deberá existir en el listado previamente cargado. Este mecanismo es
  simplificado y se utilizará únicamente para demostrar el
  funcionamiento.
- El administrador tendrá acceso a un panel de control para consultar
  las reservas, verificar el carnet físico y registrar el abordaje.
- La información se mantendrá en memoria mientras la aplicación esté
  ejecutándose. Al detener o reiniciar el programa, las reservas creadas
  durante esa ejecución se perderán y los datos iniciales de prueba
  deberán cargarse nuevamente.
- No se implementará en esta etapa una conexión real con el sistema de
  estudiantes de la UCB ni se almacenarán contraseñas institucionales.

**Posible ampliación futura:**

Si la universidad decidiera implementar oficialmente el sistema,
BusReserva UCB podría integrarse con el portal o sistema de estudiantes
existente. El estudiante ingresaría con su correo institucional y
contraseña, y desde su cuenta encontraría una sección de reserva de
buses con los horarios disponibles. La identidad del estudiante podría
obtenerse de la autenticación institucional, evitando crear un registro
público separado o almacenar nuevamente sus credenciales. También se
podría incorporar almacenamiento persistente para conservar las reservas
entre ejecuciones.

------------------------------------------------------------------------

## 3. Diseño Técnico y Aplicación de POO

### Tecnologías previstas

- **Lenguaje:** Java 21.
- **Aplicación web:** Javalin.
- **Entorno de desarrollo:** Visual Studio Code y Ubuntu mediante WSL.
- **Control de versiones:** Git y GitHub.
- **Almacenamiento del prototipo:** memoria temporal mediante
  colecciones de Java, como `Map` y `List`.
- **Base de datos:** no se utilizará MySQL en el prototipo académico.

### Principios de POO aplicados

Se planea utilizar los siguientes principios:

- ☑ Encapsulamiento (atributos privados y métodos públicos).
- ☑ Uso de constructores.
- ☑ Herencia.
- ☑ Polimorfismo.
- ☑ Interfaces o clases abstractas.

Como parte del diseño, se podrán utilizar clases relacionadas con
usuarios, estudiantes, administradores, buses, rutas, horarios, viajes y
reservas. La estructura definitiva se ajustará durante el desarrollo
para mantener el código claro y evitar complejidad innecesaria.

Por ejemplo, se podrá utilizar una clase abstracta `Usuario` y clases
derivadas `Estudiante` y `Administrador`. El administrador representará
al personal de transporte encargado de verificar los carnets y controlar
el abordaje.

### Almacenamiento de datos

- [ ] Archivos locales
- [ ] Base de datos
- ☑ En memoria (temporal)
- [ ] Otro: \_\_\_\_\_\_\_\_\_\_

Los datos se administrarán durante la ejecución mediante estructuras de
datos de Java. Para la demostración se cargarán previamente estudiantes
y horarios de prueba. Esta decisión facilita el desarrollo y permite
concentrarse en la aplicación de POO, aunque implica que la información
generada durante la ejecución no se conservará al cerrar el programa.

### Capacidad de los buses

La página de la UCB publica los horarios y la cantidad de buses
asignados a cada salida, pero no especifica la cantidad de asientos de
cada vehículo. Para el prototipo se permitirá configurar la capacidad de
cada bus dentro del rango observado de 23 a 29 asientos.

La capacidad total de una salida se calculará sumando los asientos de
los buses asignados a ese horario. Si no se conoce la capacidad exacta
de un vehículo, se podrá utilizar provisionalmente el valor conservador
de 23 asientos, sujeto a confirmación.

------------------------------------------------------------------------

## 4. Funcionalidades Principales

| Nº  | Nombre de la funcionalidad                       | Descripción breve                                                                                                                                                             | Estado actual              |
|-----|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| 1   | Listado previo de estudiantes                    | El sistema contará con estudiantes previamente cargados, identificados por nombre y código universitario. No habrá autorregistro público en el prototipo.                     | ☑ Planeada ☐ En desarrollo |
| 2   | Consulta de horarios                             | Muestra los horarios de ida y vuelta entre la Iglesia La Santa Cruz y el campus, con los días y la cantidad de buses de cada salida.                                          | ☑ Planeada ☐ En desarrollo |
| 3   | Configuración de capacidad                       | Permite establecer la capacidad de cada bus, dentro del rango previsto de 23 a 29 asientos, y calcular los cupos totales de una salida.                                       | ☑ Planeada ☐ En desarrollo |
| 4   | Reserva de cupo                                  | El estudiante previamente registrado selecciona una salida y reserva un cupo. El sistema controla la capacidad y evita reservas activas duplicadas.                           | ☑ Planeada ☐ En desarrollo |
| 5   | Cancelación y consulta de reservas               | El estudiante puede consultar sus reservas y cancelar una, liberando el cupo correspondiente.                                                                                 | ☑ Planeada ☐ En desarrollo |
| 6   | Panel del administrador / personal de transporte | Permite consultar las salidas y visualizar la lista de estudiantes que reservaron un cupo.                                                                                    | ☑ Planeada ☐ En desarrollo |
| 7   | Verificación de carnet y control de abordaje     | El personal de transporte compara el nombre y código de la reserva con el carnet universitario físico y marca el abordaje cuando la identidad coincide.                       | ☑ Planeada ☐ En desarrollo |
| 8   | Almacenamiento temporal                          | Mantiene estudiantes, horarios, viajes y reservas en memoria mediante colecciones de Java durante la ejecución del programa.                                                  | ☑ Planeada ☐ En desarrollo |
| 9   | Reporte de demanda                               | El administrador puede consultar cuántas reservas existen por salida, para identificar los horarios con mayor demanda.                                                        | ☑ Planeada ☐ En desarrollo |
| 10  | Manejo de errores                                | Valida los datos y comunica situaciones como estudiante no registrado, cupo agotado, reserva duplicada, cancelación inválida o reserva inexistente, sin cerrar la aplicación. | ☑ Planeada ☐ En desarrollo |

### Estados de una reserva

Para controlar el proceso se contemplan los siguientes estados:

- **Confirmada:** el estudiante tiene un cupo reservado.
- **Cancelada:** el estudiante canceló la reserva y el cupo vuelve a
  estar disponible.
- **Abordada:** el personal de transporte verificó el carnet y registró
  que el estudiante subió al bus.

Una reserva abordada no podrá volver a utilizarse para registrar otro
abordaje en el mismo viaje.

------------------------------------------------------------------------

## 5. Compromiso del Estudiante

Declaro que:

- Entiendo los criterios de evaluación establecidos en las rúbricas.
- Presentaré una demostración funcional del proyecto.
- Defenderé el código que yo mismo implemente y explicaré las clases y
  métodos principales.
- Si utilizo herramientas de inteligencia artificial, declararé su uso,
  revisaré el código generado o sugerido y me aseguraré de comprender y
  poder explicar las partes incorporadas al proyecto.
- Reconozco que el almacenamiento en memoria es una decisión para el
  prototipo académico y que una implementación real requeriría
  persistencia de datos e integración con los sistemas de la
  universidad.

**Firma (nombre completo):**
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

------------------------------------------------------------------------

## 6. Validación del Docente (completa el profesor)

| Campo                        | Detalle                                                    |
|------------------------------|------------------------------------------------------------|
| Visto bueno del docente:     | ☐ Aprobado para desarrollar ☐ Requiere ajustes ☐ Rechazado |
| Comentarios / Observaciones: |                                                            |
| Firma docente:               |                                                            |
| Fecha de revisión:           |                                                            |

------------------------------------------------------------------------

**Instrucciones para entrega:**

- Guarda este archivo como README.md dentro de tu repositorio Git.
- Completa todas las secciones antes de tu presentación inicial.
- No borres las casillas ni el formato para garantizar uniformidad del
  curso.
- El docente revisará y aprobará esta propuesta antes del desarrollo
  completo.
