# 2. Diseño de Alternativas

Con base en los requisitos descubiertos y el contexto de uso móvil en hora punta, el equipo propuso tres alternativas de solución interactiva para resolver el problema de consulta y reserva de salas de estudio. Las alternativas parten de los requisitos del apartado 1 y buscan satisfacerlos de formas distintas, de modo que puedan compararse antes de elegir una (Rogers et al., 2023).

## 2.1 Descripción de las alternativas propuestas

### Alternativa 1: Aplicación Web Progresiva (PWA) Mobile-First con Tablero Visual
Solución web responsiva accesible desde cualquier navegador móvil (sin necesidad de descargar ni instalar una aplicación nativa) y mediante escaneo de códigos QR ubicados fuera de cada sala. Presenta un tablero visual con tarjetas filtrables por edificio, capacidad y estado en tiempo real, permitiendo completar la reserva en tres pasos mediante selección táctil de bloques horarios y generando un código QR/PIN de acceso inmediato.

### Alternativa 2: Asistente Conversacional (Chatbot) en Mensajería Institucional
Interfaz basada en diálogo textual secuencial integrada en canales de mensajería conocidos (WhatsApp o Telegram institucional). El estudiante inicia una conversación escribiendo comandos o seleccionando botones de respuesta rápida para indicar campus, hora y cantidad de integrantes, recibiendo como respuesta una lista textual de salas disponibles para confirmar su reserva.

### Alternativa 3: Tótems Interactivos Físicos en Biblioteca y Pasillos
Terminales táctiles fijos instalados en los accesos de biblioteca y edificios principales del campus. Muestran un plano interactivo de las salas disponibles en el momento y permiten reservar únicamente de forma presencial acercando la credencial universitaria (TUI) o ingresando el RUT en pantalla.

---

## 2.2 Tabla comparativa de alternativas

| Criterio de Evaluación | Alternativa 1: PWA Mobile-First con Tablero Visual | Alternativa 2: Chatbot Conversacional | Alternativa 3: Tótems Físicos en Campus |
| :--- | :--- | :--- | :--- |
| **Rapidez de reserva (< 45 s)** | **Alta:** Visualización directa y reserva en 3 toques. | **Media-Baja:** Requiere múltiples turnos de preguntas y respuestas. | **Media:** Rápida en pantalla, pero genera filas en horas punta. |
| **Disponibilidad y movilidad** | **Alta:** Accesible desde cualquier lugar del campus o antes de llegar. | **Alta:** Disponible desde el teléfono en cualquier ubicación. | **Baja:** Obliga a desplazarse físicamente hasta un tótem. |
| **Carga cognitiva y claridad** | **Baja:** Comparación simultánea de salas, horarios y capacidades mediante indicadores visuales. | **Media-Alta:** Dificulta comparar múltiples horarios y salas en un flujo lineal de texto. | **Baja:** Vista directa en pantalla grande, pero bajo presión de fila. |
| **Check-in y liberación anticipada** | **Alta:** Notificación push/web y liberación remota con un toque. | **Media:** Requiere volver a escribir comandos en el chat. | **Baja:** Exige volver físicamente al tótem para liberar la sala. |
| **Viabilidad técnica y costo** | **Alta:** Desarrollo web estándar, multiplataforma y sin hardware adicional. | **Media:** Depende de APIs de mensajería y procesamiento de lenguaje. | **Baja:** Requiere inversión en pantallas táctiles, lectores y mantención física. |

---

## 2.3 Justificación de la alternativa seleccionada

Se selecciona la **Alternativa 1: Aplicación Web Progresiva (PWA) Mobile-First con Tablero Visual** debido a que responde de manera óptima a las restricciones de tiempo, movilidad y claridad detectadas en el descubrimiento de requisitos:

1. **Minimiza el tiempo de interacción en hora punta:** A diferencia del chatbot (Alternativa 2), que obliga a recorrer un flujo secuencial paso a paso, el tablero visual permite escanear de un vistazo qué salas están libres y en qué bloques horarios, lo que la orienta a cumplir el requisito de reservar en menos de 45 segundos (RNF01), algo que se comprobará con usuarios en la evaluación.
2. **Elimina cuellos de botella físicos:** Frente a los tótems presenciales (Alternativa 3), el acceso desde el navegador del teléfono evita filas entre cambios de clase y permite que cualquier integrante del grupo reserve o libere la sala anticipadamente desde cafetería, patios o salas de clases.
3. **Baja fricción de adopción:** Al funcionar como aplicación web responsiva (sin descarga previa en tiendas de aplicaciones), cualquier estudiante puede ingresar de forma inmediata mediante su correo institucional o escaneando el código QR en la puerta de la sala.

## 2.4 Limitaciones de la alternativa seleccionada

La Alternativa 1 también tiene límites que el diseño debe considerar:

* **Depende de la conexión a internet.** Sin conexión no se puede ver el estado en tiempo real ni reservar, por lo que la interfaz debe avisarlo con claridad y conservar el pase ya emitido (apartado 6.5.1).
* **Las notificaciones requieren instalación.** En iPhone, los avisos de una PWA solo funcionan si el usuario la agrega a su pantalla de inicio, por lo que el aviso previo al término de la reserva no llega a todos por igual.
* **Exige un teléfono con navegador.** Quien no lo tenga a mano puede usar la misma interfaz desde un computador, pero pierde la ventaja del escaneo de QR junto a la sala.

## Referencias

* Rogers, Y., Sharp, H. y Preece, J. (2023). *Interaction Design: Beyond Human-Computer Interaction* (6.ª ed.). Wiley.
