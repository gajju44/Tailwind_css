# Installation of Tailwind_css


- you can refer files in repo for some idea
- you can also refer [ this site ](https://tailwindcss.com/docs/installation)



# Run this commands on terminal after navigating to your working directory:

``` npm install -D tailwindcss@latest postcss@latest autoprefixer@latest```

``` npx tailwindcss init ```



# Ensure that tailwind is installed run: 
``` npm tailwindcss -v ```



# In tailwind.config.js add:

```
 /** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./name/**/*.{html,js,jsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```


> Note: in above code name refers to the directory where you stored the code files like html,jsx etc so make sure to change it
> you can add more than one ["./name1/**/*.{html,js,jsx}"],["./name2/**/*.{html,js,jsx}"] like this



# add following code in style.css if you are in react you can add it to index.css file in src directory:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
 ```


#add following code in package.jason (no need in react):

```
"scripts": {
    "build:css": "tailwindcss -i ./src/style.css -o ./public/style.css",
    "watch:css": "tailwindcss -i ./src/style.css -o ./public/style.css --watch",
    "start": "concurrently \"npm run watch:css\" \"live-server public\""
  }
```

> you can add above code as it is 


# after that run (no need in react):

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

  
