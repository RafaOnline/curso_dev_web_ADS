# Lidando com dados provenientes de formulário HTTP

### Contextualização 
- Vamos considerar uma aplicação simples, que envole o ciclo requisição e resposta, mostrado a seguir;
- A página web tem um formulário de login e senha;

     <img width="373" height="125" alt="image" src="https://github.com/user-attachments/assets/7be902b4-353b-44b9-8c69-5df8c43ec0cb" />

- Ao inserir os dados de login e senha e acionar a tecla Enter, os dados serão levados na requisição ao servidor que hospeda a aplicação;
- O servidor lida com os dados e devolve a resposta, que é visualizada no navegador do usuário;

### Código da página Web

*Código simples para estudo
```html
<html>
<body>

  <form action="welcome.php" method="POST">
    Name: <input type="text" name="name"><br>
    E-mail: <input type="text" name="email"><br>
  <input type="submit">
  </form>

</body>
</html>
```

### Código de aplicação `welcome.php`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    
    Welcome <?php echo $_POST["name"]; ?><br>
    Your email address is: <?php echo $_POST["email"]; ?>
    
</body>
</html>
```
**Resultado**

  <img width="500" height="155" alt="image" src="https://github.com/user-attachments/assets/40cbf08a-2ae2-4673-92c8-1a2b4705efa8" />
