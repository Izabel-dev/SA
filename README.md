
A suíte é organizada em três seções principais:

---

## 🔹 1. Testes da Página de Cadastro

Validam:

- Presença e visibilidade dos elementos da interface  
- Campos obrigatórios (required)  
- Funcionamento do botão **Cadastrar**  
- Navegação através do link **"Já tem conta? Faça login"**  

### Exemplos de validações:
- Inputs visíveis  
- Campos obrigatórios configurados corretamente  
- Formulário impedindo envio com campos vazios  

---

## 🔹 2. Testes da Página de Login

Nesta seção são verificadas:

- Estrutura visual completa da página  
- Mensagens de erro em:
  - Campos vazios  
  - Usuário inexistente ou senha incorreta  
- Comportamento do link **"Esqueceu a senha?"**  
- Mensagens de sucesso ao realizar login  

### Exemplos de validações:
- Mensagem *"Por favor, preencha todos os campos.”*  
- Mensagem *"Usuário ou senha incorretos.”*  
- Mensagem temporária exibida ao clicar em *"Esqueceu a senha?"*  

---

## 🔹 3. Fluxo Completo — Cadastro → Login

O teste mais importante verifica o funcionamento completo do sistema:

1. Usuário acessa o **Cadastro**  
2. Preenche todos os campos obrigatórios  
3. Cadastra-se (dados salvos no LocalStorage)  
4. Abre a tela **Login**  
5. Faz login com os dados cadastrados  
6. Mensagem de sucesso é exibida  

Esse teste garante que as duas páginas funcionem integradas, simulando o uso real do FireLeaf.

---

## ⚙️ O Que os Testes Validam

Os testes cobrem várias camadas da aplicação:

- **HTML:** Campos, inputs, labels, botões  
- **CSS:** Estilos das mensagens (ex.: cor vermelha para erro)  
- **JavaScript:** Validações, mensagens, redirecionamento  
- **LocalStorage:** Registro de novos usuários  
- **Navegação:** Links e comportamentos de redirecionamento  

---

## 🧩 Como o Cypress Executa os Testes

Cada teste segue uma estrutura consistente:

### `beforeEach()`
- Limpa o LocalStorage  
- Carrega a página necessária  

### Comandos utilizados:
- `cy.visit()` – abre páginas  
- `cy.get()` – seleciona elementos  
- `cy.type()` – digita nos inputs  
- `cy.click()` – simula cliques  
- `cy.should()` – valida comportamentos  

Essas ações simulam precisamente o uso real do sistema.

---

## ⭐ Conclusão

A suíte de testes E2E criada garante que:

- As páginas principais funcionam como esperado  
- O usuário consegue se cadastrar e fazer login sem erros  
- Mensagens e validações funcionam corretamente  
- A aplicação mantém estabilidade e confiabilidade  

Esses testes são essenciais para o crescimento consistente e seguro do projeto **FireLeaf**.

---

## 🛠 Tecnologias Utilizadas

- **Cypress**  
- **HTML, CSS, JavaScript**  
- **LocalStorage** para simular banco de dados local  

---

## 📞 Contato

Caso deseje expandir os testes, adicionar Page Objects ou criar testes unitários:  
**Basta solicitar!**

🔥 *FireLeaf – Qualidade, confiabilidade e automação de testes.*
