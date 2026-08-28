# Relatório de Avaliação NLU - SAC Móveis Residenciais

## Participantes:

nome: Icaro Rodrigues Santos RA: 137061
nome: Rafael Matos Celestino RA: 136771
nome: Adrián Páris Guerrero Vieira RA: 137807 

## 1. Tabela Comparativa de Métricas (Dados de Teste):
### LAB 01

                    precision    recall  f1-score   support

logistica_entregas       1.00      1.00      1.00         6
       reclamacoes       1.00      1.00      1.00         6
           suporte       1.00      1.00      1.00         6
 trocas_devolucoes       1.00      1.00      1.00         6
            vendas       1.00      1.00      1.00         6

          accuracy                           1.00        30
         macro avg       1.00      1.00      1.00        30
      weighted avg       1.00      1.00      1.00        30

[[6 0 0 0 0]
 [0 6 0 0 0]
 [0 0 6 0 0]
 [0 0 0 6 0]
 [0 0 0 0 6]]

 
### LAB 02
                    precision    recall  f1-score   support

logistica_entregas       0.80      0.67      0.73         6
       reclamacoes       1.00      0.33      0.50         6
           suporte       1.00      1.00      1.00         6
 trocas_devolucoes       0.62      0.83      0.71         6
            vendas       0.67      1.00      0.80         6

          accuracy                           0.77        30
         macro avg       0.82      0.77      0.75        30
      weighted avg       0.82      0.77      0.75        30


## 2. Análise dos Testes de Entrada (`input()`)
- **Comportamento do KNN (10 testes):** [Como o KNN reagiu às variações das frases digitadas e ao fallback?]

=== INICIANDO BATERIA DE TESTES (10 INPUTS OBRIGATÓRIOS) ===

[Teste 1/10]
Digite a frase do cliente: como faco para adquirir móvel

Bot [Intenção: VENDAS | Confiança: 100.0%]: Temos a opção de moveis de cozinha, Sala de jantar e Banheiro. Qual deseja?

[Teste 2/10]
Digite a frase do cliente: Quero registrar uma reclamação

Bot [Intenção: RECLAMACOES | Confiança: 100.0%]: Temos Reclamações, Problemas com a entrega, Defeito no movel. Qual deseja?

[Teste 3/10]
Digite a frase do cliente: onde está a minha entrega

Bot [Intenção: RECLAMACOES | Confiança: 100.0%]: Temos Reclamações, Problemas com a entrega, Defeito no movel. Qual deseja?

[Teste 4/10]
Digite a frase do cliente: onde está a minha entrega?

Bot [Intenção: RECLAMACOES | Confiança: 100.0%]: Temos Reclamações, Problemas com a entrega, Defeito no movel. Qual deseja?

[Teste 5/10]
Digite a frase do cliente: Onde está o meu pedido?

Bot [Intenção: LOGISTICA_ENTREGAS | Confiança: 100.0%]: Temos Logistica e Entregas. Qual deseja?

[Teste 6/10]
Digite a frase do cliente: Quero fazer uma devolução

Bot [Intenção: RECLAMACOES | Confiança: 100.0%]: Temos Reclamações, Problemas com a entrega, Defeito no movel. Qual deseja?

[Teste 7/10]
Digite a frase do cliente: quero devolver a entrega

Bot [Intenção: TROCAS_DEVOLUCOES | Confiança: 66.7%]: Temos a opção de Troca ou Devolução. Qual deseja?

[Teste 8/10]
Digite a frase do cliente: status da entrega

Bot [Intenção: LOGISTICA_ENTREGAS | Confiança: 100.0%]: Temos Logistica e Entregas. Qual deseja?

[Teste 9/10]
Digite a frase do cliente: Geladeira

Bot: [FALLBACK - Confiança baixa: 33.3%]
Desculpe, não consegui entender sua solicitação. Por favor, aguarde um momento enquanto encaminho você para um atendente humano...

[Teste 10/10]
Digite a frase do cliente: Quero comprar um fogão

Bot [Intenção: VENDAS | Confiança: 66.7%]: Temos a opção de moveis de cozinha, Sala de jantar e Banheiro. Qual deseja?

- **Comportamento da Decision Tree (8 testes):** [Como a Árvore de Decisão se comportou em comparação ao KNN?]:

===== INICIANDO O CHATBOT =======


[Teste 1/8]
Digite a frase para interação: Quero uma cartinha de pokemon

 INTENÇÃO: reclamacoes
 CONFIANÇA: 100.0%
Temos reclamações, Problemas com o envio e Defeitos no móvel. Qual deseja?

[Teste 2/8]
Digite a frase para interação:  quero a geladeira

 INTENÇÃO: vendas
 CONFIANÇA: 100.0%
Temos opção de todos os tipos de moveis! Qual o(a) senhor(a) deseja?

[Teste 3/8]
Digite a frase para interação: Quero abrir uma reclamação

 INTENÇÃO: reclamacoes
 CONFIANÇA: 100.0%
Temos reclamações, Problemas com o envio e Defeitos no móvel. Qual deseja?

[Teste 4/8]
Digite a frase para interação: preciso de um suporte

 INTENÇÃO: vendas
 CONFIANÇA: 100.0%
Temos opção de todos os tipos de moveis! Qual o(a) senhor(a) deseja?

[Teste 5/8]
Digite a frase para interação: Quero devolver um sofá

 INTENÇÃO: vendas
 CONFIANÇA: 100.0%
Temos opção de todos os tipos de moveis! Qual o(a) senhor(a) deseja?

[Teste 6/8]
Digite a frase para interação: Status do meu pedido

 INTENÇÃO: logistica_entregas
 CONFIANÇA: 100.0%
Temos Logistica e Entregas. Qual deseja?

[Teste 7/8]
Digite a frase para interação: Status da entrega

 INTENÇÃO: trocas_devolucoes
 CONFIANÇA: 100.0%
Temos opções de trocas e devoluções. Qual deseja?

[Teste 8/8]
Digite a frase para interação: Quero trocar meu guarda-roupa

 INTENÇÃO: logistica_entregas
 CONFIANÇA: 100.0%
Temos Logistica e Entregas. Qual deseja?
