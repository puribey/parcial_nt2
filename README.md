# parcial_nt2

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

## Objetivos

- Crear una aplicación frontend basada en Vue CLI 2 que permita ingresar un texto
  mediante un elemento de entrada y que sea representado por debajo del mismo de
  cinco formas diferentes:

1. Codificado: se hará cambiando las vocales de la siguiente forma: a por u, e por o,
   la i queda igual, o por e y u por a. Considerar pasar el texto ingresado a minúscula
   antes de realizar el cambio.
2. Todo en mayúscula.
3. Todo en minúscula.
4. Minúsculas y mayúsculas intercaladas, empezando por mayúscula.
5. Minúsculas y mayúsculas intercaladas, empezando por minúscula.

- Representar también por debajo del input, utilizando una propiedad computada, la
  cantidad de caracteres que se van ingresando. Las actualización de todos los mensajes
  tienen que ser en el mismo momento del ingreso de información.
- Definir un componente que contenga esta función y que sea llamado desde el
  componente principal. Usar en lo posible filtros de vista para realizar la conversión
  del texto ingresado.
