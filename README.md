vue-password-generator
=====================

Проект на vue. Генерирует пароль в зависимости от настроек пользователя, наличие символов, цифр, буквы верхнего регистра. Цвет фона меняется в зависимости от сложности пароля. В зависимости от положения ползунка slider'а пользователь выбирает длину пароля. Есть возможность копирования в буфер обмена. 
***


Структура проекта. 
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
Список использованных технологий
-----------------------------------
* Vue

Установка
-----------------------------------
* npm install
* npm start
