# SAP B1 - Queries de Pedidos → Produção → Faturamento

Esse repositório tem uma query SQL que eu criei no SAP Business One pra cruzar pedidos de venda com ordens de produção e ver o que já foi faturado.

Tudo aqui está anonimizado: nomes de tabelas fictícios, nada de dados reais de cliente, empresa ou valores.

### O que tem aqui
- Uma query principal que mostra:
  - Pedido (número, data, cliente)
  - Quantidade pedida vs faturada (com formatação BR: vírgula decimal, unidade kg/m/PC)
  - Ordem de produção 
  - Status da OP (Planejada, Liberada, Fechada, Cancelada)
  - Se tem fatura ou não + valor total faturado da linha do pedido de venda

É bem útil pra acompanhar produção ou identificar pedidos que ainda não foram faturados.

### Como usar
1. Abra o Query Manager no SAP B1
2. Cole o código do arquivo `.sql`
3. Troque os nomes fictícios pelas tabelas reais do seu ambiente:
   - SalesOrders → ORDR
   - SalesOrderLines → RDR1
   - Items → OITM
   - ProductionOrders → OWOR
   - InvoiceLines → INV1
4. Execute com os parâmetros:
   - [%0] = código do cliente
   - [%1] = data inicial
   - [%2] = data final


Se você adaptar e melhorar, manda um pull request ou me avisa que atualizo aqui.

Qualquer dúvida ou sugestão, abre uma issue ou manda mensagem.

Abraços
at. Mateus Varola
