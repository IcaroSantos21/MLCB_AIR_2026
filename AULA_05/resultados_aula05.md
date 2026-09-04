# Resultados

## Resultado Exercício 1

Frase Original:        Gostaria de saber se vocês estão DEVOLVENDO os valores das mesas compradas!!!       
Frase Limpa & Lemmatizada: gostar saber devolver valor meso comprada

## Resultado Exercício 2

Carregando modelo de Embeddings FastText (Gensim)...
/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))

Primeiras linhas do dataset:
                                            mensagem           intencao
0      Quero devolver este sofa que chegou com rasgo  trocas_devolucoes
1       Gostaria de trocar minha mesa veio arranhada  trocas_devolucoes
2  Como faco para solicitar a devolucao do meu es...  trocas_devolucoes
3             O rack veio com defeito e quero trocar  trocas_devolucoes
4  Preciso devolver a cadeira de escritorio com d...  trocas_devolucoes

Colunas disponíveis:
Index(['mensagem', 'intencao'], dtype='object')

Quantidade de registros: 32

Transformando mensagens em embeddings...
Formato da Matriz de Vetores Densos: (32, 300)

Dados separados:
Treino: (25, 300)
Teste : (7, 300)

Treinando classificador...
Treinamento concluído!

==============================
RESULTADOS
==============================

Acurácia: 42.86%

Classification Report:
                    precision    recall  f1-score   support

logistica_entregas       0.00      0.00      0.00         2
   suporte_tecnico       0.33      1.00      0.50         1
 trocas_devolucoes       1.00      0.50      0.67         2
  vendas_orcamento       0.33      0.50      0.40         2

          accuracy                           0.43         7
         macro avg       0.42      0.50      0.39         7
      weighted avg       0.43      0.43      0.38         7


Matriz de Confusão:
[[0 1 0 1]
 [0 1 0 0]
 [0 0 1 1]
 [0 1 0 1]]

==============================
TESTE DE NOVAS MENSAGENS
==============================

Digite uma mensagem (ou 'sair' para encerrar): Como botar a televisão na parede

Mensagem: Como botar a televisão na parede
Classe prevista: suporte_tecnico
Confiança: 49.08%

Digite uma mensagem (ou 'sair' para encerrar): como chega minha cadeira de presidente

Mensagem: como chega minha cadeira de presidente
Classe prevista: logistica_entregas
Confiança: 42.10%

Digite uma mensagem (ou 'sair' para encerrar): meu armario não veio

Mensagem: meu armario não veio
Classe prevista: logistica_entregas
Confiança: 65.62%

Digite uma mensagem (ou 'sair' para encerrar): saber que dia chega os moves

Mensagem: saber que dia chega os moves
Classe prevista: logistica_entregas
Confiança: 43.94%

## Resultado Exercício 3

/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
/usr/local/lib/python3.13/dist-packages/sklearn/metrics/_classification.py:1565: UndefinedMetricWarning: Precision is ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, f"{metric.capitalize()} is", len(result))
Formato de X_vetores: (32, 300)
Quantidade de classes: 4
Classes: ['trocas_devolucoes' 'logistica_entregas' 'suporte_tecnico'
 'vendas_orcamento']

Dados de treinamento: (25, 300)
Dados de teste: (7, 300)

Modelo treinado com sucesso!

==============================
AVALIAÇÃO DO MODELO
==============================
Acurácia: 42.86%

Relatório de classificação:
                    precision    recall  f1-score   support

logistica_entregas       0.00      0.00      0.00         2
   suporte_tecnico       0.33      1.00      0.50         1
 trocas_devolucoes       1.00      0.50      0.67         2
  vendas_orcamento       0.33      0.50      0.40         2

          accuracy                           0.43         7
         macro avg       0.42      0.50      0.39         7
      weighted avg       0.43      0.43      0.38         7


==============================
TESTES COM FALLBACK
==============================

Frase: 'Quero saber o valor do frete do sofá'
Resultado: FALLBACK_HUMANO
Confiança: 28.69%

Frase: 'Gostaria de ver receitas de bolo de cenoura'
Resultado: FALLBACK_HUMANO
Confiança: 49.17%

==============================
CLASSIFICADOR INTERATIVO
==============================

Digite uma mensagem (ou 'sair' para encerrar): Qual o tempo para minha geladeira?

