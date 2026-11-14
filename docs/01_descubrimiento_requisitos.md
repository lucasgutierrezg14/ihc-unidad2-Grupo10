# 1. Descubrimiento de Requisitos

## 1.1 Descripción del problema de interacción
En el entorno universitario, los estudiantes requieren espacios silenciosos y equipados para estudiar o realizar trabajos grupales entre clases. Actualmente, el proceso de solicitud y consulta de salas de estudio presenta fricciones de interacción importantes: los estudiantes desconocen qué salas están disponibles en tiempo real, deben acudir presencialmente a mesones de biblioteca o navegar por formularios web poco claros con exceso de campos, y no existe un mecanismo ágil para liberar una sala cuando un grupo termina antes o no se presenta. Esto provoca pérdida de tiempo entre bloques horarios, aglomeraciones en pasillos y subutilización de los espacios disponibles.

## 1.2 Caracterización de los usuarios (Usuario objetivo)
* **Usuario principal (Estudiantes de pregrado):** Jóvenes de entre 18 y 26 años, con alto manejo de dispositivos móviles y aplicaciones web, pero con poca disponibilidad de tiempo entre clases. Buscan inmediatez, claridad visual y completar la reserva en menos de un minuto sin pasos burocráticos.
* **Usuario secundario (Personal de biblioteca / administración):** Encargados de supervisar el uso correcto de los espacios, validar reservas y gestionar incidencias de disponibilidad. Requieren visualizar ocupación de forma rápida y sin procesos manuales complejos.

## 1.3 Contexto de uso
* **Contexto físico:** Campus universitario (pasillos, cafetería, patios o biblioteca) con ruido ambiental moderado a alto, muchas veces mientras el estudiante camina o está por entrar a un bloque libre.
* **Contexto tecnológico:** Uso predominante desde teléfonos inteligentes (pantalla táctil vertical, conexión Wi-Fi institucional o datos móviles) y, de forma secundaria, desde computadores portátiles.
* **Contexto temporal y social:** Alta demanda en horas punta (entre las 11:00 y las 16:00 horas) y en semanas de evaluaciones, generalmente coordinando en tiempo real con 2 a 4 compañeros de equipo.

## 1.4 Tarea principal
**Consultar la disponibilidad en tiempo real de una sala de estudio según campus, fecha y capacidad, y completar su reserva en un bloque horario determinado con confirmación inmediata.**

## 1.5 Lista de requisitos iniciales

### Requisitos Funcionales (RF)
* **RF01 – Consulta en tiempo real:** El sistema debe mostrar el estado actual de las salas (Disponible, Ocupada, Próxima a liberarse) filtrado por sede/edificio y capacidad de personas.
* **RF02 – Selección de bloque horario:** El usuario debe poder elegir fecha, hora de inicio y duración de la reserva de forma visual.
* **RF03 – Confirmación y código de acceso:** Al confirmar, el sistema debe generar un comprobante digital con número de sala, horario y código QR o PIN de validación.
* **RF04 – Check-in y liberación anticipada:** El usuario debe poder confirmar su llegada (check-in) o liberar la sala con un toque si desocupa el espacio antes de tiempo.
* **RF05 – Gestión de reservas activas:** El usuario debe poder visualizar, modificar o cancelar sus reservas vigentes desde una vista única.

### Requisitos No Funcionales y de Usabilidad (RNF)
* **RNF01 – Eficiencia de interacción:** Completar una reserva desde la pantalla principal no debe requerir más de 3 pasos ni superar los 45 segundos.
* **RNF02 – Claridad y baja carga cognitiva:** El estado de disponibilidad debe identificarse mediante códigos de color accesibles (contraste alto + etiquetas de texto) sin depender solo del color.
* **RNF03 – Diseño adaptable (Mobile-First):** La interfaz debe optimizarse para uso con una mano en pantallas móviles, con botones táctiles amplios y jerarquía visual clara.
* **RNF04 – Retroalimentación inmediata:** Cada acción (filtrar, reservar, cancelar) debe entregar confirmación visual instantánea y opción de deshacer en caso de error.
