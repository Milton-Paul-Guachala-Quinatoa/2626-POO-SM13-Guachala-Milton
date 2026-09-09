# Restaurante App - Semana 13

## Estudiante
Milton Paul Guachala Quinatoa

## Descripción

Este proyecto corresponde a la actividad de la Semana 13 de la materia Programación Orientada a Objetos.

En esta semana trabajé en pasar la aplicación `restaurante_app` que tenía anteriormente en consola a una primera versión con interfaz gráfica utilizando Tkinter.

Para realizar esta parte tomé como referencia el ejemplo visto en clase y organicé el proyecto utilizando diferentes carpetas para separar los modelos, servicios, datos y las interfaces gráficas.

En esta versión estoy trabajando principalmente con los productos y usuarios del restaurante. La parte de ventas todavía queda pendiente para desarrollarla en las siguientes semanas.

## Estructura

```text
restaurante_app/
├── datos/
│   ├── productos.json
│   └── usuarios.json
├── modelos/
│   ├── __init__.py
│   ├── producto.py
│   └── usuario.py
├── servicios/
│   ├── __init__.py
│   ├── archivo_servicio.py
│   └── restaurante_servicio.py
├── ui/
│   ├── __init__.py
│   ├── login_view.py
│   └── main_view.py
└── main.py
```

## Flujo de la aplicación

Inicio → LoginView → validación mediante RestauranteServicio →
MainView → Productos / Usuarios / Ventas pendiente → Cerrar sesión → LoginView.

La aplicación utiliza una única ventana principal de Tkinter y un único
`mainloop()`.

## Funcionalidades implementadas

- Pantalla de inicio de sesión.
- Validación de credenciales mediante `RestauranteServicio`.
- Mensaje visual para campos vacíos.
- Mensaje visual para credenciales incorrectas.
- Visualización de productos cargados desde `productos.json`.
- Visualización de usuarios cargados desde `usuarios.json`.
- Opción de Ventas identificada como funcionalidad pendiente.
- Cierre de sesión dentro de la misma ventana.

## Credenciales de demostración

- Usuario: `Milton`
- Contraseña: `admin`

La autenticación es local y simulada con fines pedagógicos.

## Requisitos

- Python 3.x
- Tkinter disponible en la instalación de Python.
- No se requieren dependencias externas.

## Cómo ejecutar

Desde la carpeta `restaurante_app`:

```bash
python main.py
```

En Windows también puede utilizar:

```bash
py main.py
```
O ejecuta el archivo en VS Code haciendo clic en el botón 'Run Python File' para verlo en la terminal.
## Nota

Las vistas no leen directamente los archivos JSON. La información es solicitada
a `RestauranteServicio`, que utiliza `ArchivoServicio` para cargar los datos.
Las funcionalidades completas de ventas y otras operaciones del proyecto de
consola se incorporarán progresivamente en semanas posteriores.
