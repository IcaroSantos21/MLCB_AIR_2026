# LAB 01
--- RESULTADOS DO LAB 01 (AULA 03) ---
Mensagem: 'Preciso urgente da segunda via da fatura'
Intenção Predita: [segunda_via]
Vocabulário Filtrado (sem stopwords): ['2a', '2a via', 'aberto', 'acordo', 'acordo pagar', 'alterar', 'alterar endereço', 'app', 'atrasada', 'atualizo', 'atualizo dados', 'boleto', 'cadastramento', 'dados', 'dados residenciais', 'débito', 'débito aberto', 'dívida', 'emitir', 'emitir segunda', 'endereço', 'endereço cadastramento', 'fatura', 'fatura atrasada', 'fazer', 'fazer um', 'gostaria', 'gostaria alterar', 'negociar', 'negociar pagamento', 'no', 'no app', 'onde', 'onde atualizo', 'pagamento', 'pagamento dívida', 'pagar', 'pagar débito', 'posso', 'posso emitir', 'residenciais', 'residenciais no', 'segunda', 'segunda via', 'um', 'um acordo', 'via', 'via boleto', 'via fatura']

#========== PRODUÇÃO DO RELATÓRIO:==============
### 1 - Qual o impacto da remoção de stopwords no tamanho do vocabulário do modelo?
Ele torna o processo mais pesado, pois acaba lendo/consumindo palavras não necessarias
### 2 - O que significa a configuração ngram_range=(1, 2) no TfidfVectorizer?
A primeira função faz com que o TfidVectorizer leia sempre uma dupla de palavras. E assim realiza o filtro com base na quantidade de vezes que aquela dupla de palavras aparece.
### 3 - Como a remoção de palavras genéricas ajuda a evitar classificações incorretas?
Caso não ocorra a remoção das palavras genéricas, o modelo fica mais impreciso, aumenta a chance de alucinação, e deixa o algoritmo sobrecarregado!
### Todos os resultados devem ser inseridos no arquivo resultados_aula03.md
#========== FIM ==============

# LAB 02

--- RESULTADOS DO LAB 02 (AULA 03) ---

--- Relatório de Classificação ---
                     precision    recall  f1-score   support

horario_atendimento       0.50      1.00      0.67         1
        localizacao       0.00      0.00      0.00         1
    troca_devolucao       0.00      0.00      0.00         1

           accuracy                           0.33         3
          macro avg       0.17      0.33      0.22         3
       weighted avg       0.17      0.33      0.22         3

--- Matriz de Confusão ---
[[1 0 0]
 [1 0 0]
 [0 1 0]]

 #========== PRODUÇÃO DO RELATÓRIO:==============
### 1 - O que representam as métricas Precision, Recall e F1-Score no relatório?
Precision mede a taxa de acerto com base na resposta do bot, o recall mede a quantidade de retornos assertivos do bot, f1-score realiza a média do precision e recall.
### 2 - Como interpretar a diagonal principal da Matriz de Confusão?
A diagonal está incorreta, pois à partir do coluna "localização" o que era para ser da linha "localização", vai para a linha "horário_atendimento" e o mesmo se repete com a coluna "troca_devolução", que a linha correta seria "troca_devolução" e está mandando para "localização"
### 3 - Por que a acurácia isolada pode ser enganosa quando temos classes desbalanceadas?
Pois por mais que ele seja eficiente para uma classe, para as outras pode acabar sendo completamente ineficiente.
### Todos os resultados devem ser inseridos no arquivo resultados_aula03.md
#========== FIM ==============

# LAB 03:
#========== PRODUÇÃO DO RELATÓRIO:==============
### 1 - Cole o código corrigido e a acurácia obtida:
```python
dados_rh = {
    'mensagem': [
        'Como solicitar minhas ferias?', 'Quero agendar meu periodo de ferias',
        'Onde baixo meu holerite do mes?', 'Preciso do comprovante de rendimentos',
        'Como cadastrar meu atestado medico?', 'Onde envio o atestado de consulta?', 'Gostaria de tirar férias no próximo mês',
        'Como posso solicitar minhas férias pelo sistema?',
        'Quero verificar quantos dias de férias tenho',
        'Onde posso consultar meu holerite?',
        'Preciso acessar meu contracheque',
        'Como faço para baixar meu holerite?',
        'Tenho um atestado médico, onde devo enviar?',
        'Preciso registrar um atestado no sistema',
        'Como envio um atestado para o RH?',
        'Onde cadastro meu documento de atestado?'
    ],
    'intencao': [
        'solicitar_ferias', 'solicitar_ferias',
        'obter_holerite', 'obter_holerite',
        'enviar_atestado', 'enviar_atestado', 'solicitar_ferias',
        'solicitar_ferias',
        'solicitar_ferias',
        'obter_holerite',
        'obter_holerite',
        'obter_holerite',
        'enviar_atestado',
        'enviar_atestado',
        'enviar_atestado',
        'enviar_atestado'
    ]
}
```
Acuracia via Pipeline: 83.33%
### 2 - Qual é a grande vantagem de utilizar o objeto Pipeline no Scikit-Learn?
O Scikit-Learn automatiza o processo de pipeline, garantindo um código limpo.
### 3 - Por que o Pipeline evita que erros de pré-processamento ocorram entre treino e teste?
Porque ele evita que dados sejam vazados, você passa o texto puro, e recebe a intenção final.
### Todos os resultados devem ser inseridos no arquivo resultados_aula03.md
#========== FIM ==============
