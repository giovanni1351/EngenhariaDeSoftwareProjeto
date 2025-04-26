Default

|Identificador|UC-XX|
|-------------|-----|
|Função|Desc|
|Atores|Desc|
|Pré Condição|Desc|
|Pós Condição|Desc|
|Fluxo Principal|Desc|
|Fluxo Alternativo|Desc|
|Fluxo de Exceção|Desc|


# Diagrama de caso de uso

|Identificador|UC01|
|-------------|-----|
|Função|Permitir que o cliente consiga fazer o gerenciamento (Inserir, atualizar ou remover ) do carrinho dos produtos.|
|Atores|Cliente, Sistema.|
|Pré Condição|1. Estar logado. <br> 2. Produto cadastrado na plataforma.|
|Pós Condição|Carrinho atualizado para o cliente|
|Fluxo Principal|1. Cliente Loga <br >2. Cliente acessa a pagina do produto <br> 3. Cliente clicka no botão de adicionar no carrinho <br> 4. Sistema adiciona no carrinho o produto|
|Fluxo Alternativo|1. Cliente Acessa a tela do carrinho <br> 2. Cliente e realiza remoção ou atualização do produto <br> 3. Sistema realiza a tarefa de exclusão ou atualização|


## Caso de uso 9 | UC-09 : Gerenciar Produto

|Identificador|UC-XX|
|-------------|-----|
|Função|Gerenciar os produtos (Criar, Deletar ou Atualizar)|
|Atores|Vendedor e sistema|
|Pré Condição|Comprador logado|
|Pós Condição|Atualização feita nos produtos do vendedor|
|Fluxo Principal|1. Vendedor acessa a tela de cadastro de produto<br> 2. Sistema disponibiliza um formulario para cadastrar as informações <br> 3. Vendedor preenche o formulario <br> 4. Vendedor submete a criação do produto <br> 5. Sistema realiza a operação de criar produto <br> |
|Fluxo Alternativo|A1. Vendedor acessa a tela de produtos cadastrados <br> A2. Vendedor seleciona produto para realizar alteração <br> A3. Sistema disponibiliza formulario para mudança <br> A4. Vendedor preenche as informações a serem atualizadas <br> A5. Vendedor submete atualização <br> A6. Sistema realiza a operação de atualizar produto <hr> B1. Vendedor acessa a tela de produtos <br> B2. Vendedor clicka em Excluir <br> B3. Sistema mostra uma tela de confirmação <br> B4. Vendedor confirma <br> Sistema realiza a remoção do produto|

