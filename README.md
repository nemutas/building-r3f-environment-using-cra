# About
This page summarizes how to build the R3F（React Three Fiber） environment using CRA（Create React App）.

# CRA（Create React App）
in your project folder.
```
create-react-app . --template typescript --use-npm
```

# R3F（React Three Fiber）
```
npm i three @react-three/fiber @react-three/drei
```
```
npm i -D @types/three
```

# Collision
[use-cannon](https://github.com/pmndrs/use-cannon) is a library to give collisions to meshes.
```
npm i @react-three/cannon
```

# State management
[valtio](https://github.com/pmndrs/valtio) is used to pass state between canvas and dom elements.
```
npm i valtio
```

# Controller
[leva](https://github.com/pmndrs/leva) is a controller package for react.<br>
When the value of the controller changes, it will regenerate the associated components. This may cause animations using useFrame to be initialized.
```
npm i leva
```

[lil-gui](https://lil-gui.georgealways.com/) is a controller supported by threejs, but it is not optimized for react, so you will need to customize it.<br>
It is useful for referencing values in useFrames, as the component is not regenerated when the controller value changes.
```
npm i lil-gui
```

# Aniamtion
[gsap](https://greensock.com/) is an animation library that supports threejs objects.<br>
Of course, it can also be used to animate CSS styling.
```
npm i gsap
```

# Using GitHub Pages
By using [gh-pages](https://github.com/tschaub/gh-pages), you can deploy your application to github pages.
```
npm i -D gh-pages
```

Add the following settings to package.json.
```.json:package.json
"homepage": "https://<your name>.github.io/<your repository name>/",
"scripts": {
	"deploy": "npm run build && gh-pages -d build"
},
```

To deploy, execute the following command.
```
npm run build
```
※ Note: A repository must have been created in order to deploy.

# Styling
[@emotion/css](https://emotion.sh/docs/introduction) is a library for writing css using CSS in JS notation.<br>
The beauty is that it can be written directly in vanilla css notation.
```
npm i @emotion/css
```

If you are using vscode, you can install the extension [vscode-styled-components](https://marketplace.visualstudio.com/items?itemName=styled-components.vscode-styled-components) to enable code completion.
