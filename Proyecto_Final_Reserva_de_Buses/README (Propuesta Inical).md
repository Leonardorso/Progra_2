# Propuesta Inicial de Proyecto – Programación Orientada a Objetos

**Carrera:** Ingeniería de Software  
**Materia:** Programación II **Periodo:** Segundo Parcial / Proyecto Final  
**Estudiante(s):** Leonardo Feeney Camacho  
**Fecha de entrega:** 2026-11-21

---

## 1. Datos Generales del Proyecto

| Campo | Descripción |
|---|---|
| Nombre del proyecto: | BusReserva UCB |
| Tipo de aplicación: | ☐ Escritorio ☑ Web ☐ Móvil ☐ Otro: __________ |
| Lenguaje / entorno de desarrollo: | Java 21 con Javalin (framework web), Visual Studio Code y MySQL 8 |
| Repositorio Git (URL): | https://github.com/Leonardorso/Progra_2.git |
| Uso de Inteligencia Artificial: | ☐ No ☑ Sí (describir a continuación) |

**Si usas IA, explica brevemente cómo y en qué etapa contribuye:**

Uso Claude (Anthropic) como apoyo en la etapa de planificación: para entender conceptos, elaborar los diagramas C4 del diseño y redactar el borrador de esta propuesta. Durante el desarrollo lo usaré para resolver dudas y entender errores. El código lo escribo, lo comprendo y lo adapto yo.

---

## 2. Descripción del Proyecto

### Resumen breve

BusReserva UCB es una aplicación web en Java (framework Javalin), pensada para usarse desde el navegador del celular o la computadora, para los estudiantes de la UCB (sede Santa Cruz) que usan el bus gratuito entre la iglesia La Santa Cruz y el campus universitario. Hoy hay más estudiantes que asientos, por lo que se hacen filas de media hora a una hora para poder subir. La aplicación permite al estudiante consultar los horarios y reservar o cancelar un cupo en una salida concreta, y al administrador cargar las rutas, los horarios y la cantidad de buses. Además, las reservas muestran cuántos estudiantes quieren viajar a cada hora, información útil para justificar más buses en los horarios más cargados.

### Objetivos principales

**Objetivo general:** desarrollar una aplicación web en Java con Javalin, aplicando programación orientada a objetos, que permita reservar cupos en el bus gratuito de la UCB para reducir las filas de espera.

**Objetivos específicos:**

1. Registrar usuarios (estudiantes y administrador) y permitirles iniciar sesión.
2. Cargar y consultar los horarios de ida y vuelta, con la cantidad de buses de cada salida.
3. Permitir reservar y cancelar cupos, sin superar la capacidad de cada salida.
4. Guardar los datos de forma persistente en una base de datos MySQL para no perderlos al cerrar la aplicación.
5. Manejar los errores con excepciones propias (por ejemplo, cupo agotado o reserva duplicada).
6. Aplicar los principios de POO (encapsulamiento, herencia, polimorfismo e interfaces) en un diseño organizado en capas.

---

## 3. Diseño Técnico y Aplicación de POO

### Principios de POO aplicados

Marca los que planeas usar:

- ☑ Encapsulamiento (atributos privados y métodos públicos)
- ☑ Uso de constructores
- ☑ Herencia
- ☑ Polimorfismo
- ☑ Interfaces o clases abstractas

### Persistencia de datos

- ☐ Archivos locales
- ☑ Base de datos
- ☐ En memoria (temporal)
- ☐ Otro: __________

---

## 4. Funcionalidades Principales

| Nº | Nombre de la funcionalidad | Descripción breve | Estado actual |
|---|---|---|---|
| 1 | Registro e inicio de sesión | El usuario se registra con su código de estudiante y una contraseña guardada cifrada, y entra según su rol (estudiante o administrador). | ☑ Planeada ☐ En desarrollo |
| 2 | Consulta de horarios | Muestra los horarios de ida y vuelta entre la iglesia La Santa Cruz y el campus, con los cupos disponibles de cada salida. | ☑ Planeada ☐ En desarrollo |
| 3 | Reserva de cupo | El estudiante reserva un cupo en una salida concreta; el sistema no permite superar la capacidad ni reservar dos veces la misma salida. | ☑ Planeada ☐ En desarrollo |
| 4 | Cancelación y consulta de mis reservas | El estudiante ve sus reservas y cancela una para liberar el cupo. | ☑ Planeada ☐ En desarrollo |
| 5 | Administración de horarios y capacidad | El administrador crea y edita rutas, horarios, cantidad de buses y capacidad. | ☑ Planeada ☐ En desarrollo |
| 6 | Persistencia de datos | Guarda usuarios, horarios, viajes y reservas en una base de datos MySQL para conservarlos entre ejecuciones. | ☑ Planeada ☐ En desarrollo |
| 7 | Reporte de demanda | El administrador ve cuántas reservas hay por horario. | ☑ Planeada ☐ En desarrollo |
| 8 | Manejo de errores | Valida los datos y avisa con excepciones propias (cupo agotado, reserva duplicada, datos inválidos) sin que el programa se cierre. | ☑ Planeada ☐ En desarrollo |

(Agrega más filas si lo necesitas.)

---

## 5. Compromiso del Estudiante

Declaro que:

- Entiendo los criterios de evaluación establecidos en las rúbricas.
- Presentaré una demostración funcional del proyecto.
- Defenderé el código que yo mismo implementé y explicaré las clases y métodos principales.
- Si usé herramientas de IA, comprendo su funcionamiento y las adapté al contexto del proyecto.

**Firma (nombre completo):** __________________________

---

## 6. Validación del Docente (completa el profesor)

| Campo | Detalle |
|---|---|
| Visto bueno del docente: | ☐ Aprobado para desarrollar ☐ Requiere ajustes ☐ Rechazado |
| Comentarios / Observaciones: | |
| Firma docente: | |
| Fecha de revisión: | |

---

**Instrucciones para entrega:**

- Guarda este archivo como README.md dentro de tu repositorio Git.
- Completa todas las secciones antes de tu presentación inicial.
- No borres las casillas ni el formato para garantizar uniformidad del curso.
- El docente revisará y aprobará esta propuesta antes del desarrollo completo.
