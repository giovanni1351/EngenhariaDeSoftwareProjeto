# Objetivo do Documento:

Este documento tem como objetivo documentar e também apresentar a definição e o detalhamento da arquitetura adotada para o desenvolvimento do projeto com foco em atender as espectativas 
e regras de negócio definidas
Além disso, inclui um diagrama representativo da arquitetura proposta e a análise dos Requisitos Não Funcionais que influenciaram diretamente na escolha da solução arquitetural.


# Escolha de Padrões Arquiteturais:

A arquitetura escolhida para o projeto é uma combinação entre a arquitetura Cliente-Servidor, o padrão MVC e a arquitetura em 3 Camadas. Nesse modelo, a estrutura mais externa segue o padrão Cliente-Servidor, em que o cliente é responsável por realizar requisições e consumir os serviços disponibilizados pelo servidor.

No lado do servidor, aplicamos a arquitetura em 3 Camadas juntamente com o padrão MVC, organizando a aplicação em camadas de apresentação, lógica de negócio e acesso a dados. Essa abordagem permite encapsular toda a lógica operacional, regras de negócio e manipulação de dados no servidor, mantendo o cliente como um componente leve e focado apenas na solicitação e no consumo dos serviços.

# Projeto de Arquitetura:

Descrição das camadas e seus componentes:

- Camada de Apresentação:
Responsável pela interação com o usuário, tratando a entrada e a saída de dados, sendo encarregada de exibir informações e capturar ações do usuário, como preenchimento de formulários e solicitações de compra na nossa plataforma.

- Camada de Lógica de Negócio:
Tem como função processar as regras de negócio da aplicação necessárias para atender as solicitações do cliente de forma segura, rápida e eficiente 

- Camada de Acesso a Dados:
Gerencia a comunicação com o banco de dados ou outros sistemas de armazenamento. Executa operações como SELECT, INSERT, UPDATE e DELETE. Sua principal responsabilidade é abstrair o acesso aos dados, permitindo que a lógica de negócio não dependa diretamente da forma como os dados são armazenados ou recuperados.

Camada de Apresentação: (Olhar nossas interfaces)
Tela de Cadastro
Tela de Login
Tela do Carrinho
Tela de Pagamento(sera que podemos juntar carrinho com pagamento?)
Tela Historico de Compras
Tela Listagem de Produtos (exibir os produtos)
Tela de Mudança de Conta
Tela de Minhas Vendas
Tela de Perfil do Usuário
Tela de Recuperação de senha
Tela de Cadastro de Produto
Tela de Produtos Cadastrados
Tela de Mensagens
Tela de Avaliação
Tela de Canceleamento


Camada de Lógica de Negócio:(Podemos olhar as nossas  regras de negocio)
Validação de login e senha
Regras de cadastro de produtos
Cálculo de preço e frete
Regras de faturamento e cancelamento
Verificação de permissões na mudança de conta
Registro e exibição de avaliações


Camada de Acesso a Dados:
Tabela de Usuários
Tabela de Produtos
Tabela de Pedidos
Tabela de Avaliações
Tabela de Transações
