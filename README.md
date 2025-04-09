<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Painel Premium - Pagamento</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #141414;
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    .container {
      background-color: #1f1f1f;
      padding: 30px;
      border-radius: 10px;
      width: 90%;
      max-width: 400px;
      box-shadow: 0 0 15px rgba(0,0,0,0.5);
    }
    h1 {
      text-align: center;
      color: #e50914;
    }
    input, select, button {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    input {
      background-color: #333;
      color: #fff;
    }
    button {
      background-color: #e50914;
      color: #fff;
      cursor: pointer;
    }
    button:hover {
      background-color: #bf0812;
    }
    .plan {
      background-color: #2a2a2a;
      padding: 10px;
      border-radius: 5px;
      margin-top: 15px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Painel Premium</h1>
    <form>
      <input type="text" placeholder="Nome completo" required>
      <input type="email" placeholder="E-mail" required>
      <select required>
        <option value="">Escolha um plano</option>
        <option value="83.99">Plano Mensal Premium – R$83,99</option>
        <option value="20.00">Plano Básico – R$20,00</option>
      </select>
      <button type="submit">Pagar com Cartão de Débito</button>
    </form>
  </div>
</body>
</html>
