
# Diagrama de Contexto:


## Avaliação:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Avaliacao.png)

## Cadastro de Produtos:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/CadastroDeProduto.png)

## Cadastro:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Cadastro.png)

## Cancelamento:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Cancelamento.png)

## Faturamento:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Faturamento.png)

## Login:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Login.png)

## Mudança de Conta:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/MudancaDeConta.png)

## Venda:
![Imagem de exemplo](Imagens/Diagrama_de_Contexto/Venda.png)

# Casos de Uso

![Imagem de exemplo](Imagens/CasosDeUso(1).png)

## Caso de uso 1 | UC-01 :   Gerenciar Carrinho

|Identificador|UC-01|
|-------------|-----|
|Função|Permitir que o cliente consiga fazer o gerenciamento (Inserir, Editar ou remover ) do carrinho dos produtos.|
|Atores|Cliente|
|Pré Condição|1. Estar logado. <br> 2. Produto cadastrado na plataforma.|
|Pós Condição|Carrinho atualizado para o cliente|
|Fluxo Principal|1. Cliente acessa a pagina do produto <br>2. Cliente clica no botão de adicionar no carrinho <br>3. Sistema adiciona o produto no carrinho|
|Fluxo Alternativo 1|1. Cliente Acessa a tela do carrinho <br> 2. Cliente realiza a atualização do produto <br> 3. Sistema realiza a atualização|
|Fluxo Alternativo 2|1. Cliente Acessa a tela do carrinho <br> 2. Cliente realiza a remoção do produto <br> 3. Sistema realiza a remoção|

## Caso de uso 2 | UC-02 :   Comprar produto
|Identificador|UC02|
|-------------|-----|
|Função|Permitir que o comprador adquira produtos ou serviços na plataforma.|
|Atores|Comprador, Vendedor e Gateway de Pagamento.|
|Pré Condição|1. Comprador deve estar logado. <br> 2. O produto deve estar cadastrado na plataforma |
|Pós Condição|1. Produto adicionado ao histórico de compras do comprador<br>2. Produto adicionado ao historico de venda do vendedor <br> 3. Produto entregue.|
|Fluxo Principal|1. Comprador acessa a pagina do produto. <br> 2. Comprador clica no botão de "Comprar Agora" <br>3. Sistema adiciona o produto no carrinho <br>4. Sistema inicia o processo de pagamento <br> 5. Comprador insere as informações de pagamento <br> 6. Sistema verifica a integridade dos dados <br> 7. Gateway de pagamento realiza a transação <br>8 Sistema guarda o valor até a finalização da entrega<br>9. Comprador realiza a primeira etapa de pagamento <br> 10. Comprador Inicia chat com o vendedor <br> 11. Comprador paga a segunda etapa apos entrega do produto <br> 12. Gateway de pagamento realiza a transação<br> 13. Sistema remove o produto do carrinho|
|Fluxo Alternativo 1|1. Comprador acessa o carrinho <br> 2. Comprador clica em "Prossegir para o Pagamento"<br> 3. Segue fluxo pincipal a partir do item 4|
|Fluxo Alternativo 2|1. Comprador inicial chat com o vendedor <br>2. Inicial o fluxo principal a partir do item 3|
|Fluxo Alternativo 3|1. Comprador acessa a tela do carrinho <br>2. Comprador seleciona os produtos que deseja comprar <br> 3. Comprador confirma a compra dos produtos<br> 4. Inicia o fluxo principal a partir do item 5|
|Fluxo de Exceção 1| 1. Comprador Cancela a compra <br> 2. Inicia processo de cancelamento|
|Fluxo de Exceção 2| 1. Vendedor cancela a venda <br>  2. Iniciar processo de cancelamento|
|Fluxo de Exceção 3| 1. Vendedor não entrega produto a tempo <br> 2. Inicia processo de cancelamento|


## Caso de uso 3 | UC-03 :  Avaliar Produto
|Identificador|UC-03|
|-------------|-----|
|Função|Avaliar produto comprado.|
|Atores|Comprador|
|Pré Condição|1. Comprador logado. <br>2. Compra realizada do determinado produto.|
|Pós Condição|Produto é rankeado a partir das avaliações.|
|Fluxo Principal|1. Sistema envia um e-mail <br>2. Comprador acessa o link recebido <br> 3. Comprador preenche os campos do formulario <br> 4. Comprador clica em "Enviar Avaliação" <br> 5. Sistema computa a avaliação |
|Fluxo Alternativo|1. Sistema envia um e-mail <br>2. Comprador não acessa o link recebido <br>3. Sistema envia outro email após 30 dias sem resposta <br>4. Comprador acessa o link recebido<br> 4. Comprador preenche os campos do formulario <br> 5. Comprador clica em "Enviar Avaliação" <br> 6. Sistema computa a avaliação |



## Caso de uso 4 | UC-04 :  Abrir Chat


|Identificador|UC-04|
|-------------|-----|
|Função|Conversa entre ambas as partes da negociação.|
|Atores|Cliente, Vendedor|
|Pré Condição| 1. Comprador Logado. <br>2. Produto cadastrado na plataforma|
|Fluxo Principal|1. Comprador acessa a pagina do produto<br> 2. Comprador clica no botão "Iniciar Chat com o Vendedor" <br> 3. Sistema cria uma instancia de chat com ambas as partes <br> 4. Vendedor e Cliente se comunicam|



## Caso de uso 5 | UC-05 :  Gerenciar perfil

