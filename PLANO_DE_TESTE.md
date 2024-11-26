# Plano de Teste - UI Testing da Plataforma SauceDemo

---

## 1. Objetivo
Garantir que a plataforma SauceDemo funcione conforme o esperado, com foco na experiência do usuário (UX/UI) e na validação dos principais fluxos.

---

## 2. Escopo
- Testar os fluxos críticos: login, ordenação, fluxo de compra, navegação, logout e mais.
- Validar a responsividade em diferentes dispositivos e navegadores.
- Testar a acessibilidade da plataforma.

---

## 3. Casos de Teste

### **3.1 Login**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC01 | Login com usuário erformance_glitch_user (Usuário com falha de desempenho) | 1. Acesse a tela de login<br>2. Insira o usuário com falha de desempenho<br>3. Clique em "Login" | Mensagem de erro exibida ao usuário                             |
| TC02 | Login com credenciais válidas              | 1. Acesse a página de login<br>2. Insira credenciais válidas no campo de usuário e senha<br>3. Clique em "Login" | Redirecionamento para a página inicial com a lista de produtos exibida |
| TC03 | Login com problem_user                     | 1. Acesse a tela de login<br>2. Insira um usuário com problemas no acesso<br>3. Clique em "Login" | Redirecionamento para a página com uma lista de produtos que não condiz com o site |
| TC04 | Login com usuário “error_user”             | 1. Acesse a página de login<br>2. Insira o usuário "error_user"<br>3. Clique em "Login"<br>4. Redirecionamento para a página com uma lista de produtos<br>5. Adicione um produto ao carrinho<br>6. Acesse o carrinho para finalizar a compra | A opção de finalizar a compra não é exibida no sistema |
| TC05 | Login com usuário bloqueado                | 1. Acesse a tela de login<br>2. Insira um usuário bloqueado<br>3. Clique em "Login" | Mensagem de erro exibida ao usuário                             |
| TC06 | Login com usuário visual_user              | 1. Acesse a tela de login<br>2. Insira o usuário "visual_user"<br>3. Clique em "Login" | Redirecionamento para a página inicial com a lista de produtos exibida |

---

### **3.2 Ordenação e Filtragem de Produtos**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC07 | Ordenação por preço crescente              | 1. Acesse a página de produtos<br>2. Selecione "Preço (Baixo para Alto)" na opção de ordenação | Produtos exibidos em ordem crescente de preço                 |

---

### **3.3 Fluxo Completo de Compra**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC08 | Adicionar item ao carrinho                 | 1. Acesse a página de produtos<br>2. Clique no botão "Adicionar ao Carrinho" de um produto | Produto adicionado ao carrinho com sucesso<br>O contador do carrinho é atualizado |
| TC09 | Finalizar compra                           | 1. Acesse o carrinho com produtos<br>2. Siga para o checkout<br>3. Preencha as informações obrigatórias<br>4. Finalize a compra | Mensagem de confirmação de pedido exibida                       |

---

### **3.4 Gerenciamento de Carrinho**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC10 | Remover item do carrinho                   | 1. Acesse o carrinho com um produto<br>2. Clique no botão "Remover" do produto no carrinho | Item removido com sucesso do carrinho<br>O contador do carrinho é atualizado |

---

### **3.5 Navegação entre Produtos e Detalhes**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC11 | Acessar página de detalhes de um produto   | 1. Acesse a página inicial de produtos<br>2. Clique em um produto específico | Redirecionamento para a página de detalhes do produto<br>As informações detalhadas do produto são exibidas |

---

### **3.6 Logout**

| ID   | Caso de Teste                               | Passos                                                                                  | Resultado Esperado                                             |
|------|--------------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| TC12 | Realizar logout                            | 1. Acesse a plataforma logado<br>2. Clique no botão "Logout" no menu | Redirecionamento para a página de login                       |

---
