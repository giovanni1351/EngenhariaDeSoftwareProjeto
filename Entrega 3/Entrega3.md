
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
|Função|Permitir que o cliente consiga fazer o gerenciamento (Inserir, atualizar ou remover ) do carrinho dos produtos.|
|Atores|Cliente e Sistema.|
|Pré Condição|1. Estar logado. <br> 2. Produto cadastrado na plataforma.|
|Pós Condição|Carrinho atualizado para o cliente|
|Fluxo Principal|1. Cliente Loga <br >2. Cliente acessa a pagina do produto <br> 3. Cliente clicka no botão de adicionar no carrinho <br> 4. Sistema adiciona no carrinho o produto|
|Fluxo Alternativo|1. Cliente Acessa a tela do carrinho <br> 2. Cliente e realiza remoção ou atualização do produto <br> 3. Sistema realiza a tarefa de exclusão ou atualização|


## Caso de uso 2 | UC-02 :   Comprar produto
|Identificador|UC02|
|-------------|-----|
|Função|Permitir que o comprador adquira produtos ou serviços na plataforma.|
|Atores|Comprador, Sistema, Vendedor e Gateway de Pagamento.|
|Pré Condição|1. Comprador deve estar logado. <br> 2. O produto deve estar cadastrado na plataforma |
|Pós Condição|1. Produto adicionado ao histórico de compras do comprador<br>2. Produto adicionado ao historico de venda do vendedor <br> 3. Produto entregue.|
|Fluxo Principal|1. Comprador Loga.<br> 2. Comprador acessa a pagina do produto. <br> 3. Comprador clica no botão de "Comprar Agora" <br> 4. Sistema inicia o processo de pagamento <br> 5. Comprador insere as informações de pagamento <br> 6. Sistema verifica a integridade dos dados <br> 7. Gateway de pagamento realiza a transação <br>7.5 Sistema guarda o valor até a finalização da entrega<br>8. Comprador realiza a primeira etapa de pagamento <br> 9. Comprador Inicia chat com o vendedor <br> 10. Comprador paga a segunda etapa apos entrega do produto <br> 11. Gateway de pagamento realiza a transação|
|Fluxo Alternativo|A1. Comprador acessa o carrinho <br> A2. Comprador clica em "Prossegir para o Pagamento"<br> A3.Segue fluxo pincipal a partir do item 4 <hr>B1. Comprador inicial chat com o vendedor <br>B2. Inicial o fluxo principal a partir do item 3|
|Fluxo de Excessão| E1. Comprador Cancela a compra <br>- E1.1. Inicia processo de cancelamento<hr>E2. Vendedor cancela a venda <br>-  E2.1. Iniciar processo de cancelamento<hr> E3. Vendedor não entrega produto a tempo <br>- E3.1 Inicia processo de cancelamento|


## Caso de uso 3 | UC-03 :  Avaliar Produto
|Identificador|UC-03|
|-------------|-----|
|Função|Avaliar produto comprado.|
|Atores|Comprador e Sistema.|
|Pré Condição|1. Comprador logado. <br>2. Compra realizada do determinado produto.|
|Pós Condição|Produto é rankeado a partir das avaliações.|
|Fluxo Principal|1. Sistema envia um e-mail <br>2. Comprador acessa o link recebido <br> 3. Comprador preenche os campos do formulario <br> 4. Comprador Clickar em "Enviar Avaliação" <br> 5. Sistema computa a avaliação |



## Caso de uso 4 | UC-04 :  Abrir Chat


|Identificador|UC-04|
|-------------|-----|
|Função|Conversa entre ambas as partes da negociação.|
|Atores|Cliente, Vendedor e Sistema.|
|Pré Condição| 1. Comprador Logado|
|Fluxo Principal|1. Comprador acessa a pagina do produto<br> 2. Comprador clica no botão "Iniciar Chat com o Vendedor" <br> 3. Sistema cria uma instancia de chat com ambas as partes <br> 4. Vendedor e Cliente se comunicam|



## Caso de uso 5 | UC-05 :  Gerenciar perfil

|Identificador|UC-05|
|-------------|-----|
|Função|Atualizar informações do perfil|
|Atores|Cliente, Vendedor e sistema|
|Pré Condição|Estar logado|
|Pós Condição|Informações atualizadas|
|Fluxo Principal|1. Usuario acessa a pagina de configuração de conta <br> 2. Usuario realiza as mudanças <br>3. Usuario submete as modificações <br> 4. Sistema realiza a operação desejada|


