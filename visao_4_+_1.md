# Visão 4 + 1

## Visão lógica
Compreende a parte responsável pelos modelos do sistema, ou seja, as classes. Aconselha-se a representação uml utilizando diagramas de classe ou de estado. Compreende a requisitos funcionais e muitas vezes pode ser elaborada juntamente à visão de desenvolvimento, que será apresentada mais à frente.

## Visão de processos
Responsável por cobrir a parte dos requisitos não funcionais. Mapeia o comportamento do sistema. Pode ser representado pelo diagrama de sequência. Por exemplo, num sistema de registro de resultados de uma partida de futebol, seria a parte em que teríamos de acrescentar um Gol para o time A, indicar que o jogador C levou um cartão amarelo, acompanhar a duração da partida etc.

## Visão de desenvolvimento
É a que de fato será a responsável por implementar o sistema. Engloba a linguagem de programação, bibliotecas utilizadas, documentação do processo. Como o nome sugere, irá conter os detalhes do fluxo de desenvolvimento e o seu gerenciamento.

## Visão física
Representa a parte física do sistema (qual banco de dados usar, a aplicação ficará na nuvem ou num servidor físico local etc). Pode ser representada pelo diagrama de deployment.

## Cenários
Descrições que auxiliarão no processo de validação das 4 visões descritas anteriormente. Descrevem uma sequência de ações que terão de ser executadas para garantir que o fluxo funciona adequadamente. Por exemplo:
1. Time A fez um gol;
2. Operador do sistema deve incluir um gol para a equipe autora do tento;
3. Ao fazer isso, o sistema salvará o gol no banco de dados Z;
4. O sistema irá exibir um gol a mais para a equipe A no placar.