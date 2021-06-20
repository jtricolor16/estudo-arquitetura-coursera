# Dataflow: Pipe and Filters

Tratar os dados é uma etapa cada vez mais importante no mundo corporativo contemporâneo. Uma forma simples de coletar as informações de um dado sistema e prepará-las para o consumo da equipe de negócios é utilizar a estratégia **pipe and filters**. Nesta abordagem, os pipes funcionam como contectores e os filters como componentes que irão tratar os dados.

Os filters podem atuar como caixa-preta, ou seja, a implementação não precisa ser do conhecimento de quem está utilizando. Além disso, também podem ser componentizados. Recebem um dado, o tratam e retornam o dado refinado. 

O esquema funciona da seguinte forma: há uma origem dos dados, que são intercambiadas através de um pipe, conectando-a ao filter. Um filter também pode se conectar a outro filter através de outros pipes até chegar à conclusão dos dados trabalhados.

As principais vantagens desse tipo de arquitura é a capacidade de reaproveitamento dos filters e também a facilidade de incluir filters e pipes no pipeline.

Como desvantagens, há potenciais problemas de desempenho, já que cada novo filter acrescentado no fluxo demandará mais tempo de execução; a natureza síncrona do processo faz com que alguns filtros demorem a ser executados; por fim, arquiteturas desse tipo não podem ser utilizadas em aplicações que interagem diretamente com o cliente, sendo voltadas para tratativas de dados em bancos de dados analíticos.