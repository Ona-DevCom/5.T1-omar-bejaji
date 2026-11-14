
# 2. Software Requirements Specification

<!-- Priority: Must, Should, Could or Won't (MoSCoW). -->
<!-- Every requirement must be verifiable and have an acceptance criterion. -->

## 2.1. Functional requirements

| ID | Requirement | Priority | Acceptance criterion |
|---|---|---|---|
| FR-01 | El sistema permitirá a los usuarios consultar las pistas deportivas disponibles por fecha, hora y deporte. | Must | Al seleccionar una fecha, hora y deporte, el sistema muestra las pistas disponibles. |
| FR-02 | El sistema permitirá a los usuarios realizar reservas de pistas deportivas. | Must | Un usuario puede seleccionar una pista y un horario disponible y obtener una reserva registrada. |
| FR-03 | El sistema permitirá al personal de recepción crear reservas en nombre de usuarios que no utilizan Internet. | Must | El personal puede registrar una reserva desde el ordenador de recepción y consultar sus datos. |
| FR-04 | El sistema impedirá reservar una pista que ya tenga una reserva confirmada en el mismo horario. | Must | Al intentar realizar una reserva duplicada, el sistema rechaza la solicitud y muestra un mensaje de error. |
| FR-05 | El sistema respetará la duración de cada actividad: 90 minutos para pádel y 60 minutos para tenis y fútbol sala. | Must | Al seleccionar cada deporte, el sistema asigna automáticamente la duración correspondiente. |
| FR-06 | El sistema permitirá reservar con una semana de antelación. La nueva semana se abrirá cada lunes a las 08:00. | Must | Antes de la apertura semanal no se pueden reservar los nuevos horarios; a partir del lunes a las 08:00 sí. |
| FR-07 | El sistema bloqueará los horarios reservados para las escuelas deportivas municipales. | Must | Los horarios fijos de las escuelas aparecen como no disponibles para el público. |
| FR-08 | El personal podrá cerrar pistas por mantenimiento o lluvia y gestionar las reservas afectadas. | Must | Al cerrar una pista, el sistema impide nuevas reservas y muestra las reservas afectadas. |
| FR-09 | El sistema calculará el precio de las reservas de los residentes a razón de 4 € por hora. | Must | Una reserva de pádel de 90 minutos para un residente tiene un precio base de 6 €. |
| FR-10 | El sistema añadirá un suplemento de 1 € a las reservas de pistas exteriores que se realicen después de las 20:00. | Must | Una reserva de una pista exterior después de las 20:00 muestra un suplemento adicional de 1 € en el precio total. |
| FR-11 | Los usuarios podrán cancelar sus reservas hasta 12 horas antes de su inicio. | Must | Una cancelación realizada 13 horas antes se acepta, mientras que una realizada 11 horas antes se rechaza. |
| FR-12 | El sistema permitirá pagar las reservas en recepción, antes de jugar, en efectivo o con tarjeta. | Must | El personal puede registrar un pago en efectivo o con tarjeta y consultar el estado del pago. |
| FR-13 | El sistema permitirá tener un máximo de tres reservas activas por persona. | Must | Un usuario con tres reservas activas no puede crear una cuarta reserva. |
| FR-14 | El personal de recepción podrá marcar una reserva como no presentada (no-show). | Must | El personal puede registrar el estado no-show de una reserva y el sistema actualiza el contador del usuario. |
| FR-15 | El sistema bloqueará las nuevas reservas de un usuario después de tres no-shows durante un mes. | Must | Después del tercer no-show, el usuario no puede reservar durante un mes. |
| FR-16 | El sistema permitirá consultar estadísticas sobre el uso de las pistas y los ingresos mensuales. | Should | El administrador puede consultar un informe con el número de reservas por pista y los ingresos mensuales registrados. |
| FR-17 | El sistema enviará notificaciones a los usuarios afectados cuando una pista se cierre por lluvia o mantenimiento. | Should | Al cerrar una pista con reservas, los usuarios afectados reciben una notificación. |

## 2.2. Non-functional requirements

| ID | Requirement | Priority | Acceptance criterion |
|---|---|---|---|
| NFR-01 | La página web será responsive y podrá utilizarse desde teléfonos móviles, tabletas y ordenadores. | Must | La página se visualiza correctamente en los tres tipos de dispositivos sin desplazamiento horizontal innecesario. |
| NFR-02 | La aplicación será accesible para personas con discapacidad visual y compatible con lectores de pantalla. | Must | Los campos del formulario tienen etiquetas accesibles y pueden utilizarse con un lector de pantalla. |
| NFR-03 | La interfaz estará disponible en español e inglés. | Should | El usuario puede cambiar el idioma y visualizar los textos de la interfaz en ambos idiomas. |
| NFR-04 | El sistema proporcionará información clara sobre el resultado de cada operación. | Must | Al reservar, cancelar o pagar, el sistema muestra un mensaje que confirma el resultado de la operación. |
| NFR-05 | El sistema protegerá los datos personales de los usuarios frente a accesos no autorizados. | Must | Un usuario no autorizado no puede consultar ni modificar los datos personales de otros usuarios. |
| NFR-06 | La aplicación deberá soportar el aumento de solicitudes durante la apertura semanal de reservas. | Must | Una prueba de carga realizada el lunes a las 08:00 permite procesar las solicitudes sin errores de disponibilidad ni reservas duplicadas. |

## 2.3. System requirements

| ID | Requirement | Priority | Acceptance criterion |
|---|---|---|---|
| SR-01 | La aplicación se instalará en los servidores del ayuntamiento, que utilizan el sistema operativo Linux. | Must | La aplicación se despliega y funciona correctamente en los servidores Linux municipales. |
| SR-02 | La base de datos del sistema utilizará PostgreSQL. | Must | La aplicación puede almacenar, consultar y actualizar las reservas en una base de datos PostgreSQL. |
| SR-03 | El sistema utilizará las copias de seguridad nocturnas de los servidores municipales para proteger los datos. | Must | Una prueba de restauración permite recuperar los datos guardados en una copia de seguridad. |
