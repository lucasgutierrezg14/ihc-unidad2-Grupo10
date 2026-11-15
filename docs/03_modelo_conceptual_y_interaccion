# 3. Modelo Conceptual

## 3.1 Qué hará el sistema y organización de la experiencia
El sistema funcionará como un **gestor visual de disponibilidad espacial y temporal en tiempo real** que conecta a los estudiantes con las salas de estudio de la universidad. La experiencia de interacción se organiza en tres momentos claros:
1. **Exploración y filtrado:** El estudiante visualiza el estado actual de todas las salas según sede, edificio y capacidad sin tener que navegar por menús profundos.
2. **Asignación directa:** El usuario selecciona una sala disponible, marca el bloque horario deseado y obtiene una confirmación instantánea.
3. **Validación y ciclo de uso:** Al llegar a la sala, el estudiante confirma su ocupación (check-in) mediante un pase digital, y al retirarse puede liberar el espacio con un toque para actualizar la disponibilidad del sistema en tiempo real.

## 3.2 Conceptos principales que debe comprender el usuario
Para operar la plataforma sin ambigüedades, el modelo conceptual se estructura en cinco entidades fundamentales:
* **Sala de Estudio (Recurso físico):** Espacio identificable por su código (ej. *Sala B-204*), ubicación (campus/piso), capacidad máxima de personas, equipamiento disponible (pizarra, pantalla HDMI, enchufes) y estado en tiempo real (*Disponible*, *Próxima a liberarse*, *Ocupada*).
* **Bloque Horario (Unidad temporal):** Intervalo de tiempo estructurado (bloques de 60 o 90 minutos) asociado a una fecha y hora específica en el que una sala puede ser reservada.
* **Reserva (Compromiso de uso):** Registro activo que vincula a un estudiante responsable con una **Sala de Estudio** durante uno o más **Bloques Horarios** consecutivos.
* **Pase de Acceso / Check-in (Credencial digital):** Comprobante generado automáticamente al confirmar una reserva (compuesto por un código QR y un PIN de 4 dígitos) que permite validar la llegada presencial dentro de los primeros 10 minutos del bloque.
* **Estado de Ocupación (Ciclo de vida):** Indicador dinámico que refleja la situación real del espacio (`Disponible` → `Reservada` → `En uso` → `Liberada`).

## 3.3 Relaciones entre los conceptos
Un **Estudiante** consulta el catálogo de **Salas de Estudio** filtrando por sus necesidades; al elegir una sala, inspecciona sus **Bloques Horarios** libres y genera una **Reserva**. Dicha **Reserva** bloquea temporalmente el espacio, cambia su **Estado de Ocupación** y emite un **Pase de Acceso**. Cuando el estudiante ejecuta el check-in en la puerta o presiona *Liberar sala*, el sistema actualiza nuevamente el **Estado de Ocupación** para toda la comunidad universitaria.

---

# 4. Metáfora de Interfaz

## 4.1 Metáfora seleccionada: Tablero de Fichas de Sala y Pase Digital
La interfaz combina dos metáforas cotidianas altamente reconocibles en el ámbito universitario: un **Tablero de Fichas** para la búsqueda y selección, y un **Pase o Ticket Digital** para la gestión de la reserva activa.

## 4.2 Justificación de la metáfora
* **Tablero de Fichas (Cards visuales):** Replica el modelo mental de observar un panel físico de llaves o tarjetas de salas en la entrada de una biblioteca. Cada sala se presenta como una "ficha" individual que agrupa su nombre, capacidad, equipamiento mediante íconos y una franja de color semántico (verde para disponible, ámbar para próxima a liberarse y rojo para ocupada). Esto permite escanear y comparar múltiples salas de un vistazo sin esfuerzo cognitivo.
* **Pase o Ticket Digital:** Una vez confirmada la selección, la reserva adopta la forma visual de un ticket o pase de acceso (similar a una tarjeta de embarque o entrada digital) que destaca la hora, el número de sala, el código QR/PIN de check-in y un botón inferior para "Entregar/Liberar sala". Esta metáfora comunica de forma intuitiva que el usuario posee un derecho temporal de uso que debe validar al llegar y devolver al salir.

---

# 5. Tipos de Interacción

La siguiente tabla relaciona los cinco paradigmas de interacción presentes en la propuesta con las acciones concretas que ejecuta el estudiante dentro de la aplicación:

| Tipo de Interacción | Aplicación en el Sistema | Acciones concretas del usuario en la propuesta |
| :--- | :--- | :--- |
| **Instruir** | El usuario emite órdenes directas y explícitas al sistema mediante controles de acción y filtros. | • Seleccionar sede, fecha y cantidad de integrantes en la barra de filtros.<br>• Presionar el botón **"Confirmar reserva"**.<br>• Ejecutar las acciones **"Liberar sala ahora"** o **"Cancelar reserva"**. |
| **Manipular** | El usuario interactúa directamente con representaciones gráficas en pantalla mediante gestos táctiles. | • Deslizar horizontalmente la línea de tiempo (*timeline*) de bloques horarios.<br>• Tocar y seleccionar directamente las tarjetas/fichas de salas y los intervalos de tiempo en la grilla visual. |
| **Explorar** | El usuario recorre libremente la oferta de espacios y detalles sin comprometer una acción inmediata. | • Navegar por el tablero de salas disponibles organizadas por piso o edificio.<br>• Abrir el detalle de una sala para revisar su equipamiento (pizarra, TV, enchufes) y fotografías antes de decidir. |
| **Conversar** | El usuario mantiene un intercambio guiado de preguntas y respuestas rápidas con el sistema ante situaciones puntuales. | • Utilizar el asistente guiado de incidencias (ej. *"Reportar sala ocupada sin reserva"* o *"Falla de equipamiento"* mediante opciones rápidas).<br>• Responder **"Sí / No"** a consultas contextuales del sistema (ej. *"¿Deseas extender tu reserva 30 minutos más?"*). |
| **Responder** | El sistema inicia proactivamente la interacción mediante alertas o recordatorios y el usuario reacciona. | • Recibir una notificación push/alerta 10 minutos antes del inicio y presionar **"Confirmar llegada (Check-in)"**.<br>• Reaccionar al aviso de término próximo del bloque horario para desocupar o renovar el espacio. |