## Caso de uso 6 | UC-06 : Cancelar Transação


|Identificador|UC-06|
|-------------|-----|
|Função|Cancelar a operação de venda ou compra|
|Atores|Cliente, Vendedor e sistema|
|Pré Condição|1. Usuario logado <br> 2. Primeira etapa da compra de um produto ja realizada|
|Pós Condição|Venda cancelada, historicos de compra do cliente atualizado e historico de vendas do vendedor atualizado |
|Fluxo Principal|1. Comprador Acessa o historico de compras <br> 2. Comprador clica em "Cancelar" no produto em andamento <br>3. Sistema mostra uma mensagem de confirmação<br>4. sistema inicia  pagamento ao vendedor do valor da primeira etapa de compra<br> 5. Sistema notifica vendedor sobre o cancelamento|
|Fluxo Alternativo|A1. Vendedor acessa a pagina de vendas<br> A2. Vendedor clica no botão de "Cancelar" no produto em andamento ou em produção <br>3. Sistema mostra uma mensagem de confirmação <br>4. Sistema reembolsa o valor da primeira etapa de compra ao comprador <hr>Se o entregador não entregue antes<br> B1. Sistema verifica data de entrega <br> B2. Enviar Aviso ao vendedor <br>B3. Valor é reembolsado para o comprador |



## Caso de uso 7 | UC-07 : Entregar Produto

|Identificador|UC-07|
|-------------|-----|
|Função|Entragar o produto desenvolvido pelo vendedor.|
|Atores|Vendedo, Comprador e sistema.|
|Pré Condição|Compra do produto realizada.|
|Pós Condição|1. Venda concluida<br> 2. status na tela de historico de vendas do vendedor como concluido<br>3. Segunda etapa do processo de venda realizada|
|Fluxo Principal|1. Vendedor acessa a pagina de vendas <br> 2. Vendedor clica no botão "Marcar Entregue"<br> 3. Sistema mostra uma modal com os campos para realizar a entregua <br>4. Vendedor faz o upload da entrega <br> 5. Sistema computa entrega<br> 6. Sistema continua fluxo no processo de compra|



## Caso de uso 8 | UC-08 : Virar Vendedor


|Identificador|UC-08|
|-------------|-----|
|Função|Mudar o tipo de conta de comprador para vendedor.|
|Atores|Comprador e sistema.|
|Pré Condição|1. Usuário logado <br> 2. Usuário ser do tipo comprador|
|Pós Condição|Conta de comprador vira vendedor|
|Fluxo Principal|1. Comprador acessa a tela de perfil <br>2. Comprador clica no botão "Tornar-se Vendedor" <br> 3. Sistema mostra uma modal com um formulario para preencher as informações de vendedor <br> 4. Comprador preenche informações solicitadas <br> 5. Comprador submete a Solicitação <br> 6. Sistema realiza a mudança do tipo de conta|



## Caso de uso 9 | UC-09 : Gerenciar Produto

|Identificador|UC-09|
|-------------|-----|
|Função|Gerenciar os produtos (Criar, Deletar ou Atualizar)|
|Atores|Vendedor e sistema|
|Pré Condição|Comprador logado|
|Pós Condição|Atualização feita nos produtos do vendedor|
|Fluxo Principal|1. Vendedor acessa a tela de cadastro de produto<br> 2. Sistema disponibiliza um formulario para cadastrar as informações <br> 3. Vendedor preenche o formulario <br> 4. Vendedor submete a criação do produto <br> 5. Sistema realiza a operação de criar produto <br> |
|Fluxo Alternativo|A1. Vendedor acessa a tela de produtos cadastrados <br> A2. Vendedor seleciona produto para realizar alteração <br> A3. Sistema disponibiliza formulario para mudança <br> A4. Vendedor preenche as informações a serem atualizadas <br> A5. Vendedor submete atualização <br> A6. Sistema realiza a operação de atualizar produto <hr> B1. Vendedor acessa a tela de produtos <br> B2. Vendedor clicka em Excluir <br> B3. Sistema mostra uma tela de confirmação <br> B4. Vendedor confirma <br> Sistema realiza a remoção do produto|
