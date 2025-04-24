# Diagramas de Contexto - TechSales

## 1. Processo de Cadastro

```mermaid
graph TD
    Usuario[Usuário] -- Solicita Cadastro / Fornece Dados --> Sistema((Sistema de cadastro))
    Sistema -- Confirma Cadastro / Envia Email --> Usuario
```

## 2. Processo de Login

```mermaid
graph TD
    Usuario[Usuário] -- Tenta Login (Fornece Credenciais) --> Sistema((Sistema de login))
    Sistema -- Concede ou Nega Acesso --> Usuario
```

## 3. Processo de Venda

```mermaid
graph TD
    Comprador[Comprador] -- Interage com Venda (Seleciona, Negocia, Confirma) --> Sistema((Sistema de vendas))
    Sistema -- Processa Venda / Atualiza Comprador --> Comprador
    Vendedor[Vendedor] -- Responde Negociação --> Sistema
    Sistema -- Facilita Chat / Notifica Vendedor --> Vendedor
    Sistema -- Inicia Processo de Faturamento --> PlataformaInterna[Sistema de faturamento Faturamento]
```

## 4. Processo de Faturamento

```mermaid
graph TD
    Comprador[Comprador] -- Realiza Pagamentos / Confirma Recebimento --> Sistema((Sistema de faturamento))
    Sistema -- Solicita Pagamentos / Confirma Entrega (via Vendedor) --> Comprador
    Vendedor[Vendedor] -- Informa Conclusão / Envia Produto --> Sistema
    Sistema -- Notifica / Libera Pagamento --> Vendedor
    Sistema -- Interage com --> GatewayPagamento[Gateway Pagamento]
    Sistema -- Inicia Processo de Avaliação --> PlataformaInterna[Sistema de Avaliação]
```

## 5. Processo de Avaliação

```mermaid
graph TD
    Comprador[Comprador] -- Envia Avaliação Preenchida --> Sistema((Sistema de avaliação))
    Sistema -- Solicita Avaliação / Registra Dados --> Comprador
```

## 6. Processo de Cancelamento

```mermaid
graph TD
    Solicitante[Usuario] -- Solicita Cancelamento --> Sistema((Sistema de cancelamento))
    Sistema -- Processa Cancelamento (Notifica, Ajusta Financeiro) --> Solicitante
    Sistema -- Notifica --> OutraParte[Outro usuario da negociação]
    Sistema -- Interage com --> GatewayPagamento[Gateway Pagamento]
```

## 7. Processo de Mudança de Tipo de Conta (Comprador para Vendedor)

```mermaid
graph TD
    Usuario[Comprador] -- Solicita Mudança / Fornece Dados --> Sistema((Sistema de mudança de conta))
    Sistema -- Solicita Dados / Confirma Mudança --> Usuario
```

## 8. Processo de Cadastro de Produto

```mermaid
graph TD
    Vendedor[Vendedor] -- Cadastra Produto (Envia Detalhes) --> Sistema((Sistema de cadastro de produto))
    Sistema -- Confirma Cadastro / Publica Produto --> Vendedor
    Sistema -- Publica Produto --> PlataformaInterna[Catálogo Produtos]
```
