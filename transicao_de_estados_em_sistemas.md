# Transição de estados em sistemas (State Transition Systems)

O uso deste tipo de abordagem é de suma importância nas aplicações contemporâneas, nas quais há computação distribuída, multiprocessamento (mais de um núcleo no processo de processamento) ou multithreading (mais de uma threading do SO). Neste tipo de implementação, há 3 pontos a serem destacados:
* state (estado): Uma aplicação pode conter diferentes tipos de estado (rodando, executado, etc). Eles podem ser alterados e gerarem consequências na execução do sistema;
* transition (transição): Etapa responsável por alterar o estado da aplicação. Um único sistema pode ter muitas transições, já que costumam conter mais de um estado. Isso pode gerar a comportamentos não determinísticos, no momento em que não conseguimos precisar qual será o próximo estado do sistema.
* behaviour (comportamento): A mudança de estados gerará uma consequência na aplicação, ou seja, um coportamento será acionado.

Há dois tipos de sistemas de transições de estado o categorizado(labelled) e o não categorizado(unlabelled). O primeiro engloba um conjunto de transições de estado (p ⭇ q). Enquando o segundo possui apenas um conjunto de estados (p → q).

Em suma, transição de estados em sistemas otimiza a execução dos serviços a partir do momento em que consegue geranciar os recursos de um SO, por exemplo, através de priorização com base nos estados dos processos.