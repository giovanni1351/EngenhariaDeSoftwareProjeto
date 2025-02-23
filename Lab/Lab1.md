# O trabalho de engenharia de software é para criar uma empresa
Temos que fazer um projeto que tenha um criador de conteudo e usuario, ou um prestador de servico e um consumidor


# 4 Processos muito importantes

- Venda *A fazer*

- Cancelamento *A fazer*

- Faturamento *Feito* 

- NPS (Avaliação) *Dentro do Faturamento*

## A nossa empresa vai ter muito mais processos do que esses. Mas esses 4 são obrigatorios na avaliação!

# Nossa escolha atual

Uma plataforma de anuncio e vendas de produtos e serviçoes de tecnologia (marketplace), o anunciante pode escolher a porcentagem que vai nos dar do valor do produto para ser anunciado na nossa plataforma, para poder impulcionar o prduto de alguma forma, no caso vamos criar areas no nosso site para deixar com destaque esse produto

O anunciante pode anunciar varios produtos, com varias porcentagem de participação do lucro, ou seja, ele pode anunciar um produto que vale 100 reais e deixar 30 para nossa plataforma, isso vai nos dar um parametro de quanto ele pode ser bom para deixarmos ele em evidencia. 

Nosso site vai ter areas de cadastro, login, tela de configuração da conta, para mudar da conta comprador para conta de anunciante

Uma tela principal, onde vai ter os outdoors de anuncios dos produtos, essa tela tem que ter uma sazonalidade para ser sempre justo com os anunciantes

Tela de compra do produto

Tela de pesquisa, para encontrar produtos por categoria, depois de dar o enter no search que vai ter na tela principal

Tela de compras historicas

Tela de admin, para cadastros de categorias de produto

Tela de perfil, para mudar o tipo de conta

Se a conta for de vendedor uma tela para cadastro de produto

Tela de todos os produtos cadastrados do usuario vendedor

Tela de analise de vendas

Tela de analises comerciais do vendedor

Carrosel na tela inicial fixo (position absolute na direita) para os produtos que são confiaveis da nossa marca, uma media de venda boa e uma confiaça no produto (forma de recompensa para bons vendedores)


# Processo de cadastro
```mermaid
graph TD;
    A[Criar conta no marketplace]-->B[Entrar no site];
    B-->C[Entrar no formulario de cadastro];
    C-->D[Inserir informações];
    D-->|Caso informações esteja de acordo para o cadastro|E[Cadastro bem sucedido];
    D-->|Caso informações não esteja de acordo para o cadastro|G[Enviar aviso ao usuario de erro em alguma informação no formulario];
    G-->|Tentar novamente|D;
    E-->F[Logar];

    Logar[Logar]--> EntrarForm[Entrar no Formulario de login];
    EntrarForm --> InserirInfos[Inserir informações de login];
    InserirInfos --> Verifica[ Verificar informações preenchidas];
    Verifica --> |Informações Encontradas e corretas| LogarCorreto[Login bem sucedido]
    LogarCorreto--> Redirect[Redirecionar para o site logado]
    Verifica --> |Informações não encontrada ou incorretas| MensagemDeErroLogin[Aparece botões para poder tentar novamente ou criar conta]
    MensagemDeErroLogin-->InserirInfos;
    MensagemDeErroLogin-->RedirectRegistro[Entrar no processo de registro];
```

# Processo de Faturamento 

O comprador deve enviar metade do valor do produto, que fica retido dentro da plataforma, após isso o vendedor começa o desenvolvimento, quando o produto está finalizado o consumidor é notificado e deve pagar a segunda parte do valor.

Quando a segunda parte do valor é paga o vendedor envia o produto, após a confirmação da entrega do produto por parte do consumidor o valor retido na plataforma é enviado para o vendedor com o desconto da plataforma
```mermaid
graph TD;

    Fat[Faturamento]-->PagamentoInicial[Comprador escolhe a forma de pagamento e faz o pagamento inicial]
    PagamentoInicial --> InicioDoDesenvolvimento[Vendedor ou Prestador de serviço começa o desenvolvimento da aplicação]
    InicioDoDesenvolvimento--> FimDoDev[Aviso de Desenvolvimento Finalizado]
    FimDoDev --> SolcitacaoPagamentoParte2[Comprador é solicitado para o pagamento da segund parte do valor do produto]
    SolcitacaoPagamentoParte2 --> |Pagamento é realizado|EntregaProd[Produto é entrege para o consumidor]
    SolcitacaoPagamentoParte2 -->|Pagamento não realizado| CancelamentoPorNaoPagamento[ A transação é cancelada e o valor inicial é retornado para o comprador]
    EntregaProd -->|Comprador confirma recebimento| PagamentoAoVendedor[Vendedor recebe o valor, apos confirmação]
    PagamentoAoVendedor--> Avaliacao[Avaliação]
    CancelamentoPorNaoPagamento --> Avaliacao
```

# Processo de Venda 

O processo de venda se inicia quando o comprador escolhe um produto/serviço e o adiciona no carrinho de compras, após isso fazemos a verificação de conta onde pode ser necessário ou não direcionar o cliente para o processod de cadastro.

Após isso um chat com o vendedor é aberto onde pode ocorrer negecociações ou esclarecimento de dúvidas.
Com todos os pontos em ordem iniciamos o processo de faturamento
```mermaid
graph TD;

    InicioVenda[Início processo de venda] --> EscolherProduto[Escolher Produto]
    EscolherProduto --> Carrinho[Carrinho]
    Carrinho --> VerificaExistenciaConta{Possui Conta?}
    VerificaExistenciaConta -- Não --> Cadastrar[Criar conta]
    VerificaExistenciaConta -- Sim --> Negociar[Negociação com o Vendedor]
    Cadastrar --> Negociar
    Negociar --> ProcessoFaturamento[Inicio do processo de Faturamento]
    ProcessoFaturamento --> FimVenda[Fim]
```

# Processo de Avaliação
```mermaid
graph TD;

    A[1 Mês após o uso do projeto desenvolvido] --> B[Envio do formulário questionando sobre a plataforma]
    B --> C[Dados obtidos]
    C --> D[Fim]
```

# Processo de Cancelamento
```mermaid
graph TD;

    A[Início: Solicitação de Cancelamento] --> B{Vendedor quem solicitou?}
    B --> |Sim| C[Notificação para o comprador]
    B --> |Não| D[Notificação para o vendedor]
    C --> E[Valor não é passado para o vendedor e a transação é encerrada]
    D --> F[Valor da metade inicial é pago ao vendedor]
    F --> Final[Fim da transação]
    E --> Final
```

# Processo de Mudança de Tipo de Conta
```mermaid
graph TD;

    A[Mudança de conta] --> B[Solicitação de alteração de conta consumer para vendedor]
    B --> C[Solicitação de informações técnica]
    C --> D[Solicitação de informações bancarias]
    D --> E[Inserir portfolio]
    E --> F[Escolha categoria de atuação]
    F --> G[Operação realizada]
```
