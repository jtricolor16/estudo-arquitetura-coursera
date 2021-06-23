# Controle de Processos

Estilo arquitetural utilizado no controle de sistemas de automação. Neste curso, foram apresentadas duas estratégias: **Feedback Loop** e **Feedforward Control**.

## Feedback Loop

Empregado no acmopanhamento de sistemas em que há a necessidade de executar algum recurso com base nas métricas oferecidas pelo ambiente de uso. Contém 4 componentes básicos: sensor, controlador, atuador e processo. As informações do ambiente são coletadas pelos sensores. Esses dados são encaminhados ao controlador que será incumbido de ativar os atuadores, que são a parte física responsável por manipular os processos (solução lógica do problema).

Para exemplificar o quadro descrito acima, o curso apresenta como caso de uso um sistema de controle de temperatura de uma sala. No qual os sensores são responsáveis por acompanhar se há alguma oscilação significativa que exija um aumento ou não da temperatura; os controladores, após eventos encaminhados pelos sensores ativarão os atuadores que, na camada de processos, definirão a necessidade de regular a temperatura para valores aceitáveis.

## Feedforward Control

Em alguns casos, há a necessidade de que sistemas funcionem em ambientes mais abertos, ou seja, sem regras tão restritas como no caso de controle de temperatura. Para esse tipo de situação, o uso do Feedforward Control é recomendado. Eles são frequentemente utilizados em conjunto com o Feedback Loops. Sua principal diferença está no acréscimo da camada de monitoramento, que não se faz presente no estilo apresentado anteriormente. Por exemplo, ao implementar o feedforward, taxas muito elevadas, que muitas vezes não foram identificadas ao elaborar o feedback loop, podem ser capturadas através da camada de monitoramento, inclusive valores outliers, já que ultrapassam as métricas consideradas normais. 

Um exemplo claro de uso do Feedforward Control é na estrutura MAPE-k usada em alguns carros autônomos. Ela contempla 5 itens: Monitoramento, Análise, Plano, Execução e Conhecimento. Essa estrutura aliada à disponibilidade de dados cada vez maior faz com que veículos deste tipo consigam desenvolver-se cada vez mais. As principais etapas deste fluxo passam por: coletar informações através dos sensores, encaminhar à camada de monitoramento, para ver se não é algo incomum, ir para a de análise, passar pela definição do plano e ação e, enfim, executar o comando necessário via atuadores. Todo esse processo passa pela camada de conhecimento do veículo que está intimamente ligada ao desenvolvimento de técnicas de machine learning e à disponibilidade cada vez maior de dados para uso dessas aplicações.