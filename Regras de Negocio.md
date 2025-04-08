
## Regras de Negócio

### Gerais
- RN01: Todo usuário inicialmente é registrado como comprador.
- RN02: Todo usuario tem que se registrar com as seguintes informações:
Aqui está a lista de todos os campos do formulário de cadastro:
    - Nome Completo
    - CPF
    - Data de Nascimento
    - Telefone
    - E-mail
    - Senha
    - CEP
    - Estado
    - Cidade
    - Rua
    - Número
    - Complemento (opcional)
    - Bairro

- RN03: Para se tornar vendedor, o usuário deve fornecer informações técnicas, bancárias e portfólio.
- RN04: Um mesmo usuário não pode comprar e avaliar seus próprios produtos.


### Anúncios e Comissões
- RN05: O vendedor define a porcentagem de comissão para a plataforma valor minimo de 5%.
- RN06: Produtos com maior porcentagem de comissão recebem maior destaque na plataforma (produtos em destaque).
- RN07: Produtos com boa média de vendas e alta confiabilidade ganham espaço no painel de produtos confiaveis.

### Pagamentos e Faturamento

- RN08: Todo pagamento é dividido em duas etapas (metade inicial, metade final).
- RNX:O valor da primeira etapa será retida até a confirmação da segunda etapa.
- RN10: A segunda metade só é solicitada após o vendedor finalizar o desenvolvimento/preparação.
- RNx: O valor da comissão será descontada do valor final pago, após a confirmação da segunda etapa
- RN11: O valor é liberado para o vendedor somente após confirmação de entrega pelo comprador.


### Cancelamentos
- RN13: Se o vendedor solicitar cancelamento, o valor pago é estornado integralmente ao comprador.
- RN14: Se o comprador solicitar cancelamento, o valor da primeira parcela é destinado ao vendedor como compensação com a taxa do produto.
- RN15: Após a entrega do produto, não é possível realizar cancelamento.

### Avaliações
- RN16: O formulário de avaliação é enviado ao comprador 30 dias após a entrega, caso o produto ainda não tenha sido avaliado.
- RN17: Apenas compradores que finalizaram a compra podem avaliar produtos e vendedores.
- RN18: Avaliações são consideradas no algoritmo de destaque de produtos e vendedores.

### Cadastro de Produtos
- RN19: Todos os produtos devem pertencer a pelo menos uma categoria.
- RNX: O cadastro de produto deve conter os seguintes campos:
    - Nome do Produto/Serviço
    - Categoria
    - Subcategoria
    - Descrição Curta
    - Descrição Detalhada
    - Tags
    - Imagem Principal
    - Preço
    - Comissão da Plataforma
    - Desconto
    - Preço Final
    - Prazo de Entrega (Valor)
    - Prazo de Entrega (Unidade)
    - O que está incluído
    - O que não está incluído
    - Requisitos para o Comprador
- RN20: Imagens de produtos devem seguir padrões definidos (dimensões, tamanho).
- RN21: Descrições de produtos devem ter um mínimo de caracteres para garantir informações adequadas.
- RNX: O vendedor dispõe de um prazo adicional de 7 (sete) dias corridos, após o término do prazo de entrega estipulado no cadastro do produto, para efetuar a entrega.
- RNX: Caso o produto não seja entregue dentro do prazo estabelecido (incluindo o prazo adicional de 7 dias corridos), o valor pago será integralmente reembolsado ao comprador. Adicionalmente, o vendedor será penalizado com uma redução em sua avaliação geral e a taxa de comissão devida à plataforma será majorada na venda subsequente.