|Identificador|UC-05|
|-------------|-----|
|Função|Atualizar informações do perfil|
|Atores|Cliente, Vendedor|
|Pré Condição|Estar logado|
|Pós Condição|Informações atualizadas|
|Fluxo Principal|1. Usuario acessa a pagina de configuração de conta <br> 2. Usuario realiza as mudanças <br>3. Usuario submete as modificações <br> 4. Sistema realiza a operação desejada|


## Caso de uso 6 | UC-06 : Cancelar Transação


|Identificador|UC-06|
|-------------|-----|
|Função|Cancelar a operação de venda ou compra|
|Atores|Cliente, Vendedor|
|Pré Condição|1. Usuario logado <br> 2. Primeira etapa da compra de um produto ja realizada|
|Pós Condição|Venda cancelada, historicos de compra do cliente atualizado e historico de vendas do vendedor atualizado |
|Fluxo Principal|1. Comprador Acessa o historico de compras <br> 2. Comprador clica em "Cancelar" no produto em andamento <br>3. Sistema mostra uma mensagem de confirmação<br>4. sistema inicia  pagamento ao vendedor do valor da primeira etapa de compra<br> 5. Sistema notifica vendedor sobre o cancelamento|
|Fluxo Alternativo 1|1. Vendedor acessa a pagina de vendas<br> 2. Vendedor clica no botão de "Cancelar" no produto em andamento ou em produção <br>3. Sistema mostra uma mensagem de confirmação <br>4. Sistema reembolsa o valor da primeira etapa de compra ao comprador|
|Fluxo Alternativo 2|1. Sistema verifica data de entrega <br> 2. Enviar Aviso ao vendedor <br>3. Valor é reembolsado para o comprador |



## Caso de uso 7 | UC-07 : Entregar Produto

|Identificador|UC-07|
|-------------|-----|
|Função|Entragar o produto desenvolvido pelo vendedor.|
|Atores|Vendedor, Comprador|
|Pré Condição|Compra do produto realizada.|
|Pós Condição|1. Venda concluida<br> 2. Produto entregue para o cliente <br>3. Status na tela de historico de vendas do vendedor como concluido<br>4. Segunda etapa do processo de venda realizada|
|Fluxo Principal|1. Vendedor acessa a pagina de vendas <br> 2. Vendedor clica no botão "Marcar Entregue"<br> 3. Sistema mostra uma modal com os campos para realizar a entregua <br>4. Vendedor faz o upload da entrega <br> 5. Sistema computa entrega <br> 6. Sistema inicia processo de avaliar produto|



## Caso de uso 8 | UC-08 : Virar Vendedor


|Identificador|UC-08|
|-------------|-----|
|Função|Mudar o tipo de conta de comprador para vendedor.|
|Atores|Comprador|
|Pré Condição|1. Usuário logado <br> 2. Usuário ser do tipo comprador|
|Pós Condição|Conta de comprador vira vendedor|
|Fluxo Principal|1. Comprador acessa a tela de perfil <br>2. Comprador clica no botão "Tornar-se Vendedor" <br> 3. Sistema mostra uma modal com um formulario para preencher as informações de vendedor <br> 4. Comprador preenche informações solicitadas <br> 5. Comprador submete a Solicitação <br> 6. Sistema realiza a mudança do tipo de conta|



## Caso de uso 9 | UC-09 : Gerenciar Produto

|Identificador|UC-09|
|-------------|-----|
|Função|Gerenciar os produtos (Criar, Deletar ou Atualizar)|
|Atores|Vendedor|
|Pré Condição|Vendedor logado|
|Pós Condição|Atualização feita nos produtos do vendedor|
|Fluxo Principal|1. Vendedor acessa a tela de cadastro de produto<br> 2. Sistema disponibiliza um formulario para cadastrar as informações <br> 3. Vendedor preenche o formulario <br> 4. Vendedor submete a criação do produto <br> 5. Sistema realiza a operação de criar produto <br> |
|Fluxo Alternativo 1|1. Vendedor acessa a tela de produtos cadastrados <br> 2. Vendedor seleciona produto para realizar alteração <br> 3. Sistema disponibiliza formulario para mudança <br> 4. Vendedor preenche as informações a serem atualizadas <br> 5. Vendedor submete atualização <br> 6. Sistema realiza a operação de atualizar produto |
|Fluxo Alternativo 2|1. Vendedor acessa a tela de produtos <br> 2. Vendedor clicka em Excluir <br> 3. Sistema mostra uma tela de confirmação <br> 4. Vendedor confirma <br> 5. Sistema realiza a remoção do produto|


## Caso de uso 10 | UC-10 : Visualizar histórico de compras 

|Identificador|UC-10|
|-------------|-----|
|Função|Permitir que o comprador visualize seu histórico de compras realizadas na plataforma.|
|Atores|Comprador|
|Pré Condição|Comprador deve estar logado.|
|Pós Condição|Histórico de compras exibido para o comprador.|
|Fluxo Principal|1. Comprador acessa a área de histórico de compras, clicando em "Minhas compras". <br> 2.  lista de compras realizadas, ordenadas por data mais recente. 


## Caso de uso 11 | UC-11 : Visualizar histórico de vendas 

|Identificador|UC-11|
|-------------|-----|
|Função|Permitir que o vendedor visualize seu histórico de vendas realizadas na plataforma.|
|Atores|Vendedor|
|Pré Condição| Vendedor deve estar logado.|
|Pós Condição| Histórico de vendas exibido para o vendedor.|
|Fluxo Principal|1. Vendedor acessa a área de histórico de vendas. <br> 2. Sistema exibe lista de vendas realizadas|

