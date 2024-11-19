<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/css-modules/css-modules/assets/9113740/f0de16c6-aee2-4fb7-8752-bf400cc5145e">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/css-modules/logos/master/css-modules-logo.png">
  <img alt="Logotipo de CSS Modules" src="https://raw.githubusercontent.com/css-modules/logos/master/css-modules-logo.png" width="150" height="150">
</picture>

# CSS Modules

Un **CSS Module** es un archivo CSS donde todos los nombres de clases y animaciones están delimitados de manera local por defecto. Todas las URL (`url(...)`) y `@imports` están en formato de solicitud de módulo (`./xxx` y `../xxx` significan rutas relativas, mientras que `xxx` y `xxx/yyy` se refieren a la carpeta de módulos, es decir, `node_modules`).

CSS Modules se compilan a un formato de intercambio de bajo nivel llamado ICSS (o [Interoperable CSS](https://github.com/css-modules/icss)), pero se escriben como archivos CSS normales:

```css
/* style.css */
.className {
  color: green;
}
```

Al importar un **CSS Module** desde un módulo JavaScript, este exporta un objeto con todos los mapeos de nombres locales a nombres globales.

```js
import styles from './style.css';

element.innerHTML = '<div class="' + styles.className + '">';
```

## Tabla de Contenidos

- [Comenzar y Ejemplos](/docs/get-started.md)
- [Nomenclatura](/docs/naming.md)
- [Composición](/docs/composition.md)
- [Alcance Local](/docs/local-scope.md)
- [Historia](/docs/history.md)
- [Selectores de Pseudo-Clases](/docs/pseudo-class-selectors.md)
- [Temas](/docs/theming.md)

## ¿Por qué CSS Modules?

- **El Alcance Local Evita Conflictos:** CSS Modules utiliza alcance local para evitar conflictos de estilos entre diferentes partes de un proyecto, permitiendo estilos específicos por componente.
- **Dependencias de Estilo Claras:** Importar estilos en sus respectivos componentes aclara qué estilos afectan a qué áreas, mejorando la legibilidad y el mantenimiento del código.
- **Resuelve Problemas del Alcance Global:** CSS Modules previene el problema común de que los estilos en un archivo afecten a todo el proyecto, localizando los estilos en componentes específicos.
- **Mejora la Reutilización y Modularidad:** CSS Modules permite usar los mismos nombres de clases en diferentes módulos, promoviendo estilos modulares y reutilizables.
```
