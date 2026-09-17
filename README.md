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
