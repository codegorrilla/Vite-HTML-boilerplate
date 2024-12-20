### Vite HTML Boilerplate template - <small>made by codegorrilla</small>
![Vite-html](images/vite-html.png)
***

#### How to make the boilerplate-
1. Open terminal, type the below commands in order create a folder and get inside the folder

```bash
mkdir folder-name && cd folder-name
```
2. Initialize npm inside the folder
```bash
npm init -y
```
3. Install Vite front-end build tool as development only dependency
```bash
npm --save-dev vite
```
4. Install Sass compiler
```bash
npm --save-dev sass
```
5. Create a folder src, and inside it create two sub folders as-
```bash
mkdir {src,src/js,src/scss}
```
6. Now create following files as-
```bash
touch src/index.html src/js/main.js src/scss/styles.scss vite.config.js
```
7. Paste the following code inside vite.config.js in order to enable HMR via Vite, to create a local server and output the build files into a folder named dist-
```js
import { resolve } from 'path'

export default {
  root: resolve(__dirname, 'src'),
  build: {
    outDir: '../dist'
  },
  server: {
    port: 8080
  }
}
```
8. Now to run the local Vite server, we need to add the following npm script inside package.json file as-
```json
{
  // ...
  "scripts": {
    "start": "vite",
  },
  // ...
}
```
9. Now add the following HTML code inside the index.html file as-
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script type="module" src="./js/main.js"></script>
</head>
<body>
    
</body>
</html>
```
10. Add the following code inside the main.js file as-
```js
import '../scss/styles.scss';
```
11. Now run the project by typing the following command inside terminal
```bash
npm start
```
*<i>for macOS users only: in case if you face any issue in the terminal while running npm start like</i>
```bash
Expected identifier but found "import"
(define name):1:0:
1 │ import.meta.dirname
```
<i> use the following command in order to downgrade esbuild version as-</i>
```bash
npm i -D esbuild@0.24.0
```

12. Initialize Git in the project folder
```bash
git init
```

13. Add a .gitignore file in the root of the project folder 
```bash
touch .gitignore
```
and add following directories to exclude them while performing Git operations inside the .gitignore file as-
```bash
node_modules
.vscode/*
```

You're all set to move ahead :)





