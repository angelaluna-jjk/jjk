# Contexto Administrativo
ADMINISTRACIÓN CENTRALIZADA: Al poseer una única sede, la administración centralizada es la estrategia más eficiente para la empresa porque garantiza que todos los procesos de venta y control de inventario operen bajo un mismo entorno. Esto evita que existan diferencias entre el stock físico de la sede y lo que muestra la tienda online, facilitando que el equipo interno supervise la seguridad de los activos y responda con agilidad ante cualquier falla técnica sin causar conflicto en la toma de decisiones.

# Modelado de Roles
1. Administrador General
- Acceso total a reportes financieros, márgenes de ganancia y balances de ventas de textiles.
- Gestión de cuentas bancarias y configuración de las cuentas receptoras del dinero.
- Alta, baja y asignación de roles para todos los empleados en el sistema.
- Poseedor de las credenciales maestras y llaves de producción de las APIs de Pago.
- Propiedad legal y acceso de recuperación del Dominio web.
- Capacidad de revocar accesos de emergencia en Servidores y Repositorios.

2. Gestor de Tienda
- Crear, modificar y eliminar productos del catálogo (subir fotos de telas, descripciones, precios y tallas).
- Controlar el inventario (actualizar los metros de tela o stock disponible en el almacén).
- Gestionar pedidos (cambiar estados a "Enviado", generar guías logísticas y procesar devoluciones).
- Ver datos de contacto de clientes únicamente para fines de envío.

3. Contador (Solo Lectura)
- Acceso de solo lectura al historial completo de transacciones financieras y facturación.
- Exportación de reportes de ventas para auditorías contables o pago de impuestos.
- Acceso de solo lectura a los registros de actividad (logs) para verificar quién entró al sistema y qué cambios hizo.
- Visualización de las configuraciones de seguridad para garantizar el cumplimiento de las normativas de protección de datos.

4. Líder de Desarrollo: Es el encargado de programar "lo que no se ve": las conexiones, el carrito de compras, el procesamiento de pagos y el inventario.

- Aprobación final en el Repositorio: Autorizar la unión de código nuevo (Merge/Pull Requests) a la versión oficial de la tienda.
- Control de accesos técnicos: Crear o dar de baja las cuentas de los programadores en el servidor o repositorio.
- Gestión de APIs: Configurar y actualizar las llaves de producción de las APIs de Pago (en coordinación con el Admin General).

5. Desarrollador Backend: Es el encargado de programar las conexiones, el carrito de compras, el procesamiento de pagos y el inventario.

- Escritura en Base de Datos: Crear nuevas tablas, modificar la estructura de los datos (ej: añadir un campo para "Tipo de Tela") y realizar mantenimientos.
- Conexión con APIs: Programar la integración de las pasarelas de pago y los servicios de las transportadoras en entornos de prueba.
- Escritura en el Repositorio: Subir código en sus ramas de trabajo correspondientes.

6. Desarrollador Frontend: Es el encargado de el diseño de la tienda, la pasarela visual de productos, los colores, botones y la experiencia móvil.

- Escritura limitada en el Repositorio: Modificar exclusivamente los archivos visuales y de diseño de la interfaz de la tienda.
- Sin acceso a Base de Datos: No tiene permisos para modificar datos sensibles, inventarios generales ni registros de ventas.
- Sin acceso al Servidor: No puede alterar la configuración del servidor de producción.

7. Ingeniero DevOps: Es el encargado de montar la infraestructura, los servidores y asegurar que la página web no se caiga cuando entren miles de clientes a comprar.

- Control total del Servidor de Despliegue: Configurar la memoria RAM, el procesador, las reglas de seguridad (Firewall) y los Certificados SSL de la tienda.
- Automatización de despliegues: Configurar los sistemas para que el código aprobado por el Líder se suba al servidor de forma segura.
- Gestión de Backups: Programar y verificar que las copias de seguridad de la Base de Datos se realicen de forma automática todos los días.

# Matriz RACI
<img width="751" height="442" alt="Screenshot 2026-05-19 233057" src="https://github.com/user-attachments/assets/e51a8736-17dd-4e88-bf99-21899ecfd65f" />

# Diccionario de Datos
<img width="1427" height="701" alt="image" src="https://github.com/user-attachments/assets/e67cbabc-d7c3-40dd-b7de-392a99108df4" />
<img width="1422" height="790" alt="image" src="https://github.com/user-attachments/assets/f80c3cfe-234c-48aa-a430-17d9b3091fb5" />
<img width="1556" height="575" alt="image" src="https://github.com/user-attachments/assets/8a0117a1-6f1a-4943-b02a-d73d38814930" />
<img width="742" height="562" alt="image" src="https://github.com/user-attachments/assets/696fb4e6-6248-4e41-a2c9-60df3c5d001d" />
<img width="816" height="610" alt="image" src="https://github.com/user-attachments/assets/29c2ab63-0950-437e-a426-700ac7621b15" />

# Validacion de Entrada
<img width="1117" height="778" alt="image" src="https://github.com/user-attachments/assets/9de6bbad-39a0-4ce5-a91c-4d4ab92d6ac1" />

# Arquitectura
<img width="964" height="527" alt="Screenshot 2026-05-23 174558" src="https://github.com/user-attachments/assets/15ee4a58-27bd-4cab-86ec-d66df94e6bd3" />

# Tipo de SI
Nuestro proyecto funciona de dos maneras. Primero, trabaja como un sistema TPS porque se encarga de registrar en el momento todo lo que pasa en el negocio cada día, como las ventas que hacen los clientes y el control de los productos que entran y salen del almacén. Segundo, también actúa como un sistema MIS porque junta toda esa información diaria y la convierte en reportes sencillos. Esto le permite al dueño revisar de forma rápida qué productos se venden más, cuánta mercancía queda en stock y cómo van las ganancias para poder tomar buenas decisiones en la empresa.





