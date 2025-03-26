<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Protegida</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #121212; /* Fondo oscuro */
            color: white; /* Texto blanco */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-container {
            background-color: #333; /* Fondo oscuro del contenedor */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            width: 300px;
            text-align: center;
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #555; /* Borde más oscuro */
            border-radius: 4px;
            background-color: #222; /* Fondo oscuro para el campo de texto */
            color: white; /* Texto blanco en el campo */
        }
        input::placeholder {
            color: #888; /* Color del texto del placeholder */
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        #error-message {
            color: red;
            display: none;
        }
    </style>
</head>
<body>

    <div class="login-container">
        <h2>Ingreso Protegido</h2>
        <input type="password" id="password" placeholder="Introduce la contraseña">
        <button onclick="checkPassword()">Ingresar</button>
        <p id="error-message">Contraseña incorrecta. Intenta de nuevo.</p>
    </div>

    <script>
        const correctPassword = "090909"; // Cambia esta contraseña por la que prefieras.

        function checkPassword() {
            const userPassword = document.getElementById('password').value;
            const errorMessage = document.getElementById('error-message');
            
            if (userPassword === correctPassword) {
                // Si la contraseña es correcta, redirige a la página.
                window.location.href = "http://localhost:8158/Indix.html"; // Cambia esta URL por la de tu página.
            } else {
                // Si la contraseña es incorrecta, muestra el mensaje de error.
                errorMessage.style.display = "block";
            }
        }
    </script>

</body>
</html>
