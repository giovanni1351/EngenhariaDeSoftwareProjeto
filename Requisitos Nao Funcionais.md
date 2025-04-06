# Requisitos Não Funcionais



## 1) Regras Gerais:

- **RNF01:** O sistema estará disponível 24 x 7, com disponibilidade de 99,98%.
- **RNF02:** O sistema será desenvolvido com a linguagem de programação Python.
- **RNF03:** Os dados serão armazenados em um banco de dados relacional SQL Server.
- **RNF04:** O sistema deverá atender às normas da LGPD.
- **RNF05:** O sistema deve suportar Gateways de Pagamento.
- **RNF06:** O sistema deve realizar backup diariamente dos dados.
- **RNF07:** O sistema deve ser implantado em um ambiente de computação em Nuvem.
- **RNF08:** As informações serão criptografadas.
- **RNF09:** O sistema deve utilizar a ferramenta Docker.
- **RNF10:** O sistema deve ter interface intuitiva, com fácil acesso às funções principais do sistema e com campos descritivos.
- **RNF11:** O sistema deve voltar ao ar em caso de falha em até 30 minutos.
- **RNF12:** O sistema deve suportar até 100.000 usuários simultâneos.
- **RNF14:** O sistema deve ser compatível com os principais navegadores (Chrome, Firefox, Safari, Edge).
- **RNF15:** A interface deve ser responsiva e funcionar em dispositivos móveis e desktop.
- **RNF16:** O sistema deve disponibilizar APIs para consulta de dados pessoais.
- **RNF17:** O sistema deve ser capaz de enviar e-mails automaticamente para notificações, confirmações e comunicados relevantes aos usuários. 

## 2) Gerenciamento de usuários

- **RNF18:** Os usuários serão identificados com email e senha. 
- **RNF19:** O tempo de resposta para o cadastro de um usuário será de até 3 segundos. 
- **RNF20:** O sistema deve permitir ao vendedor exportar seu histórico de vendas.
- **RNF21:** O sistema deve fornecer retornos de ação para o usuário em casos:
    - Compra
    - Venda
    - Produto adicionado ou removido no carrinho
    - Produto anunciado
    - Produto entregue
    - Atualização de informações
    - Avaliação
    - Cancelamento
    - Pagamento
    - Cadastro, Login ou Logout realizado

- **RNF22:** O sistema deve notificar o comprador sobre uma venda em até 5 segundos após a confirmação da compra.
- **RNF23:** O sistema deve possuir o calculo para a validação do CPF fornecido pelo usuário é válido.
- **RNFX:** O sistema deve validar a existencia da conta bancaria do usuario vendedor
- **RNFX:** O sistema deve validar as informações do cartão de credito do comprador
- **RNFX:** O sistema deve aceitar varios metodos de pagamento
- **RNFX:**  O sistema deve verificar a nova senha com a anterior para realizar a troca de senha
- **RNFX:** O sistema tem que conter sistema de aramazenamento de arquivos, para guardar os portifolios dos vendedores
- **RNFX:** O sistema deve atualizar as informações diretamento no banco de dados em menos de 2 segundos
- **RNFX:** O sistema deve verificar a data das entregas todos os dias para o envio dos formularios de avaliação
- **RNFX:** O sistema deve enviar um e-mail ao usuário comprador 30 dias após a data da compra, caso a avaliação correspondente ainda não tenha sido realizada.
- **RNFX:** O sistema deve armazenar os comentarios dos produtos 
- **RNFX:** O sistema deve armazenar as avaliações e utilizar para algoritmos de recomendação
- **RNFX:** O sistema deve ser capas de realizar filtros por meio das avaliações
- **RNFX:** O sistema deve calcular juros para parcelamentos para certa quantidade de vezes
## 3) Navegação do site/Compra de produto
- **RNF24:** O sistema deve retornar uma pesquisa feita pelo usuário em 2 segundos.
- **RNF25:** O sistema deve carregar a página do site em menos de 3 segundos.


## 4)Pagamentos
- **RNF26:** O sistema deve processar pagamentos em menos de 10 segundos.
- **


## 
