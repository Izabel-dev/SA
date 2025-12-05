Documentação dos Testes E2E — FireLeaf (Cypress)
Tecnologias Utilizadas:

Os testes automatizados da aplicação FireLeaf foram desenvolvidos utilizando:

✔ Cypress.io

Framework moderno de testes E2E

Permite simular ações reais do usuário

Executa em ambiente controlado dentro do navegador

Oferece asserts, mocks, inspeção visual e time-travel

Ideal para validar interfaces web e fluxos completos

✔ JavaScript

Utilizado para escrever os testes Cypress

✔ HTML, CSS e JavaScript da Aplicação

Cada página testada depende dos elementos construídos na interface

Validações JS e LocalStorage também são testadas

✔ LocalStorage

Usado como simulação de banco de dados de usuários

Cypress testa leitura, escrita e comportamento desses dados

 Descrição Geral da Suíte de Testes

Toda a suíte foi construída para validar todas as principais páginas e funcionalidades da plataforma FireLeaf, cobrindo:

Estrutura visual das páginas

Funcionalidade dos formulários

Comportamento de validações obrigatórias

Redirecionamentos simulando o fluxo real

Armazenamento no LocalStorage

Mensagens de erro e sucesso

Links de navegação e interações do usuário

Os testes garantem confiabilidade e evitam regressões durante atualizações da aplicação.

 1. Testes da Página Home

Esses testes asseguram que todos os elementos importantes da página inicial aparecem corretamente.

Eles validam:

Logo e cabeçalho

Menu de navegação

Seção do mapa

Descrições e botões

Botões FAQ

Footer da página

Links principais

Além disso, verificam se:

Links principais podem ser clicados

Botões executam suas ações (ex.: abrir FAQ ou seções de informação)

Isso assegura que a primeira impressão da aplicação esteja funcional e bem apresentada.

 2. Testes da Página de Cadastro

Nesta seção, os testes garantem que:

✔ Todos os elementos estão presentes

Como inputs, botão de cadastro e link para login.

✔ Campos obrigatórios funcionam

Eles verificam se:

should('have.attr', 'required')


está aplicado corretamente, impedindo envios incompletos.

✔ Redirecionamentos do fluxo de cadastro

Botão "Cadastrar" deve iniciar o processo corretamente.

✔ Link de login funciona

Testa navegação para a página de login.

✔ Estrutura do formulário

Verifica se todos os campos essenciais estão presentes e acessíveis.

Esses testes validam usabilidade e integridade funcional da etapa de criação de conta.

 3. Testes da Página de Denúncia

Os testes desta página asseguram:

Visibilidade de todos elementos da interface

Cabeçalho, navegação, footer

Inputs de Nome, Local e Relato

Upload de arquivos

Botão de envio do formulário

Mensagens obrigatórias

Links do menu de navegação

O objetivo é validar que o usuário consiga:

✔ Fazer denúncias corretamente
✔ Inserir informações obrigatórias
✔ Navegar para outras áreas

A página de denúncia é crítica, então os testes garantem que nenhum campo importante falte ou esteja quebrado.

 4. Testes da Página de Login

Possui as validações mais importantes, incluindo:

✔ Interface

Inputs, botões e links visíveis

✔ Validações de erro:

Campos vazios → mensagem vermelha

Credenciais incorretas → mensagem apropriada

✔ Login correto

Simula um usuário no LocalStorage e testa:

Preenchimento dos campos

Clique no botão Login

Exibição da mensagem "Login realizado com sucesso"

✔ Link "Esqueceu a senha?"

Garante que a mensagem adequada seja exibida ao clicar.

Esses testes certificam que o sistema possui segurança mínima e resposta adequada a erros.

 Fluxo Completo Validado (Cadastro → Login → Sistema)

A suíte garante que:

Usuário se cadastra

Dados são salvos no LocalStorage

Usuário acessa login

Faz login com sucesso

Recebe mensagens adequadas

Esse fluxo simula o uso real do sistema FireLeaf, garantindo que:

✔ Cadastro funciona
✔ Login identifica credenciais
✔ Redirecionamentos são ativados corretamente

Como os Testes Cypress Funcionam no Código

Todos os trechos seguem a mesma arquitetura:

beforeEach()

Limpa LocalStorage

Garante página limpa a cada teste

Abre a página específica com cy.visit()

Ações simuladas

cy.get() → seleciona elementos

cy.type() → digita nos campos

cy.click() → clica em botões

cy.should() → faz assertivas

cy.wait() → aguarda para animações ou mensagens

Isso faz com que o Cypress emule exatamente o comportamento do usuário no navegador, garantindo realismo total.

 Conclusão Final

Os testes E2E escritos utilizando Cypress garantem:

✔ Confiabilidade em todas as telas do FireLeaf
✔ Interações completas simulando usuários reais
✔ Validações de erro e sucesso funcionando
✔ Fluxos essenciais (Cadastro / Login / Denúncia) estáveis
✔ Interface consistente, acessível e funcional
✔ Redirecionamentos e links testados em todas as páginas

A aplicação está totalmente mapeada e protegida contra comportamentos inesperado

