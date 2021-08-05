# PWM_8051

Algoritmo para controle de velocidade de motores elétricos de corrente contínua (DC) com base em uma comunicação serial, desenvolvido em linguagem Assembly para microprocessadores da arquitetura 8051. Para efetuar o controle da velocidade, o motor elétrico deve estar conectado a uma chave (podem ser transistores de junção bipolar (TBJ), MOSFETs ou IGBTs, por exemplo). A porta que efetua o chaveamento do motor é a P2.0. 

O algoritmo utiliza modulação por largura de pulso (pwm) para variar a tensão média (e a potência) entregue à carga, com base na entrada recebida pela porta serial. Caso, por exemplo, seja necessária uma velocidade igual à metade da velocidade nominal do motor, a porta P2.0 emitirá um sinal de onda quadrada com 50% do período em nível lógico alto e 50% em nível lógico baixo. Dessa forma, a potência média entregue ao motor será aproximadamente a metade de sua potência nominal e a velocidade angular de seu eixo também será a metade da nominal.

São usados os dois temporizadores do 8051, e a frequência deve estar fixa em 11.049 kHz.
