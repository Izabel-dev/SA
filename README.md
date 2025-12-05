

 **Documentação dos Testes E2E — FireLeaf (Cypress)**

**Tecnologias Utilizadas:**

Os testes automatizados da aplicação FireLeaf foram desenvolvidos utilizando:

✔ **Cypress.io**
Framework moderno de testes E2E
Permite simular ações reais do usuário
Executa em ambiente controlado dentro do navegador
Oferece asserts, mocks, inspeção visual e time-travel
Ideal para validar interfaces web e fluxos completos

✔ **JavaScript**
Utilizado para escrever os testes Cypress

✔ **HTML, CSS e JavaScript da Aplicação**
Cada página testada depende dos elementos construídos na interface
Validações JS e LocalStorage também são testadas

✔ **LocalStorage**
Usado como simulação de banco de dados de usuários
Cypress testa leitura, escrita e comportamento desses dados



 **Descrição Geral da Suíte de Testes**

Toda a suíte foi construída para validar todas as principais páginas e funcionalidades da plataforma FireLeaf, cobrindo:

* Estrutura visual das páginas
* Funcionalidade dos formulários
* Comportamento de validações obrigatórias
* Redirecionamentos simulando o fluxo real
* Armazenamento no LocalStorage
* Mensagens de erro e sucesso
* Links de navegação e interações do usuário

Os testes garantem confiabilidade e evitam regressões durante atualizações da aplicação.



 **Testes da Página Home**

Esses testes asseguram que todos os elementos importantes da página inicial aparecem corretamente.

Eles validam:

* Logo e cabeçalho
* Menu de navegação
* Seção do mapa
* Descrições e botões
* Botões FAQ
* Footer da página
* Links principais

Além disso, verificam se:

* Links principais podem ser clicados
* Botões executam suas ações (ex.: abrir FAQ ou seções de informação)

Isso assegura que a primeira impressão da aplicação esteja funcional e bem apresentada.

---

 **Testes da Página de Cadastro**

Nesta seção, os testes garantem que:

✔ **Todos os elementos estão presentes**
Inputs, botão de cadastro e link para login.

✔ **Campos obrigatórios funcionam**
Verificam se `required` está aplicado corretamente.

✔ **Redirecionamentos do fluxo de cadastro**
Botão "Cadastrar" deve iniciar o processo corretamente.

✔ **Link de login funciona**
Testa navegação para a página de login.

✔ **Estrutura do formulário**
Confirma todos os campos essenciais presentes.

---

## **Testes da Página de Denúncia**

Os testes desta página asseguram:

* Cabeçalho, navegação e footer
* Inputs de Nome, Local e Relato
* Upload de arquivos
* Botão de envio do formulário
* Mensagens obrigatórias
* Links do menu de navegação

O objetivo é validar que o usuário consiga:

✔ Fazer denúncias corretamente
✔ Inserir informações obrigatórias
✔ Navegar para outras áreas

---

**Testes da Página de Login**

Possui as validações mais importantes, incluindo:

✔ **Interface:** inputs, botões e links visíveis
✔ **Validações de erro:** campos vazios e credenciais incorretas
✔ **Login correto:** simula usuário no LocalStorage
✔ **Link “Esqueceu a senha?”** com mensagem adequada

---

## **Fluxo Completo Validado (Cadastro → Login → Sistema)**

A suíte garante que:

* Usuário se cadastra
* Dados são salvos no LocalStorage
* Usuário acessa login
* Faz login com sucesso
* Recebe mensagens adequadas

Esse fluxo simula o uso real do sistema FireLeaf.

---

 **Como os Testes Cypress Funcionam no Código**

Arquitetura padrão:

* `beforeEach()` limpa LocalStorage
* `cy.visit()` abre a página
* `cy.get()`, `cy.type()`, `cy.click()` simulam ações
* `cy.should()` faz assertivas
* `cy.wait()` aguarda animações e mensagens

Isso reproduz exatamente o comportamento do usuário.

---

# **Conclusão Final**

Os testes E2E escritos utilizando Cypress garantem:

✔ Confiabilidade em todas as telas
✔ Interações completas de usuários reais
✔ Validações de erro e sucesso
✔ Fluxos essenciais estáveis
✔ Interface consistente e navegável
✔ Redirecionamentos e links funcionando em todas as páginas

A aplicação está totalmente mapeada e protegida contra comportamentos inesperados.






