```mermaid
classDiagram
    class Comprador {
        -id: int
        -nomeCompleto: string
        -cpf: string
        -dataNascimento: date
        -telefone: string
        -email: string
        -senha: string
        -ativo: bool
        -Endereço: string
    }
    class Vendedor {
        -id: int
        -nomeCompleto: string
        -cpf: string
        -dataNascimento: date
        -telefone: string
        -email: string
        -senha: string
        -ativo: bool
        -Endereço: string
        -infoTecnica: string
        -contaBancaria: string
        -portifolio: string
        -portifolioLink: string
    }
    class Produto {
        -id: int
        -nome: string
        -descricaoCurta: string
        -descricaoDetalhada: string
        -preco: float
        -comissao: float
        -desconto: float
        -precoFinal: float
        -prazoEntregaValor: int
        -prazoEntregaUnidade: string
        -inclui: string
        -naoInclui: string
        -requisitosComprador: string
        -categoria: string
        -urlImagem: string
    }

    class Carrinho {
        -id: int
    }
    class Pedido {
        -id: int
        -status: string
        -dataCriacao: date
    }
    class Pagamento {
        -id: int
        -valor: float
        -status: string
        -dataPagamento: date
        -formaPagamento: string
    }
    class Avaliacao {
        -id: int
        -nota: int
        -comentario: string
        -data: date
    }

    Vendedor "1" --o "*" Produto : cadastra
    Comprador "1" --o "1" Carrinho : possui
    Comprador "1" --o "*" Pedido : realiza
    Carrinho "1" --o "*" Pedido : possui
    Pedido "1" --o "1" Pagamento : possui
    Pedido "*" --o "1" Comprador : pertence
    Pedido "*" --o "1" Vendedor : realiza
    Pedido "1" --o "1..*" Produto : possui
    Produto "1" --o "*" Avaliacao : recebe
    Avaliacao "*" --o "1" Comprador : realiza
    
```

# Descrição das Classes

## Comprador
Representa o usuário que realiza compras na plataforma. Todo usuário inicialmente é registrado como comprador, podendo posteriormente se tornar vendedor. O comprador possui um carrinho de compras, pode realizar pedidos e fazer avaliações dos produtos adquiridos.

## Vendedor
Representa o usuário que cadastra e vende produtos na plataforma. O vendedor possui informações técnicas específicas, conta bancária para recebimentos e portfólio para demonstrar suas habilidades. Pode cadastrar múltiplos produtos e receber avaliações sobre seus produtos.

## Produto
Representa os itens ou serviços disponíveis para venda na plataforma. Cada produto possui informações detalhadas como preço, comissão para a plataforma, prazo de entrega, requisitos e descrições. Produtos com maior comissão recebem maior destaque na plataforma.

## Carrinho
Representa o carrinho de compras do comprador, onde são armazenados temporariamente os produtos que o comprador deseja adquirir. Cada comprador possui um único carrinho, que pode conter múltiplos produtos.

## Pedido
Representa uma transação de compra realizada pelo comprador. O pedido possui um status que indica seu estágio (em andamento, finalizado, cancelado) e está associado a um ou dois pagamentos (primeira e segunda parcela). Cada pedido pertence a um comprador e um vendedor.

## Pagamento
Representa as transações financeiras realizadas na plataforma. Cada pedido pode ter um ou dois pagamentos (primeira e segunda parcela). O pagamento possui informações sobre valor, status, data e forma de pagamento.

## Avaliação
Representa as avaliações feitas pelos compradores sobre os produtos adquiridos. As avaliações incluem nota e comentário, e são utilizadas para ranquear produtos e vendedores na plataforma. Um comprador não pode avaliar seus próprios produtos.