--------------------------------
Mensagem: Qual o tempo para minha geladeira?
Intenção: FALLBACK_HUMANO
Confiança: 30.28%
--------------------------------

Digite uma mensagem (ou 'sair' para encerrar): Faltou parafuso no meu guardaroupa

--------------------------------
Mensagem: Faltou parafuso no meu guardaroupa
Intenção: FALLBACK_HUMANO
Confiança: 35.50%
--------------------------------

Digite uma mensagem (ou 'sair' para encerrar): Como montar um painel de tv na sala

--------------------------------
Mensagem: Como montar um painel de tv na sala
Intenção: FALLBACK_HUMANO
Confiança: 36.66%
--------------------------------

Digite uma mensagem (ou 'sair' para encerrar): vsfd

--------------------------------
Mensagem: vsfd
Intenção: FALLBACK_HUMANO
Confiança: 30.46%
--------------------------------

Digite uma mensagem (ou 'sair' para encerrar): macacos me mordam 

--------------------------------
Mensagem: macacos me mordam 
Intenção: FALLBACK_HUMANO
Confiança: 35.81%
--------------------------------

Digite uma mensagem (ou 'sair' para encerrar): como montar uma tv na slaa

--------------------------------
Mensagem: como montar uma tv na slaa
Intenção: FALLBACK_HUMANO
Confiança: 49.25%

Digite uma mensagem (ou 'sair' para encerrar): sair
Programa encerrado.
Formato da Matriz de Vetores Densos (Exemplos, Dimensões): (32, 300)


## Resultado Exercício 4

Dataset carregado!

Colunas disponíveis:
['mensagem', 'intencao']

Quantidade de registros: 32

Formato dos embeddings:
(32, 300)

Divisão dos dados:
Treino: (25, 300)
Teste : (7, 300)

Treinando Regressão Logística...
Regressão Logística treinada!

Treinando KNN com K=3...
KNN treinado!

========================================
COMPARAÇÃO DOS MODELOS
========================================
Acurácia - Regressão Logística (Linear): 42.86%
Acurácia - KNN (Distância K=3): 28.57%

========================================
MODELO COM MELHOR DESEMPENHO
========================================
Regressão Logística apresentou a maior acurácia.
Diferença: 14.29%

========================================
COMPARAÇÃO NA BASE COMPLETA
========================================
Regressão Logística: 96.88%
KNN K=3: 56.25%

========================================
TESTES COM NOVAS FRASES
========================================

----------------------------------------
Mensagem: Quero saber o valor do frete do sofá
----------------------------------------
Regressão Logística: vendas_orcamento
KNN (K=3): suporte_tecnico

----------------------------------------
Mensagem: Gostaria de trocar minha mesa
----------------------------------------
Regressão Logística: trocas_devolucoes
KNN (K=3): vendas_orcamento

----------------------------------------
Mensagem: Qual o prazo de entrega do meu pedido?
----------------------------------------
Regressão Logística: vendas_orcamento
KNN (K=3): vendas_orcamento

----------------------------------------
Mensagem: Quero comprar um guarda roupa
----------------------------------------
Regressão Logística: trocas_devolucoes
KNN (K=3): trocas_devolucoes

========================================
CLASSIFICAÇÃO INTERATIVA
========================================

Digite uma mensagem (ou 'sair' para encerrar): como montar tv

----------------------------------------
Mensagem: como montar tv
----------------------------------------
Regressão Logística: logistica_entregas
KNN (K=3): trocas_devolucoes

Digite uma mensagem (ou 'sair' para encerrar): cade minha geladeira?

----------------------------------------
Mensagem: cade minha geladeira?
----------------------------------------
Regressão Logística: logistica_entregas
KNN (K=3): logistica_entregas

Digite uma mensagem (ou 'sair' para encerrar): parafusos perdidos, oq fazer?

----------------------------------------
Mensagem: parafusos perdidos, oq fazer?
----------------------------------------
Regressão Logística: suporte_tecnico
KNN (K=3): logistica_entregas

Digite uma mensagem (ou 'sair' para encerrar): como monta o rack de sala?

## Respostas
O KNN tende a lidar melhor quando as frases semelhantes ficam próximas no espaço vetorial, pois sua classificação depende diretamente dos vizinhos. Porém, com frases muito curtas ou distantes dos exemplos conhecidos, ele pode ter dificuldade. Nesse caso, a Regressão Logística pode ser mais estável.
