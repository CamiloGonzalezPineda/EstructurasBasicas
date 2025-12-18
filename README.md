# Simple Header Website

Proyecto básico de una página web, navegación y estilos CSS aplicados para una presentación limpia y centrada.

---

## 📁 Estructura del proyecto

```bash
project/
├── .vscode/
├── src/
├── css/
│   └── index.css
├── js/
│   └── index.js
├── index.html
├── README.md


📄 index.html
Este archivo contiene la estructura principal del sitio web.
Incluye un encabezado (header) con un título y un menú de navegación.

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

🔎 Detalles importantes
Se utiliza una estructura semántica correcta (header, nav, ul, li)
El menú está preparado para navegación interna mediante anchors
El HTML es limpio y fácil de escalar

🎨 styles.css
Este archivo define los estilos globales del sitio y controla la apariencia del header y la navegación.

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