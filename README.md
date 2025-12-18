# Simple Header Website

Proyecto básico de una página web con un header, menú de navegación y estilos CSS aplicados para una presentación limpia y centrada.

Estructura del proyecto:
```
project/
├── .vscode/
├── src/
├── css/
│   └── index.css
├── js/
│   └── index.js
├── index.html
└── README.md

```
Código HTML (index.html):
```html
<header>
  <h1>Welcome to My Website</h1>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
```

Este HTML utiliza una estructura semántica correcta (header, nav, ul, li). El menú está preparado para navegación interna mediante anchors y el código es limpio y fácil de escalar.

Código CSS (index.css):
```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  background-color: #f4f4f4;
}

header {
  width: 100%;
  background-color: #ffffff;
  color: #000000;
  text-align: center;
}

h1 {
  padding: 20px;
}

nav ul {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  list-style: none;
  gap: 20px;
}

a {
  text-decoration: none;
  color: #000000;
}
```
Proyecto base funcional para practicar HTML semántico y Flexbox, pensado como punto de partida para futuros desarrollos Front-End.
