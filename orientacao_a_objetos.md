# Orientação a Objetos

A escolha da linguagem e do estilo de programação a serem utilizados impactam diretamente nas definições arquiteturais. Ao optar por Java, C++ ou qualquer outra linguagem que possibilite o uso de POO, deve-se atentar aos padrões e conceitos ligados à POO na elaboração de uma arquitetura eficiente e escalável.

## Princípios da Programação Orientada a Objetos
- Abstração: Simplificar um conceito. Ou seja, capacidade de representar no seu projeto um cenário preestabelecido da melhor forma.
- Encapsulamento: Controlar o acesso a funções e classes de acordo com as necessidades previstas nas interfaces dos objetos.
- Generalização: Capacidade de tornar funcionalidades e recursos comuns reaproveitáveis;
- Decomposição: Dividir para conquistar.

## Padrões de Projeto POO
Há 3 grandes grupos de padrões de projetos para POO:
- Criacionais: Lidam com a criação dos objetos (Singleton, por exemplo).
- Estruturais: Compreendem aos padrões incumbidos de criarem elos entre classes e subclasses (Proxy, por exemplo)
- Comportamentais: Preocupa-se em como um objeto funciona individualmente ou acoplado a um conjunto de outros componentes (Observer, por exemplo).

## Tipos de dados abstratos e POO
A Orientação Ojbeto é uma abordagem orientada a dados, ou seja, as primeiras definições levam em consideração as classes que irão refletir os componentes a serem representados na base de dados. Os bojetos nada mais são do que instâncias das classes definidas, respeitando todas as diretrizes e regras estabelecidas nestas. A ligação entre as classes e o comportamento dos objetos é que irão definir a arquitetura a ser representado numa arquitetura orientada a objetos.

Por exemplo, um sistema de placar poderia conter classes como jogo, equipes, (gol, ponto ou qualquer indicador de mudança no placar). Nesse processo, um jogo iria conter equipes e valores de pontuação para cada equipe. Esses valores poderiam ser alterados no decorrer da partida.