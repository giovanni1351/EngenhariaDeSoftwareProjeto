# Apresentação TechSales - Engenharia de Software

## Índice
1. [Metodologia Ágil Recomendada](#metodologia-ágil-recomendada)
2. [Stakeholders do Sistema](#stakeholders-do-sistema)
3. [Técnica de Coleta de Requisitos](#técnica-de-coleta-de-requisitos)
4. [Requisitos Funcionais](#requisitos-funcionais)
5. [Requisitos Não Funcionais](#requisitos-não-funcionais)
6. [Regras de Negócio](#regras-de-negócio)
7. [Protótipos das Interfaces Gráficas](#protótipos-das-interfaces-gráficas)
8. [Histórias de Usuário](#histórias-de-usuário)
9. [Conclusão](#conclusão)

## Metodologia Ágil Recomendada

Nosso grupo concordou com o uso do **Scrum** e do **Kanban**

### Justificativa:

Escolhemos essas metodologias por que com a divisão do trabalho em sprints e histórias de usuário podemos ter uma evolução contínua e organizada, evitando retrabalho e tendo o progresso documentado para que possamos reaproveitar em momentos futuros. Somando isso com quadro Kanban podemos também facilitar o acompanhamento do fluxo de trabalho e evolução. Dessa forma podemos evoluir de uma maneira mais efetiva, sistemática e organizada

## Stakeholders do Sistema

### 1. Compradores/Consumidores
- **Impacto:** Usuários que buscam produtos/serviços de tecnologia na plataforma.
- **Interesses:** Interface intuitiva, segurança nas transações, comunicação eficiente com vendedores, avaliações confiáveis.

### 2. Vendedores/Anunciantes
- **Impacto:** Profissionais ou empresas que oferecem produtos/serviços tecnológicos.
- **Interesses:** Visibilidade, ferramentas de análise, facilidade para cadastrar produtos, sistema de pagamento confiável.

### 3. Administradores da Plataforma
- **Impacto:** Responsáveis pela gestão da plataforma.
- **Interesses:** Métricas de desempenho, ferramentas de moderação, cadastro de categorias.

### 4. Investidores/Proprietários
- **Impacto:** Financiadores e proprietários do negócio.
- **Interesses:** Lucratividade, crescimento, integridade operacional.

### 5. Equipe de Suporte
- **Impacto:** Funcionários que lidam com problemas e dúvidas dos usuários.
- **Interesses:** Ferramentas eficientes para resolução de problemas.

### 6. Reguladores/Órgãos Fiscalizadores
- **Impacto:** Entidades que regulam o comércio eletrônico.
- **Interesses:** Conformidade legal, proteção ao consumidor.

## Técnica de Coleta de Requisitos

Para o TechSales, a técnica mais adequada para coleta de requisitos seria a **combinação de workshops de requisitos com entrevistas direcionadas e prototipação**.

### Justificativa:

1. **Workshops de Requisitos:**
   - Permitem reunir representantes de diferentes stakeholders (compradores, vendedores, administradores).
   - Facilitam a discussão colaborativa sobre os processos complexos (faturamento, cancelamento).
   - Auxiliam na identificação de conflitos de requisitos entre diferentes partes interessadas.

2. **Entrevistas Direcionadas:**
   - Fornecem insights específicos de cada tipo de usuário.
   - Permitem aprofundar em necessidades particulares (vendedores precisam de ferramentas analíticas diferentes dos compradores).
   - Capturam expectativas e preocupações individuais.

3. **Prototipação:**
   - Essencial para validar o design das múltiplas telas mencionadas no documento.
   - Permite que stakeholders visualizem a implementação antes do desenvolvimento completo.
   - Facilita a coleta de feedback sobre usabilidade em estágios iniciais.

4. **Análise de Sistemas Similares:**
   - Complementarmente, analisar outros marketplaces para identificar boas práticas e diferenciais competitivos.

### Processo de Coleta:

1. Iniciar com workshops para entender processos de negócio macro.
2. Realizar entrevistas individuais com representantes de cada stakeholder.
3. Desenvolver protótipos baseados nas informações coletadas.
4. Validar protótipos em sessões de feedback com stakeholders.
5. Refinar requisitos com base no feedback.
6. Documentar requisitos no formato de histórias de usuário para o backlog.

## Requisitos Funcionais

### RF01 - Gerenciamento de Usuários
- RF01.1: O sistema deve permitir o cadastro de novos usuários com nome, CPF, e-mail, senha, data de nascimento, telefone e endereço.
- RF01.2: O sistema deve validar o formato do e-mail, autenticidade do documento e segurança da senha.
- RF01.4: O sistema deve permitir login de usuários cadastrados.
- RF01.5: O sistema deve permitir a alteração de conta de comprador para vendedor.

### RF02 - Gerenciamento de Produtos
- RF02.1: O sistema deve permitir que vendedores cadastrem produtos com nome, descrição, preço, categoria e porcentagem de comissão.
- RF02.2: O sistema deve permitir o upload de imagens para os produtos.
- RF02.3: O sistema deve permitir a edição e remoção de produtos cadastrados.
- RF02.4: O sistema deve categorizar produtos por área de atuação.
- RF02.5: O sistema deve exibir produtos em destaque na página inicial.

### RF03 - Processo de Compra
- RF03.1: O sistema deve permitir adicionar produtos ao carrinho de compras.
- RF03.2: O sistema deve permitir que compradores visualizem detalhes dos produtos.
- RF03.3: O sistema deve fornecer um chat para negociação entre comprador e vendedor.
- RF03.4: O sistema deve permitir pagamento em duas etapas (metade inicial e metade final).
- RF03.5: O sistema deve notificar vendedores sobre novas compras.

### RF04 - Faturamento e Pagamento
- RF04.1: O sistema deve processar pagamentos em duas etapas.
- RF04.2: O sistema deve reter valores até a confirmação da entrega.
- RF04.4: O sistema deve transferir valores para a conta do vendedor após confirmação.
- RF04.5: O sistema deve gerar comprovantes de pagamento.

### RF05 - Avaliação e Feedback
- RF05.1: O sistema deve enviar formulário de avaliação um mês após a compra.
- RF05.2: O sistema deve permitir avaliação do produto, vendedor e plataforma.
- RF05.3: O sistema deve exibir média de avaliações nos perfis dos vendedores.
- RF05.4: O sistema deve permitir comentários sobre produtos e vendedores.

### RF06 - Cancelamento
- RF06.1: O sistema deve permitir solicitações de cancelamento por compradores ou vendedores.
- RF06.2: O sistema deve processar reembolsos ou pagamentos conforme a origem do cancelamento.
- RF06.3: O sistema deve notificar as partes envolvidas sobre cancelamentos.

### RF07 - Administração
- RF07.1: O sistema deve permitir que administradores gerenciem categorias de produtos.
- RF07.2: O sistema deve fornecer métricas e relatórios para administradores.
- RF07.3: O sistema deve permitir a moderação de avaliações e comentários.
- RF07.4: O sistema deve permitir definir áreas de destaque na página inicial.

### RF08 - Análise para Vendedores
- RF08.1: O sistema deve fornecer análises de vendas para vendedores.
- RF08.2: O sistema deve fornecer análises comerciais para vendedores.
- RF08.3: O sistema deve exibir histórico de vendas e pagamentos.

## Requisitos Não Funcionais



### Requisitos de Performance
- RNF01: O sistema deve carregar a página inicial em menos de 3 segundos.
- RNF02: O sistema deve processar pagamentos em menos de 10 segundos.
- RNF03: O sistema deve suportar até 10.000 usuários simultâneos.
- RNF04: O sistema deve processar até 1.000 transações por minuto.
- RNF05: O tempo de resposta para pesquisas não deve exceder 2 segundos.

### Requisitos de Segurança
- RNF06: Todas as transações devem ser criptografadas usando protocolo SSL/TLS.
- RNF07: Senhas devem ser armazenadas com hash e salt.
- RNF08: O sistema deve implementar autenticação de dois fatores.
- RNF09: O sistema deve bloquear contas após 5 tentativas incorretas de login.
- RNF10: O sistema deve realizar backups diários dos dados.

### Requisitos de Disponibilidade
- RNF11: O sistema deve ter disponibilidade de 99,9% (downtime máximo de 8,76 horas/ano).
- RNF12: Manutenções programadas devem ser realizadas em horários de baixo uso.
- RNF13: O sistema deve implementar redundância para pontos críticos de falha.
- RNF14: O tempo de recuperação após falha não deve exceder 30 minutos.

### Requisitos de Usabilidade
- RNF15: O sistema deve ser compatível com os principais navegadores (Chrome, Firefox, Safari, Edge).
- RNF16: A interface deve ser responsiva e funcionar em dispositivos móveis e desktop.
- RNF17: O sistema deve seguir diretrizes de acessibilidade WCAG 2.1.
- RNF18: O sistema deve fornecer feedback claro para ações dos usuários.
- RNF19: A interface deve ser intuitiva, requerendo no máximo 3 cliques para funções principais.

### Requisitos de Interoperabilidade
- RNF20: O sistema deve fornecer APIs RESTful para integração com sistemas externos.
- RNF21: O sistema deve suportar múltiplas gateways de pagamento.
- RNF22: O sistema deve permitir exportação de dados em formatos padrão (CSV, JSON).
- RNF23: O sistema deve suportar single sign-on (SSO) com contas Google e Facebook.

### Requisitos Operacionais
- RNF24: O sistema deve ser desenvolvido usando arquitetura de microsserviços.
- RNF25: O sistema deve utilizar contêineres Docker para facilitar implantação.
- RNF26: O sistema deve implementar monitoramento em tempo real com alertas automáticos.
- RNF27: O código deve seguir padrões de qualidade verificados por ferramentas automatizadas.
- RNF28: O sistema deve manter logs detalhados para auditoria e resolução de problemas.

### Requisitos Organizacionais
- RNF29: O sistema deve ser desenvolvido utilizando a linguagem de programação Python.
- RNF30: O desenvolvimento deve seguir metodologias ágeis, como Scrum.
- RNF31: A equipe de desenvolvimento deve realizar revisões de código regulares.
- RNF32: O sistema deve ser implantado em um ambiente de nuvem seguro e escalável.

### Requisitos Externos
- RNF33: O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD).
- RNF34: O sistema deve atender às regulamentações de comércio eletrônico vigentes.
- RNF35: O sistema deve seguir práticas éticas de desenvolvimento, garantindo privacidade e segurança dos dados dos usuários.
- RNF36: O sistema deve ser auditável para garantir conformidade com requisitos legais e regulatórios.

### Requisitos de Ética
- RNF37: O sistema deve garantir a privacidade dos dados dos usuários, não compartilhando informações sem consentimento explícito.
- RNF38: O sistema deve implementar mecanismos para evitar discriminação e preconceito em suas funcionalidades.
- RNF39: O sistema deve fornecer transparência sobre o uso de dados e algoritmos utilizados.
- RNF40: O sistema deve permitir que os usuários controlem suas próprias informações e decidam sobre seu uso.
- RNF41: O sistema deve promover práticas de comércio justo, evitando práticas enganosas ou fraudulentas.
- RNF42: O sistema deve garantir acessibilidade para todos os usuários, incluindo aqueles com deficiências.
- RNF43: O sistema deve ser projetado para minimizar impactos ambientais, utilizando recursos de forma eficiente.

## Regras de Negócio

### Gerais
- RN01: Todo usuário inicialmente é registrado como comprador.
- RN02: Para se tornar vendedor, o usuário deve fornecer informações técnicas, bancárias e portfólio.
- RN03: Um mesmo usuário não pode comprar seus próprios produtos.

### Anúncios e Comissões
- RN04: O vendedor define a porcentagem de comissão para a plataforma (valor mínimo a definir).
- RN05: Produtos com maior porcentagem de comissão recebem maior destaque na plataforma.
- RN06: A sazonalidade dos anúncios em destaque deve garantir visibilidade justa a todos os anunciantes.
- RN07: Produtos com boa média de vendas e alta confiabilidade ganham espaço no carrossel fixo.

### Pagamentos e Faturamento
- RN08: Todo pagamento é dividido em duas etapas (metade inicial, metade final).
- RN09: A metade inicial é retida pela plataforma até a conclusão da venda.
- RN10: A segunda metade só é solicitada após o vendedor finalizar o desenvolvimento/preparação.
- RN11: O valor é liberado para o vendedor somente após confirmação de entrega pelo comprador.
- RN12: A plataforma retém a porcentagem acordada antes de repassar o valor ao vendedor.

### Cancelamentos
- RN13: Se o vendedor solicitar cancelamento, o valor pago é estornado integralmente ao comprador.
- RN14: Se o comprador solicitar cancelamento, o valor da primeira parcela é destinado ao vendedor como compensação.
- RN15: Após a entrega do produto, não é possível realizar cancelamento, apenas acionamento de garantias se aplicável.

### Avaliações
- RN16: A avaliação do produto só pode ser realizada após 1 mês de uso.
- RN17: Apenas compradores que finalizaram a compra podem avaliar produtos e vendedores.
- RN18: Avaliações são consideradas no algoritmo de destaque de produtos e vendedores.

### Cadastro de Produtos
- RN19: Todos os produtos devem pertencer a pelo menos uma categoria.
- RN20: Imagens de produtos devem seguir padrões definidos (dimensões, tamanho).
- RN21: Descrições de produtos devem ter um mínimo de caracteres para garantir informações adequadas.

## Protótipos das Interfaces Gráficas

*Nota: Aqui seriam incluídas imagens dos protótipos. Como não é possível incluir imagens diretamente, fornecemos a descrição detalhada das telas principais.*

### 1. Tela Principal/Home
- Banner superior com logo TechSales
- Barra de pesquisa centralizada
- Menu de navegação (Categorias, Minha Conta, Carrinho)
- Carrossel central com produtos em destaque (baseado na comissão)
- Carrossel fixo à direita com produtos confiáveis (alta avaliação)
- Grid de produtos organizados por categorias
- Footer com informações de contato e links úteis

### 2. Tela de Cadastro/Login
- Formulário de cadastro com campos:
  - Nome completo
  - CPF
  - E-mail
  - Senha
  - Confirmação de senha
  - Data de nascimento
  - Telefone
  - Endereço
- Opção alternativa para login
- Verificação de segurança (CAPTCHA)
- Botões "Cadastrar" e "Já tenho conta"

### 3. Tela de Produto
- Galeria de imagens do produto
- Informações detalhadas (nome, preço, descrição)
- Avaliações e comentários de compradores
- Informações do vendedor (perfil, avaliação)
- Botão "Adicionar ao Carrinho"
- Botão "Iniciar Chat com Vendedor"
- Produtos relacionados

### 4. Carrinho de Compras
- Lista de produtos selecionados
- Opções de quantidade
- Valor total
- Opção de remover itens
- Botão "Continuar Comprando"
- Botão "Finalizar Compra"

### 5. Tela de Pagamento
- Resumo da compra
- Explicação do processo de pagamento em duas etapas
- Opções de forma de pagamento
- Campos para informações financeiras
- Termos e condições
- Botão "Pagar Primeira Parcela"

### 6. Dashboard de Vendedor
- Visão geral (vendas recentes, faturamento, avaliações)
- Menu lateral (Meus Produtos, Cadastrar Produto, Análise de Vendas, Chats)
- Gráficos de desempenho
- Notificações de novas compras/mensagens
- Tabela de produtos com status e métricas

### 7. Tela de Cadastro de Produto
- Formulário com campos:
  - Nome do produto
  - Categoria (dropdown)
  - Descrição detalhada (editor rico)
  - Preço
  - Porcentagem de comissão para plataforma
  - Upload de imagens
- Prévia do anúncio
- Botão "Publicar Produto"

### 8. Tela de Administração
- Painel de controle com métricas gerais
- Gerenciamento de categorias
- Moderação de avaliações
- Relatórios financeiros
- Configurações de destaque na home

## Histórias de Usuário

### Para Compradores

**HU01:** Como comprador, quero me cadastrar na plataforma para poder comprar produtos tecnológicos.
- **Critérios de Aceitação:**
  - Formulário de cadastro com validação de campos
  - E-mail de confirmação enviado
  - Acesso à conta após confirmação

**HU02:** Como comprador, quero navegar por categorias de produtos para encontrar o que preciso.
- **Critérios de Aceitação:**
  - Menu de categorias acessível
  - Filtros por preço e avaliação
  - Grid de produtos com informações básicas

**HU03:** Como comprador, quero adicionar produtos ao carrinho para finalizar minha compra posteriormente.
- **Critérios de Aceitação:**
  - Botão "Adicionar ao Carrinho" em cada produto
  - Notificação de produto adicionado
  - Contador no ícone do carrinho

**HU04:** Como comprador, quero conversar com o vendedor antes da compra para esclarecer dúvidas.
- **Critérios de Aceitação:**
  - Botão para iniciar chat com vendedor
  - Interface de chat funcional
  - Notificações de novas mensagens

**HU05:** Como comprador, quero realizar o pagamento em duas etapas para garantir a entrega do produto.
- **Critérios de Aceitação:**
  - Processo de pagamento claro
  - Confirmação do pagamento inicial
  - Notificação para pagamento final

**HU06:** Como comprador, quero avaliar um produto após utilizá-lo para ajudar outros compradores.
- **Critérios de Aceitação:**
  - Formulário de avaliação enviado após 1 mês
  - Opção de classificar produto, vendedor e plataforma
  - Comentário publicado após moderação

**HU07:** Como comprador, quero visualizar meu histórico de compras para acompanhar meus pedidos.
- **Critérios de Aceitação:**
  - Lista de compras com status
  - Opção de acessar detalhes da compra
  - Filtros por data e status

### Para Vendedores

**HU08:** Como vendedor, quero mudar minha conta de comprador para vendedor para oferecer meus produtos.
- **Critérios de Aceitação:**
  - Formulário para informações técnicas e bancárias
  - Upload de portfólio
  - Seleção de áreas de atuação

**HU09:** Como vendedor, quero cadastrar um novo produto com detalhes e imagens para atrair compradores.
- **Critérios de Aceitação:**
  - Formulário completo de cadastro
  - Upload de múltiplas imagens
  - Definição da porcentagem de comissão

**HU10:** Como vendedor, quero ser notificado sobre novas vendas para iniciar o desenvolvimento.
- **Critérios de Aceitação:**
  - Notificação em tempo real
  - E-mail informativo
  - Detalhes da venda acessíveis

**HU11:** Como vendedor, quero acessar análises de vendas para entender meu desempenho.
- **Critérios de Aceitação:**
  - Gráficos de vendas por período
  - Métricas de conversão
  - Comparativo com médias da plataforma

**HU12:** Como vendedor, quero informar quando o produto está pronto para solicitar o pagamento final.
- **Critérios de Aceitação:**
  - Botão para marcar desenvolvimento como concluído
  - Notificação automática ao comprador
  - Status da venda atualizado

**HU13:** Como vendedor, quero receber o pagamento após a confirmação de entrega para garantir minha remuneração.
- **Critérios de Aceitação:**
  - Confirmação de recebimento pelo comprador
  - Processamento do pagamento com dedução da comissão
  - Comprovante de pagamento disponível

### Para Administradores

**HU14:** Como administrador, quero gerenciar categorias de produtos para organizar a plataforma.
- **Critérios de Aceitação:**
  - Interface para adicionar/editar/remover categorias
  - Associação de produtos às categorias
  - Hierarquia de categorias

**HU15:** Como administrador, quero definir áreas de destaque na home para produtos com maior comissão.
- **Critérios de Aceitação:**
  - Configuração de banners e carrosséis
  - Algoritmo de rotação baseado em comissão
  - Visibilidade justa entre anunciantes

**HU16:** Como administrador, quero acessar relatórios de desempenho para monitorar a saúde da plataforma.
- **Critérios de Aceitação:**
  - Dashboard com KPIs principais
  - Filtros por período e categoria
  - Exportação de relatórios

**HU17:** Como administrador, quero moderar avaliações para garantir conteúdo adequado.
- **Critérios de Aceitação:**
  - Fila de moderação
  - Opções de aprovar/rejeitar
  - Filtros por tipo de conteúdo

## Conclusão

O projeto TechSales apresenta características de um marketplace de tecnologia com processos bem definidos e fluxos de trabalho detalhados. A metodologia Scrum com elementos de Kanban é a mais adequada para o desenvolvimento, permitindo entregas incrementais e adaptação às necessidades dos stakeholders.

A implementação deve focar inicialmente nos requisitos funcionais essenciais (cadastro, login, produtos, vendas), seguidos pelos processos de suporte (avaliação, cancelamento). Os requisitos não funcionais, especialmente segurança e usabilidade, são críticos para o sucesso da plataforma.

As histórias de usuário apresentadas formam um backlog inicial para o desenvolvimento, priorizando a experiência de compradores e vendedores. A atenção às regras de negócio garantirá que o sistema atenda às expectativas de todos os stakeholders identificados.

O próximo passo é definir o backlog priorizado, formar o time Scrum e iniciar o planejamento da primeira sprint, focando nas funcionalidades básicas que permitirão validar a proposta de valor da plataforma.









Pergunta 1
Remover:
Item 2 (Kanban)
Pq não usar outras metodologias


Melhorias:
Unir as justificativas Scrum e Kanban em um único texto

Pergunta 2
	Remover:
		Riscos

	Melhorias:
		Reescrever tudo de uma maneira mais clara e objetiva


Pergunta 3:
	Remover:
		Workshop de requisitos
		Analise de Sistemas 
Similares
		Entrevistas Direcionadas
		Analise de Documentos
		Processo de Coleta
		

	Adicionar:
		Brainstorming
		Questionário

Pergunta 4:
	Remover os tópicos
	Alterar a escrita de (RF01.1, RF01.2) para RF01 e RF02

	Implementar RF02.5: O sistema deve exibir produtos em destaque na página inicial.


RF:
o sistema deve permitir inserir informações técnicas e bancarias para o cadastro do vendedor.

O SISTEMA DEVE PERMITIR QUE O VENDEDOR CONSIGA CADASTRAR SEU PORTFOLIO

O VENDEDOR DEVE CONSEGUIR INSERIR OU EDITAR A AREA DE ATUACAO(EDITAR ESSE PROCESSO MUDANCA DE TIPO DE CONTA)




RF04.3: O sistema deve calcular automaticamente a comissão da plataforma.

ME PARECE SER UM REGRA DE NEGOCIO

