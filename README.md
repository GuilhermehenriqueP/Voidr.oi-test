# Voidr.io-test

# Projeto de Testes Automatizados com Playwright

Este repositório contém uma suíte de testes automatizados usando Playwright. O objetivo é entregar o desafio teste para a empresa Voidr.io.Usei o Padrão Page Object Model para o desenvolvimento. 

## Cenários de Testes

1. **Verificar login bem-sucedido**  
   **Cenário:** O usuário deve conseguir fazer login com credenciais válidas.  
   **Ação:** O usuário insere um e-mail e uma senha válidos e clica no botão de login.  
   **Resultado Esperado:** O sistema autentica o usuário e redireciona para a página principal.

2. **Verificar erro no login com credenciais inválidas**  
   **Cenário:** O sistema deve exibir uma mensagem de erro ao tentar fazer login com credenciais inválidas.  
   **Ação:** O usuário insere um e-mail ou senha inválidos e clica no botão de login.  
   **Resultado Esperado:** O sistema exibe uma mensagem de erro informando que as credenciais estão incorretas.

3. **Verificar o nome dos produtos na lista**  
   **Cenário:** O sistema deve exibir corretamente os nomes dos produtos na lista de produtos.  
   **Ação:** O usuário acessa a página de produtos.  
   **Resultado Esperado:** Todos os produtos são exibidos com os nomes corretos, sem erros de ortografia.  
   **Nota:** Este cenário está falhando propositalmente devido a um bug no site.

4. **Testar o filtro de preço**  
   **Cenário:** O sistema deve filtrar corretamente os produtos por faixa de preço.  
   **Ação:** O usuário define uma faixa de preço no filtro e aplica.  
   **Resultado Esperado:** Somente produtos dentro da faixa de preço selecionada são exibidos.

5. **Testar o filtro de nome**  
   **Cenário:** O sistema deve filtrar corretamente os produtos pelo nome.  
   **Ação:** O usuário insere parte do nome de um produto no filtro de nome e aplica.  
   **Resultado Esperado:** Somente produtos que correspondem ao critério de nome são exibidos.

6. **Verificar itens no carrinho de compras**  
   **Cenário:** O sistema deve mostrar corretamente os itens adicionados ao carrinho.  
   **Ação:** O usuário adiciona produtos ao carrinho e acessa a página do carrinho de compras.  
   **Resultado Esperado:** Todos os itens adicionados ao carrinho são exibidos corretamente.

7. **Verificar o botão de remover itens do carrinho**  
   **Cenário:** O sistema deve permitir que o usuário remova itens do carrinho.  
   **Ação:** O usuário clica no botão de remover item ao lado de um produto no carrinho.  
   **Resultado Esperado:** O item é removido do carrinho e a lista de itens é atualizada.

8. **Tentar avançar no checkout com o carrinho vazio**  
   **Cenário:** O sistema deve impedir que o usuário avance no checkout com o carrinho vazio.  
   **Ação:** O usuário tenta prosseguir para o checkout sem nenhum item no carrinho.  
   **Resultado Esperado:** O sistema exibe uma mensagem de erro e não permite avançar no checkout.  
   **Nota:** Este cenário está falhando propositalmente devido a um bug no site.

9. **Tentar avançar no checkout sem preencher os campos obrigatórios**  
   **Cenário:** O sistema deve exigir que todos os campos obrigatórios sejam preenchidos antes de avançar no checkout.  
   **Ação:** O usuário tenta prosseguir para o checkout sem preencher todos os campos obrigatórios.  
   **Resultado Esperado:** O sistema exibe uma mensagem de erro indicando os campos obrigatórios que faltam e não permite avançar.

10. **Preencher os campos obrigatórios e avançar no checkout**  
    **Cenário:** O usuário deve conseguir avançar no checkout após preencher todos os campos obrigatórios.  
    **Ação:** O usuário preenche todos os campos obrigatórios no checkout e clica em avançar.  
    **Resultado Esperado:** O sistema permite que o usuário avance para a próxima etapa do checkout.

## Como Rodar o Projeto

### Pré-requisitos

- Node.js e npm instalados na sua máquina.
- Clonar este repositório.

### Passos para Instalar e Rodar

1. **Instale as dependências:**
   ```bash
   npm install
   ```

2. **Execute os testes:**
   ```bash
   npx playwright test
   ```

3. **Gere um relatório dos testes:**
   ```bash
   npx playwright show-report
   ```

### Observações

- Certifique-se de que a aplicação esteja rodando antes de executar os testes.
- Para ajustar os testes ou adicionar novos, edite os arquivos na pasta `tests`.
- Os cenários 3 e 8 estão falhando propositalmente pois o site tem esses bugs, achei importante colocá-los para demonstrar a eficiência dos testes.

---

