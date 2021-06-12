# Diagramas UML

## Diagramas de componentes
Representa a comunicação entre os componentes do serviço. Conector em forma de bola representa que aquele componente tem uma interface para se comunicar com outros clientes ou compontentes. Um conector em forma de socket indica que aquele componente necessita se conectar a outro para o funcionamento adequado.

## Diagramas de pacotes
Utilizados para representar a interação, comunicação, depedências, encapsulamento, e itens presentes em cada pacote. Ver exemplos no material do curso. Em sua representação, o nome do pacote deverá vir no meio da pasta se estiver vazio e no topo dela caso haja algum elemento. Há a possibilidade de acrescentar o tipo de componente no meio da pasta ou do lado de fora, integrando através de composição. + representa acesso público e - privado.

## Diagrama de Deploy
Utilizado para especificar os artefatos necessários, em orderm, para rodar a aplicação deployada. Ver exemplo no material do curso. Há dois tipos deste diagrama:
- o de nível de especificação: Mais genralista. Não entra no detalhe dos dispositivos. Focado nos artefatos
- o de instância de níveis: Mais específico. Entra no detalhe das máquinas em que haverá o deploy. Auxilia nos processos de build em diferentes ambientes (dev, stg e prod). Os devices são representados em nós. Cada artefato desenhado dentro desses nós significa que ele só será necessário a rodar naquele tipo de dispositivo. O principal objetivo do diagrama de deploy é dar mais consistência às publicações dos sistemas.

## Diagrama de atividades
Utilizado para mapear as ações possíveis dentro do sistema e os fluxos encadeados por cada uma delas. É importante ter bem definidas as ações e quais os fluxos permitidos. O início deste diagrama é feito através de um cículo comum e o seu final tb é seguido por um círculo, mas com espessura mais grossa. Os fluxos são representados por diagramas de decisão e as ações são exibidas dentro de representações ovais. Ver o exemplo no material do curso. Para fluxos que funcionem paralelamente, utilizam-se raias, como na natação, para ilustrar o processo. 

