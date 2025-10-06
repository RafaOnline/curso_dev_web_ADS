# 📋 Formulários em HTML

## 📌 Assuntos abordados nessa aula:
- Estrutura do formulário
- Elementos e atributos de um formulário
- Atributos de formlário: o atributo type
- Novos atributos e tipos de entrada

## Exemplo de formuário:
    <form action="/pagina-processa-dados-do-form" method="post">
    
    <fieldset>
      <legend>Dados gerais</legend>
  
      <label for="nome">Nome:</label>
      <input type="text" minlength="3" id="nome">
  
      <label for="data_nascimento">Data de nascimento</label>
      <input type="text" id="data_nascimento">
  
      <label for="cpf">CPF:</label>
      <input type="text" id="cpf">
    </fieldset>

    <fieldset>

      <legend>Endereço</legend>
  
      <label for="tipo_endereco" >Tipo:</label>
      <select id="tipo_endereco">
      <option value="">Selecione</option>
      <option value="">Rua</option>
      <option value="">Estrada</option>
      <option value="">Rodovia</option>
      <option value="">Avenida</option>
      <option value="">Outros</option>
      </select>
  
      <label for="logradouro" >Logradouro:</label>
      <input type="text" id="logradouro">
  
      <label for="numero" >Número</label>
      <input type="text" id="numero">
  
      <label for="complemento" >Complemeto:</label>
      <input type="text" id="complemento">

    </fieldset>

    <fieldset>

      <legend>Fale conosco</legend>
  
      <label for="mensagem">Mensagem:</label>
      <textarea id="mensagem">
  
      </textarea>

    </fieldset>

    <fieldset>

      <button type="submit">Enviar sua mensagem</button>
  
      <button type="reset">Limpar formulário</button>

    </fieldset>

    </form>

 Resultado:
<img width="955" height="239" alt="image" src="https://github.com/user-attachments/assets/6e45f96e-bdcb-47e2-b2ab-fc5ba2e20fc3" />

