# Simple Header Website

# LINK

https://camilogonzalezpineda.github.io/EstructurasBasicas/

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
## Código HTML (index.html):
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

## Código CSS (index.css):
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
Estructura semántica correcta usando main y section, ideal para SEO y accesibilidad. Cada sección representa un bloque independiente del contenido.
```html
<main>
  <section class="home">
    <h2>Home Section</h2>
    <p>This is the home section of the website.</p>
  </section>

  <section class="about">
    <h2>About Section</h2>
    <p>This section contains information about us.</p>
  </section>

  <section class="contact">
    <h2>Contact Section</h2>
    <p>This section provides contact information.</p>
  </section>
</main>
```


## Estilos CSS del layout principal

Se utiliza Flexbox para alinear horizontalmente las secciones y mantener un espaciado consistente.

```css
main {
  width: 100%;
  height: 400px;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}

h2 {
  color: #000000;
}
```
# Estilos y animaciones por sección

## Home
```css
.home {
  width: 200px;
  height: 200px;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 20px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 1px 2px 10px rgb(0, 0, 0, 0.7);
  transition: transform 1s ease-in-out;
  cursor: pointer;
}

.home:hover {
  transform: scale(1.1);
}

```

## About
```css
.about {
  width: 220px;
  height: 220px;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 20px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 1px 2px 10px rgb(0, 0, 0, 0.7);
  transition: transform 0.5s ease-in-out;
  cursor: pointer;
}

.about:hover {
  transform: translateY(-10px);
}
```
## Contact + animación 3D

```css
.contact {
  width: 240px;
  height: 240px;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 20px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 1px 2px 10px rgb(0, 0, 0, 0.7);
  transition: transform 1s ease-in-out;
  cursor: pointer;
}

.contact:hover {
  transform: scale(1.1);
  animation: gira 2s linear infinite;
}

```

## Keyframes

```css

@keyframes gira {
  0% {
    transform: rotateY(0deg);
  }

  100% {
    transform: rotateY(360deg);
  }
}

```

## Estructura HTML (sección desplegable con botón)

```html
<section class="desplegarse">
  <button class="abriendo" id="click">Clickeame</button>
  <div class="desplegan" id="desplegar">
    <p>Home</p>
    <p>About</p>
    <p>Contact</p>
  </div>
</section>
```
## Estilos

```css
.desplegarse {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 100%;
  height: 200px;
  background-color: #ffffff;
  color: #e70606;
  overflow: hidden;
  padding: 20px;
  gap: 10px;
}

.desplegan {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 90%;
  height: 0px;
  background-color: #ffffff;
  box-shadow: 1px 2px 10px rgba(0, 0, 0, 0.7);
  color: #000000;
  overflow: hidden;
  transition: height 0.3s ease;
  gap: 10px;
  border-radius: 10px;
}

.desplegan.abrir {
  height: 200px;
}

.abriendo {
  width: 120px;
  height: 40px;
  background-color: #000000;
  color: #ffffff;
  cursor: pointer;
  border-radius: 10px;
  flex-shrink: 0;
}

```

## JavaScript para activar el menú

```js
const click = document.getElementById('click');
const abrir = document.getElementById('desplegar');

click.addEventListener('click', () => {
  abrir.classList.toggle('abrir');
});

```

## Footer
```html
<footer>
  <p>&copy; 2024 My Website</p>
</footer>

```

## Estilos Fotter

```css
footer {
  width: 100%;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #ffffff;
  color: #000000;
  text-align: center;
}
```