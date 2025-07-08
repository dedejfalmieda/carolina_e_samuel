# carolina_e_samuel
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Confirmar Presença</title>
  <style>
    body {
      font-family: sans-serif;
      max-width: 400px;
      margin: 40px auto;
      padding: 20px;
      background-color: #fff8f8;
      border: 2px solid #8b0000;
      border-radius: 10px;
    }
    h1 {
      color: #8b0000;
      text-align: center;
    }
    input[type="text"] {
      width: 100%;
      padding: 12px;
      margin-top: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      margin-top: 20px;
      width: 100%;
      background-color: #8b0000;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Confirme sua Presença</h1>
  <form id="formulario">
    <input type="text" id="nome" placeholder="Seu nome completo" required />
    <button type="submit">Confirmar</button>
  </form>

  <script>
    document.getElementById("formulario").addEventListener("submit", function(event) {
      event.preventDefault();
      const nome = document.getElementById("nome").value;
      const destino = "carolinajfalmeida@gmail.com";
      const assunto = "Confirmação de Presença";
      const corpo = `Olá, meu nome é ${nome} e estou confirmando presença no casamento!`;

      window.location.href = `mailto:${destino}?subject=${encodeURIComponent(assunto)}&body=${encodeURIComponent(corpo)}`;
    });
  </script>
</body>
</html>
