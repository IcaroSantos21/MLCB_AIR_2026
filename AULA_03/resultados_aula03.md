# LAB 01
--- RESULTADOS DO LAB 01 (AULA 03) ---
Mensagem: 'Preciso urgente da segunda via da fatura'
Intenção Predita: [segunda_via]
Vocabulário Filtrado (sem stopwords): ['2a', '2a via', 'aberto', 'acordo', 'acordo pagar', 'alterar', 'alterar endereço', 'app', 'atrasada', 'atualizo', 'atualizo dados', 'boleto', 'cadastramento', 'dados', 'dados residenciais', 'débito', 'débito aberto', 'dívida', 'emitir', 'emitir segunda', 'endereço', 'endereço cadastramento', 'fatura', 'fatura atrasada', 'fazer', 'fazer um', 'gostaria', 'gostaria alterar', 'negociar', 'negociar pagamento', 'no', 'no app', 'onde', 'onde atualizo', 'pagamento', 'pagamento dívida', 'pagar', 'pagar débito', 'posso', 'posso emitir', 'residenciais', 'residenciais no', 'segunda', 'segunda via', 'um', 'um acordo', 'via', 'via boleto', 'via fatura']

#========== PRODUÇÃO DO RELATÓRIO:==============
# 1 - Qual o impacto da remoção de stopwords no tamanho do vocabulário do modelo?
# Ele torna o processo mais pesado, pois acaba lendo/consumindo palavras não necessarias
# 2 - O que significa a configuração ngram_range=(1, 2) no TfidfVectorizer?
# A primeira função faz com que o TfidVectorizer leia sempre uma dupla de palavras. E assim realiza o filtro com base na quantidade de vezes que aquela dupla de palavras aparece.
# 3 - Como a remoção de palavras genéricas ajuda a evitar classificações incorretas?
# Caso não ocorra a remoção das palavras genéricas, o modelo fica mais impreciso, aumenta a chance de alucinação, e deixa o algoritmo sobrecarregado!
# Todos os resultados devem ser inseridos no arquivo resultados_aula03.md
#========== FIM ==============
