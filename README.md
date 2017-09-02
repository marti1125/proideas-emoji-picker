# proideas-emoji-picker

modificacion del plugin [emoji-picker](https://github.com/OneSignal/emoji-picker/)

### Instalación y Uso:

1. Dentro de la sección `<head>` agregar los siguientes estilos

  ```
  <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css" rel="stylesheet">
  <link href="./css/emoji.css" rel="stylesheet">
  ```

2. Antes de terminar la seccion del `<body>` agregar los siguientes scripts: (No olvidar agregar [jQuery](http://jquery.com/download/))

  ```
  <!-- ** No olvidar agregar jQuery aquí ** -->
  <script src="./js/config.js"></script>
  <script src="./js/util.js"></script>
  <script src="./js/jquery.emojiarea.js"></script>
  <script src="./js/emoji-picker.js"></script>
  ```

3. Agregar a cualquier `<input>` el siguiente atributo `data-emojiable="true"`

  ```
  <input type="text" data-emojiable="true" />
  ```

4. Finalmente agregamos el siguiente **script** para que funcione nuestros emojis

  ```
  $(function() {
    window.emojiPicker = new EmojiPicker({
      emojiable_selector: '[data-emojiable=true]',
      assetsPath: '../img/',
      popupButtonClasses: 'fa fa-smile-o'
    });
    window.emojiPicker.discover();
  });
  ```
