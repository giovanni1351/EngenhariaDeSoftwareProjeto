# Requisitos Funcionais

## 1) Gerenciamento de usuários

- **RF01:** O sistema deve permitir o cadastro de novos usuários.
- **RF02:** O sistema deve validar o formato do e-mail, autenticidade do documento e segurança da senha.
- **RF03:** O sistema deve permitir login de usuários cadastrados.
- **RF04:** O sistema deve permitir a alteração de conta de comprador para vendedor.
- **RF05:** O sistema deve oferecer suporte para recuperação de senha em caso de esquecimento.
- **RF06:** O sistema deve permitir que o usuário atualize suas informações pessoais.
- **RF07:** O sistema deve permitir que o usuário personalize as configurações de notificações.
- **RF08:** O sistema deve permitir que o usuário navegue entre as páginas.
- **RF09:** O sistema deve permitir que o vendedor adicione informações como portifólio, redes sociais, diplomas e conta bancária
  
## 2) Mensagens entre os clientes

- **RF10:** O sistema deve garantir a comunicação entre usuário e comprador.

## 3) Pagamento

** Confirmar com a Gabriela **(
- **RF11:** O sistema deve processar o pagamento da primeira etapa referente ao produto e reter o montante correspondente na plataforma até a confirmação da entrega pelo comprador.
- **RF12:** O sistema deve processar o pagamento da segunda etapa, calcular o valor líquido a ser repassado ao vendedor (deduzindo a comissão da plataforma do valor total) e efetuar a liberação do montante após a confirmação da entrega pelo comprador.
)


- **RF13:** O sistema deve processar pagamentos em duas etapas.
- **RF14:** O sistema deve reter valores até a confirmação da entrega.
- **RF15:** O sistema deve transferir o valor da venda para a conta do vendedor, deduzida a comissão da plataforma, após a confirmação de entrega pelo comprador.
- **RF16:** O sistema deve gerar comprovantes de pagamento.
- **RF17:** O sistema deve permitir que o usuário cadastre as informações do cartão.
- **RF18:** O sistema deve permitir que o usuário escolha diferentes formas de pagamento, exemplo: cartão de crédito, transferência bancária e PIX.

## 4) Navegação do site/Compra de produto

- **RF19:** O sistema deve exibir os produtos cadastrados pelos vendedores.
- **RF20:** O sistema deve permitir que o usuário pesquise produtos específicos.
- **RF21:** O sistema deve permitir adicionar produtos ao carrinho de compras.
- **RF22:** O sistema deve permitir que compradores visualizem detalhes dos produtos.
- **RF23:** O sistema deve exibir os produtos em destaque.
- **RF24:** O sistema deve permitir que o usuário filtre os produtos por categoria e avaliação.
- **RF25:** O sistema deve exibir as avaliações.
- **RF26:** O sistema deve exibir as compras realizadas pelo usuário.
- **RF27:** O sistema deve permitir que o usuário filtre o produto do histórico de compras.
- **RF28:** O sistema deve notificar as novidades do site, caso o cliente cadastre seu email no newsletter.


## 5) Cadastro de produtos

- **RF29:** O sistema deve permitir que vendedores cadastrem produtos ex: nome, descrição, imagem, preço, categoria, detalhes adicionais e comissão da plataforma.
- **RF30:** O sistema deve permitir o upload de imagens para os produtos.
- **RF31:** O sistema deve permitir a edição e remoção de produtos cadastrados.

## 6) Avaliação

- **RF32:** O sistema deve permitir avaliação do produto, vendedor e plataforma.
- **RF33:** O sistema deve enviar dois formulários de avaliação, um imediamente após a compra do produto e outro 30 dias após a compra do produto, caso o comprador não tenha feito a avaliação

## 7) Cancelamento

- **RF34:** O sistema deve permitir solicitações de cancelamento por compradores ou vendedores.
- **RF35:** O sistema deve processar reembolsos ou pagamentos conforme a origem do cancelamento.
- **RF36:** O sistema deve notificar as partes envolvidas sobre o cancelamento.

