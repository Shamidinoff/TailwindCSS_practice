### Tailwind CSS - Practice

documentation

### Install Tailwind CSS

npm install -D tailwindcss
npx tailwindcss init

### tailwind.config.js - Configure your template paths

/** @type {import('tailwindcss').Config} \*/
module.exports = {
content: ["./src/**/\*.{html,js}"],
theme: {
extend: {},
},
plugins: [],
}

or other example

/\*_ @type {import('tailwindcss').Config} _/
module.exports = {
content: ["./index.html"],
theme: {
extend: {},
},
plugins: [],
};

## package.json file

{
"name": "tailwind",
"version": "",
"description": "",
"main": "index.js",
"scripts": {
"build": "tailwindcss build -i src/main.css -o public/styles.css --watch"
},
"author": "",
"license": "ISC",
"devDependencies": {
"postcss": "^8.4.31",
"tailwindcss": "^3.3.5"
}
}

(--watch чтобы не запускать генерацию стилей каждый раз, то есть npm run build)

## Add the Tailwind directives to your CSS

create folder src and file input.css or main.css (src/input.css) and put this below

@tailwind base;
@tailwind components;
@tailwind utilities;
