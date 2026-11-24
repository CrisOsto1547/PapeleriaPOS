# PapeleriaPOS
Nombre del proyecto: PapeleriaPOS.
Negocio: Papelería.

Objetivo: Conformar el equipo de trabajo, definir el negocio y realizar el diseño inicial del sistema de punto de venta (POS).

Definición del negocio Nombre del negocio: Papelería POS.
Descripción:

Es un negocio dedicado a la venta de útiles escolares y artículos de papelería. Su objetivo es ofrecer productos a estudiantes, profesores y personas que necesiten materiales escolares y de oficina.

¿Qué vende?

Cuadernos.
Lápices y lapiceros.
Borradores y sacapuntas.
Carpetas y hojas.
Colores y marcadores.
Artículos de oficina.
Tipos de productos y precios:

Productos escolares: tienen un precio individual dependiendo del producto.
Productos de papelería al por mayor: tienen precios especiales cuando se compran en grandes cantidades.
Medios de pago aceptados:

Efectivo.
Transferencia bancaria.
Integrantes del equipo
Alejandro Acevedo.
Cristopher Osto.
Requisitos funcionales (RF1 a RF7)
Los requisitos funcionales indican las funciones que debe realizar el sistema.

RF1. Gestión de productos: El sistema debe permitir registrar, modificar, consultar y eliminar productos. Clase responsable: Producto.

RF2. Control de inventario: El sistema debe permitir controlar las existencias de los productos. Clase responsable: Producto.

RF3. Gestión de clientes: El sistema debe permitir registrar y administrar la información de los clientes. Clase responsable: Cliente.

RF4. Registro de ventas: El sistema debe permitir registrar las ventas realizadas. Clase responsable: Venta.

RF5. Comprobantes de venta: El sistema debe generar comprobantes de las ventas realizadas. Clase responsable: Venta.

RF6. Reportes: El sistema debe permitir generar reportes de ventas. Clase responsable: SistemaPOS.

RF7. Menú principal: El sistema debe mostrar un menú de opciones para facilitar su utilización. Clase responsable: Main. 2. Identificación de clases, atributos y métodos

Cliente
Atributos: nombre, documento y teléfono.

Métodos: registrarCliente(), consultarDatos(), modificarCliente() y eliminarCliente().

Producto
Atributos: código, nombre, precio y stock.

Métodos: registrarProducto(), consultarProducto(), modificarProducto(), eliminarProducto() y actualizarStock().

ProductoEscolar
Atributos: características escolares.

Métodos: calcularPrecio().

Esta clase hereda de Producto.

ProductoPapeleriaMayor
Atributos: cantidad mínima y descuento.

Métodos: calcularPrecio().

Esta clase hereda de Producto.

Venta
Atributos: número, fecha y total.

Métodos: registrarVenta(), calcularTotal() y generarComprobante().

ItemVenta
Atributos: producto, cantidad y subtotal.

Métodos: calcularSubtotal().

MetodoPago
Atributos: valor del pago.

Métodos: procesarPago().

Es una clase abstracta propuesta.

PagoEfectivo
Atributos: valor recibido.

Métodos: calcularCambio() y procesarPago().

Esta clase hereda de MetodoPago.

PagoTransferencia
Atributos: referencia.

Métodos: validarTransferencia() y procesarPago().

Esta clase hereda de MetodoPago.

SistemaPOS
Atributos: lista de productos, clientes y ventas.

Métodos: registrarProducto(), buscarProducto(), realizarVenta() y generarReporte().

Main
Método principal: main().

Se encarga de iniciar el programa y mostrar el menú principal. 3. Relaciones entre las clases

ProductoEscolar hereda de Producto.
ProductoPapeleriaMayor hereda de Producto.
PagoEfectivo hereda de MetodoPago.
PagoTransferencia hereda de MetodoPago.
Venta contiene varios ItemVenta.
ItemVenta se relaciona con Producto.
Venta se relaciona con Cliente.
Venta utiliza MetodoPago.
SistemaPOS administra productos, clientes y ventas.
Main inicia y utiliza SistemaPOS.
Requisitos técnicos (RT1 a RT11) RT1. Clases y objetos: Crear las clases y sus respectivos objetos para representar los elementos del negocio.
RT2. Encapsulamiento: Utilizar atributos privados mediante la palabra private para proteger la información.

RT3. Constructores y this: Inicializar los atributos mediante constructores y utilizar this para identificar los atributos del objeto.

RT4. Referencias y null: Manejar referencias entre objetos y valores nulos cuando sea necesario.

RT5. Paquetes: Organizar las clases en paquetes de ejecución, lógica y modelo.

RT6. ArrayList: Utilizar listas para almacenar productos, clientes y ventas.

RT7. Herencia: Utilizar extends para permitir que unas clases hereden características de otras.

RT8. Polimorfismo: Permitir diferentes comportamientos mediante métodos sobrescritos.

RT9. Abstracción: Utilizar clases abstractas o interfaces para organizar el funcionamiento del sistema.

RT10. Static: Utilizar atributos o métodos compartidos mediante la palabra static.

RT11. Relaciones: Establecer relaciones entre los diferentes objetos del sistema para permitir su funcionamiento conjunto.
