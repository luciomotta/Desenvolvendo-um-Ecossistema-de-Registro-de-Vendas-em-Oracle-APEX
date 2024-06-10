# Desenvolvendo-um-Ecossistema-de-Registro-de-Vendas-em-Oracle-APEX
Este projeto ilustra o desenvolvimento de um ecossistema robusto para o registro e monitoramento de vendas usando Oracle APEX. O sistema é composto por três tabelas principais: SALDOS, VENDAS e HIST_VENDAS, e utiliza gatilhos para automatizar processos de atualização e registro de dados.


Passos Implementados:

1.Criação das Tabelas:

-SALDOS: Armazena informações sobre os produtos, incluindo saldo inicial, saldo final e data da última movimentação.
-VENDAS: Registra cada venda realizada, incluindo detalhes como o produto vendido, quantidade e data da venda.
-HIST_VENDAS: Mantém um registro histórico de todas as vendas realizadas, para fins de auditoria e análise.

2.Criação da Sequência:

-Uma sequência SEQ_VENDAS foi criada para gerar automaticamente o ID das vendas na tabela VENDAS.
-Gatilhos para Atualização Automática:

-TRG_AJUSTA_SALDO: Após cada inserção na tabela VENDAS, este gatilho é acionado para atualizar o saldo final na tabela SALDOS e registrar a venda na tabela HIST_VENDAS.
-TRG_ID_VENDAS: Antes de cada inserção na tabela VENDAS, este gatilho é acionado para atribuir automaticamente o próximo valor da sequência SEQ_VENDAS ao campo ID_VENDAS.

3.Inserção de Dados de Teste:

-Foram inseridos registros de teste na tabela VENDAS para simular vendas de produtos.
-As alterações nos saldos de produtos e o registro das vendas foram automaticamente realizados pelos gatilhos.
4.Resultados:

O ecossistema implementado demonstra a capacidade de automatizar e registrar transações de vendas de forma eficiente e precisa. Com gatilhos bem definidos e uma estrutura de banco de dados adequada, o sistema oferece uma base sólida para o acompanhamento e análise das vendas de produtos.


    SELECT * FROM VENDAS
![image](https://github.com/luciomotta/Desenvolvendo-um-Ecossistema-de-Registro-de-Vendas-em-Oracle-APEX/assets/83682095/6da1bafa-8123-4cfc-82a9-5190b7ad8beb)

    SELECT * FROM saldos
![image](https://github.com/luciomotta/Desenvolvendo-um-Ecossistema-de-Registro-de-Vendas-em-Oracle-APEX/assets/83682095/215d670d-fe05-4a01-84b6-9009270b503e)

    SELECT * FROM HIST_VENDAS
![image](https://github.com/luciomotta/Desenvolvendo-um-Ecossistema-de-Registro-de-Vendas-em-Oracle-APEX/assets/83682095/03c9402b-cc2d-402c-a723-02c92b43247b)


Este projeto no GitHub incluirá o script SQL completo para a criação das tabelas, sequência e gatilhos, juntamente com uma descrição detalhada de cada componente e seu papel no sistema de registro de vendas.
