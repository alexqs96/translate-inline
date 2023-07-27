# Language Switcher

## Functions
- #### Load Language: This function loads the specified language for translation.
- #### Switch for Language: This function allows you to switch between the available languages.

## Installation

### To use the Language Switcher, you need to provide the languages you want to support in the translateOptions variable inside the `<script>` tag in the `<head>` section of your HTML.

- ### Requirements
- #### The first language in the list will be considered your default language.
- #### You need to include at least two languages (your default language and another one). For example: ["en","es"]

```html
<head>
  ...
  <script>
      const translateOptions = ["en", "es", "pt", "fr"];
  </script>
</head>
```

## And add the script translate-inline.js inside your `<body>` tag

```html
<body>
  ...
  <script src="translate-inline.js"></script>
</body>
```

## Usage

### To translate content, add the translations to the respective data attributes in the HTML tags you want to translate.

```html
  <p
    data-en="Hello"
    data-es="Hola"
    data-pt="Oi"
    data-fr="Salut"
  >
    Hello
  </p>
```

## Buttons

### The script provides two controls to switch between languages.

### Single Translation: This button works only for two languages (your default language and one other language). 
### To use this switcher, simply add the id "singleTranslation" to your button or image, and it will work as a switcher.

```html

<button id="singleTranslation">
  Change Language
</button>

```

### Multiple Translation: This control works with a `<select>` element and applies the first language of translateOptions as the selected language by default and changes when another language is selected.
### This method is suitable when you have multiple languages to choose from.

```html

  <select id="multipleTranslation">
    <option value="en">english</option>
    <option value="es">spanish</option>
    <option value="pt">portuguese</option>
    <option value="fr">french</option>
  </select>

```

## Show selected language

### To display the selected language, simply add the id "currentLanguage" to any HTML tag, and it will be updated every time the language changes.

```html

<p id="currentLanguage">en</p>

```

### Important: this method might increase your HTML size, but it can make managing translations on your page easier.
### Any suggestions or improvements are welcome! Feel free to check out my portfolio to contact me.