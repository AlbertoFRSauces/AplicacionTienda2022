# AplicacionTienda2022
Aplicación de una tienda online realizada para el proyecto final del curso.

## Autor: Alberto Fernandez Ramirez

**Fecha Inicio Proyecto: 27/04/2022**

**Ultima Actualización: 08/05/2022**

## Descripción 
Aplicación de una tienda online realizada para el proyecto final del curso.

## Funcionalidades
- La web contará con una cabecera y un pie común a todas las páginas que componen la aplicación (uso de includes/fragments), así como de un menú para la navegación entre las diferentes páginas de la web.
- Al acceder a la página inicial se mostrará el catálogo completo de productos (tabla Productos).
- En la página principal existirá un filtro de búsqueda de los productos del catálogo por diferentes características: búsqueda general, categoría (tabla Categorias).
- La tienda contará con un formulario de login, permitiendo al usuario de la aplicación logarse en todo momento (común a todos los roles).
- Existirán 3 roles de usuario (tabla Roles) además del rol por defecto ‘anónimo’ cuando el usuario no está logado.
- Si un usuario no está dado de alta, podrá registrarse en la aplicación a través del formulario correspondiente (tabla Usuarios), tomando el rol ‘cliente’ por defecto.
- Se simulará el proceso de compra (no es necesario enlazar con una pasarela de pago real), obligando al usuario a logarse antes de realizar el pedido (solo usuarios con el rol ‘cliente’).
- Los pedidos realizados (tabla Pedidos) podrán encontrarse en alguno de los siguientes estados: ‘pendiente envío’ (PE), ‘pendiente cancelación’ (PC), ‘enviado’ (E) o ‘cancelado’ (C) (campo estado).
- Inicialmente se dispondrá de dos métodos de pago: ‘tarjeta’ o ‘paypal’ (campo metodo_pago).
- Cada uno de los pedidos estará formado por varias líneas de pedido (tabla Detalles_pedido), asociadas cada una de estas a un producto y al número de unidades compradas de dicho producto.
- Una vez que el usuario está logado (uso de sesiones), la funcionalidad disponible, a través de las opciones del menú de la aplicación (tabla Opciones_menu), vendrá determinada por el rol de dicho usuario.

-----------------------------------------------------------------------------------------------------------------------------------

Anónimo - (Funcionalidad dependiendo del rol del usuario)
- Ver el catálogo de productos.
- Navegar a través del catálogo, pudiendo ver los detalles de los productos pinchando en cada uno de ellos desde la vista del catálogo.
- Añadir productos al carrito de la compra, tanto desde la vista del catálogo como desde la del detalle del producto.

Cliente - (Funcionalidad dependiendo del rol del usuario)
Además de las funciones descritas para el usuario con rol ‘anónimo’:
- Realizar pedido (proceso de compra).
- Ver historial de pedidos realizados (incluido el estado actual del pedido).
- Ver detalle del pedido.
- Cancelar pedido: podrá solicitar la cancelación total del pedido realizado (a través del historial de pedidos).
- Ver perfil de usuario (el suyo propio).

Empleado - (Funcionalidad dependiendo del rol del usuario)
- Gestionar productos (altas, actualizaciones).
- Gestionar clientes (altas, actualizaciones).
- Ver perfil de usuario (el suyo propio).
- Procesar pedidos: validará los pedidos de los clientes (cambio de estado del pedido de ‘pendiente envío’ a ‘enviado’).

Administrador - (Funcionalidad dependiendo del rol del usuario)
Además de las funciones descritas para el usuario con rol ‘empleado’:
- Gestionar productos (bajas lógicas).
- Gestionar clientes (bajas lógicas).
- Gestionar empleados (altas, actualizaciones, bajas lógicas).
- Procesar cancelaciones: validará las cancelaciones de los pedidos solicitadas por los clientes (cambio de estado del pedido de ‘pendiente cancelación’ a ‘cancelado’).

-----------------------------------------------------------------------------------------------------------------------------------

- Se creara una factura, únicamente se poblará cuando el pedido pase a estado ‘enviado’, de la misma forma que el total de la factura (tabla Pedidos).
- Encriptación de la contraseña: se realizará una encriptación de la clave de acceso en el proceso de alta de los usuarios.
- Validaciones de datos: se realizarán comprobaciones de los datos introducidos por los usuarios, tanto en el lado del cliente como en el lado del servidor (en un solo formulario).

Cliente - (Funcionalidad dependiendo del rol del usuario)
- Modificar perfil de usuario (el suyo propio), sin incluir la contraseña de acceso a la aplicación.

-----------------------------------------------------------------------------------------------------------------------------------

- Descargar factura del pedido en pdf: solo pedidos en estado ‘enviado’.
- Adaptación al tamaño de la pantalla (responsive): la vista será adaptable a un mínimo de 3 tamaños diferentes de pantalla (móvil, tableta y pc).
- Se hará uso de una plantilla de Bootstrap para la maquetación de las vistas de la aplicación.
- Doble validación de contraseña: tanto en el proceso de alta de los usuarios (todos los roles) como en el cambio de contraseña (rol ‘cliente’).
- Creación de la documentación del proyecto: diagrama de base de datos, Javadoc.

Administrador - (Funcionalidad dependiendo del rol del usuario)
Además de las funciones descritas para el usuario con rol ‘empleado’:
- Gestionar administradores (altas, actualizaciones, bajas lógicas): solo el usuario ‘admin’ (superadministrador).

## Front end
- HTML
- CSS
- JavaScript

## Back end
- Java 8
