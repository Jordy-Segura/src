# src

html


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Citas Médicas</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Citas Médicas</h1>
        <nav>
            <ul>
                <li><a href="#">Inicio</a></li>
                <li><a href="#">Servicios</a></li>
                <li><a href="#">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Formulario de Cita Médica</h2>
            <form id="citaForm">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required>
                
                <label for="correo">Correo Electrónico:</label>
                <input type="email" id="correo" name="correo" required>
                
                <label for="fecha">Fecha de la Cita:</label>
                <input type="date" id="fecha" name="fecha" required>
                
                <button type="submit">Enviar</button>
            </form>
        </section>
        
        <section>
            <h2>Ejercicio de Suma</h2>
            <input type="number" id="numero1" placeholder="Número 1">
            <input type="number" id="numero2" placeholder="Número 2">
            <button id="calcularBtn">Calcular Suma</button>
            <p id="resultado"></p>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2023 Citas Médicas. Todos los derechos reservados.</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>



css
:root {
    --color-fondo: #f4f4f4;
    --color-texto: #333;
    --color-boton: #007bff;
    --color-boton-hover: #0056b3;
    --color-header: #007bff;
    --color-footer: #333;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: var(--color-fondo);
}

header {
    background-color: var(--color-header);
    color: white;
    text-align: center;
    padding: 1rem 0;
}

nav ul {
    list-style-type: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav a {
    color: white;
    text-decoration: none;
}

nav a:hover {
    text-decoration: underline;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
    padding: 15px;
    background-color: white;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin: 5px 0;
}

form input {
    margin-bottom: 10px;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    padding: 10px;
    background-color: var(--color-boton);
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: var(--color-boton-hover);
}

footer {
    background-color: var(--color-footer);
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}


jv
function calcularSuma() {
    const num1 = parseFloat(document.getElementById('numero1').value);
    const num2 = parseFloat(document.getElementById('numero2').value);
    const resultado = num1 + num2;
    console.log('La suma es:', resultado);
    document.getElementById('resultado').innerText = 'La suma es: ' + resultado;
}

document.getElementById('calcularBtn').addEventListener('click', calcularSuma);
