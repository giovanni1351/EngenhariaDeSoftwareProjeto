# Objetivo do Documento:

Este projeto tem como objetivo principal definir e documentar a arquitetura de software de um sistema, por meio da escolha e justificativa de padrões arquiteturais adequados à sua proposta. Busca-se organizar de forma estruturada os componentes do sistema, identificando suas camadas, serviços e relacionamentos, a fim de garantir uma arquitetura coesa, escalável e de fácil manutenção. Além disso, o documento visa detalhar os requisitos não funcionais que influenciaram as decisões arquiteturais, como desempenho, segurança, manutenibilidade e interoperabilidade, assegurando que a solução atenda às necessidades técnicas e de negócio de forma eficiente.


# Escolha de Padrões Arquiteturais:

A arquitetura escolhida foi Arquitetura em Camadas (3 camdadas), sendo elas apresentação, lógica de negócio e acesso a dados. Essa estrutura facilita a organização do sistema, separando responsabilidades e promovendo um desenvolvimento mais limpo e sustentável. 
Entre as principais vantagens dessa abordagem estão: facilidade de manutenção, possibilidade de substituir ou atualizar uma camada sem afetar as demais, desenvolvimento paralelo entre equipes e maior organização do código.


# Projeto de Arquitetura:

Descrição das camadas e seus componentes:

- Camada de Apresentação:
Responsável pela interação com o usuário, tratando a entrada e a saída de dados. Engloba interfaces gráficas (como páginas web ou aplicativos móveis), sendo encarregada de exibir informações e capturar ações do usuário, como cliques e preenchimento de formulários.

- Camada de Lógica de Negócio:
Tem como função processar as regras de negócio da aplicação. É responsável por decisões como validar dados, verificar se um usuário já existe antes do cadastro. Atua como intermediária entre a apresentação e os dados, centralizando a lógica da aplicação.

- Camada de Acesso a Dados:
Gerencia a comunicação com o banco de dados ou outros sistemas de armazenamento. Executa operações como SELECT, INSERT, UPDATE e DELETE. Sua principal responsabilidade é abstrair o acesso aos dados, permitindo que a lógica de negócio não dependa diretamente da forma como os dados são armazenados ou recuperados.


-- OBS:
no item 3 perguntamos ao professor o que precisavamos colocar no item 3, e ele disse para detalhar as camadas. Fiquei com duvida se o que esta escrito acima responde a pergunta, ou seria necessario colocolar algo como:

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