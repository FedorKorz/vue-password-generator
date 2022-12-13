vue-password-generator
=====================

The project is on vue. Generates a password depending on the user's settings, the presence of symbols, numbers, uppercase letters. The background color changes depending on the complexity of the password. Depending on the position of the slider's slider, the user selects the password length. It is possible to copy to the clipboard.
***


Structure
-----------------------------------
```
├── build
│   ├── build.js
│   ├── check-versions.js
│   ├── logo.png
│   ├── utils.js
│   ├── vue-loader.conf.js
│   ├── webpack.base.conf.js
│   ├── webpack.dev.conf.js
│   └── webpack.prod.conf.js
├── config
│   ├── dev.env.js
│   ├── index.js
│   └── prod.env.js
├── index.html
├── package.json
├── package-lock.json
├── README.md
└── src
    ├── App.vue
    ├── assets
    │   └── logo.png
    ├── components
    │   ├── CheckBoxes.vue
    │   ├── PasswordBox.vue
    │   └── RangeSlider.vue
    ├── main.js
    └── store
        ├── Digits.vue
        ├── LowerCase.vue
        ├── Symbols.vue
        └── UpperCase.vue

```
Dependencies
-----------------------------------
* Vue

Install
-----------------------------------
* npm install
* npm start

Lve Demo 

[![output.gif](https://i.postimg.cc/2jvFGTs3/output.gif)](https://postimg.cc/K4GMv7vy)

[![Watch the video]](https://www.loom.com/share/4f5985ad63164b32a5070f05e2094dba)

