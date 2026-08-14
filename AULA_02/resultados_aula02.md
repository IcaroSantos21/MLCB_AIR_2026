# LAB 01

--- RESULTADOS DO LAB 01 ---
Mensagem: 'Quero consultar quanto dinheiro tenho' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Pode me ajudar a fazer um pix?' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Gostaria de cancelar meu cartão de crédito' ==> Intenção Predita: [cancelar_conta]

1 - Avaliem os resultados e verifiquem se os resultados foram corretos ou incorretos. Coloque a resposta no arquivo do relatório do laboratório:
Mensagem: 'Quero consultar quanto dinheiro tenho' ==> Intenção Predita: [fazer_pix] -> INCORRETO
Mensagem: 'Pode me ajudar a fazer um pix?' ==> Intenção Predita: [fazer_pix] -> CORRETO
Mensagem: 'Gostaria de cancelar meu cartão de crédito' ==> Intenção Predita: [cancelar_conta] -> CORRETO

2 - Detectado algum erro, qual seria a maneira mais correta de melhorar o resultado do algoritmo?
A Maneira mais correta seria utilizar a mensagem com o resultado incorreto como base para aprimorar nosso dataframe, adicionando uma mensagem de exemplo com palavras-chaves semelhantes às da mensagem com resultado incorreto, e associar ao novo rótulo adequado.

3 - Detalhe a função do LogisticRegression no algorítmo.
O LogisticRegression funciona da seguinte forma, com base no nosso dataframe, ele calcula a probabilidade de uma mensagem nova ser associada à algum rótulo, ele utiliza os nossos treinos e testes para aprimorar esta classificação!
