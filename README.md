# Installation of Tailwind_css


- you can refer files in repo for some idea


# Run this commands on terminal after navigating to your working directory:

``` npm install -D tailwindcss@latest postcss@latest autoprefixer@latest```

``` npx tailwindcss init ```



# Ensure that tailwind is installed run: 
``` npm tailwindcss -v ```



# In tailwind.config.js add:

```
 /** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./public/**/*.{html,js,jsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```


> Note: in above code src refers to the directory where you stored the code files like html,jsx etc so make sure to change it
> you can add more than one ["./public/**/*.{html,js,jsx}"],["./public/**/*.{html,js,jsx}"] like this



# add following code in index.css file in src directory:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
 ```


#add following code in package.jason:

```
"scripts": {
    "build:css": "tailwindcss -i ./src/style.css -o ./public/style.css",
    "watch:css": "tailwindcss -i ./src/style.css -o ./public/style.css --watch",
    "start": "concurrently \"npm run watch:css\" \"live-server public\""
  }
```

> make sure to change public directory name in above code which refers to the directory where we want to run code or where we stored them like html, etc.


# after that run:

```
npm run build:css
```
```
npm run watch:css
```

# And you are all set now just run following command whenever you want To start the development server and watch for CSS changes:

```
npm start
```

  
