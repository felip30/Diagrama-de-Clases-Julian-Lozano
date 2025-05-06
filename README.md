# Diagrama-de-Clases-Julian-Lozano
# 🏗 Diagrama de Clases  

## 📜 Descripción  
Este documento describe la arquitectura del sistema a través de un **diagrama de clases**, mostrando las entidades clave, sus atributos, métodos y relaciones.  

## 🛠 Clases y Propiedades  
A continuación se detallan las clases principales y sus elementos:  

### 🔹 **Administrador**  
- `idAdmin: int` → Identificador único.  
- `nombre: string` → Nombre del administrador.  
- `correo: string` → Email de contacto.  
- **Métodos:**  
  - `agregarUsuario()`  
  - `configurarParametros()`  
  - `modificarSeguridad()`  

### 🔹 **Usuario**  
- `idUsuario: int`  Identificador único.  
- `nombre: string`  Nombre del usuario.  
- `correo: string`  Email del usuario.  
- `telefono: string`  Teléfono de contacto.  
- `rol: string` → Tipo de usuario (Cliente, Admin, etc.).  
- **Métodos:**  
  - `registrarUsuario()`  
  - `validarSesion()`  
  - `recuperarContraseña()`  

### 🔹 **Pedido**  
- `idPedido: int` → Identificador único.  
- `fechaPedido: date`  Fecha de creación.  
- `montoTotal: float`  Valor total del pedido.  
- `estadoPedido: string`  Estado actual.  
- **Métodos:**  
  - `crearPedido()`  
  - `actualizarEstadoPedido()`  
  - `consultarPedido()`  

### 🔹 **Producto**  
- `idProducto: int`  Identificador único.  
- `nombre: string`  Nombre del producto.  
- `descripcion: string`  Detalles del producto.  
- `cantidad: int` → Stock disponible.  
- `disponibilidad: string`  Estado del producto. 
- **Métodos:**  
  - `agregarProducto()`  
  - `modificarProducto()`  
  - `eliminarProducto()`  
  - `consultarProducto()`  
  - `actualizarStock()`  

## 🔗 Relaciones entre Clases  
El diagrama establece las siguientes relaciones:  
- **Asociación:** `Administrador → Usuario`  
- **Dependencia:** `Pedido → Factura`  
- **Herencia:** `Usuario` hereda de `Cliente`  

## 📌 Consideraciones  
- El diagrama debe actualizarse si hay modificaciones en la estructura de la base de datos.  
- Se recomienda seguir **principios de diseño orientado a objetos** para mantener la escalabilidad del sistema.  

