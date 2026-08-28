# Relatório de Avaliação NLU - SAC Móveis Residenciais
## 1. Tabela Comparativa de Métricas (Dados de Teste):

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
