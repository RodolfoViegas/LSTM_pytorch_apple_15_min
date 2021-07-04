# LSTM_pytorch_apple_15_min
Projeto final para a Disciplina de Redes Neurais


Este projeto visa à implementação de uma rede neural LSTM para a previsão das séries temporais financeiras da empresa Apple. 

Os dados foram obtivos através da biblioteca Pandas Data Reader, que usa a API Alpha Venture para coletar dados em tempo real de dia de pregão. Foram coletetados ao do 6842 obsevações, que correspondem aos dias e horas de 21/062021 04:01:00 a 01/07/2021 20:00:00. Estes dados foram tratados diminuindo a frequência, que originalmente é de minuto a minuto, para 15 minutos. 

Após a modificação da frequência, foram constatados dados em falta. A série foi dividida em dois conjuntos de treino e teste para assim realizar o preenchido com interpolação linear e o valor mais próximo. Além disso, outra parte de pré-processamento foi feita , traformação logaritmica, já que a série história provavelmente é não-estacionária.

Os dados foram tranformados para sequência de "lag" de valor 5, este número foi selecionado por maior de testes.


A rede neural foi finalmente implementada pela API Pytorch, esta bastante popular em meio acadêmico. Sua configuração final ficou com duas camadas LSTM de 70 e 50 células de memória e uma cada MLP de 50 neurônios. 

As métrica para valoração foram de RMSE 0.0615674586857886 e MAE 0.05369377469424135.
