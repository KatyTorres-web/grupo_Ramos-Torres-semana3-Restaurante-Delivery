# Sumaq · Cocina peruana y delivery en Huancayo

## Integrantes

* Torres Ambrosio Katherine Medally
* Ramos Tacza Camilda

## Tema del proyecto

Restaurante de cocina peruana y servicio de delivery en Huancayo.

La página web presenta la propuesta del restaurante, su menú, opciones de reserva y servicio de delivery, utilizando un diseño responsive para dispositivos de escritorio y móviles.

## Tecnologías utilizadas

* HTML5
* Bootstrap 5.3.3
* Tailwind CSS
* JavaScript
* Git
* GitHub

## Combinación de Bootstrap y Tailwind CSS

En el proyecto se utilizaron Bootstrap y Tailwind CSS de manera complementaria.

Bootstrap se utilizó principalmente para componentes y estructuras responsivas, como el sistema de navegación, el grid y los estilos de formularios.

Tailwind CSS se utilizó para aplicar clases de utilidad relacionadas con espaciado, sombras, bordes redondeados, transiciones, gradientes y otros aspectos visuales.

Para evitar conflictos entre ambos frameworks se desactivó `Preflight` de Tailwind mediante `corePlugins: { preflight: false }`. De esta manera, Bootstrap mantiene sus estilos base y Tailwind se utiliza principalmente mediante sus clases de utilidad.

## Organización del trabajo

* `Torres-Ambrosio`: implementación de los pasos 1, 2 y 3.
* `Ramos-Tacza`: implementación de los pasos 4, 5 y 6.
* `main`: rama de integración final del proyecto.

Cada integrante desarrolló sus actividades en su propia rama y posteriormente realizó un Pull Request hacia `main` para su revisión e integración.


## Conflictos de especificidad entre Bootstrap y Tailwind CSS

Durante la implementación de la interfaz se presentó un conflicto entre los estilos base de Bootstrap y Tailwind CSS, principalmente relacionado con los estilos globales que Tailwind aplica mediante su mecanismo `Preflight`. Estos estilos podían modificar el comportamiento visual de componentes que pertenecen a Bootstrap, como la barra de navegación.

Para resolverlo, se desactivó `Preflight` en la configuración de Tailwind mediante:

```javascript
corePlugins: {
    preflight: false
}
```

De esta manera, Bootstrap mantiene sus estilos base y componentes, mientras que Tailwind se utiliza principalmente para aplicar clases de utilidad.

También se presentó un problema de visibilidad en el menú de navegación. Para solucionarlo se reforzó mediante CSS propio la visibilidad del contenido del `navbar-collapse`, evitando que los estilos de ambos frameworks afectaran su visualización.

En la sección Hero se mantuvo la separación de responsabilidades entre ambos frameworks: Bootstrap se utilizó para la tipografía y el sistema de layout (`display-3`, `lead`, `d-flex` y `gap-3`), mientras que Tailwind se utilizó para las utilidades visuales (`text-balance`, `max-w-3xl` y `bg-gradient-to-r`).

De esta forma, ambos frameworks pueden utilizarse de manera conjunta sin reemplazar completamente uno por otro.
