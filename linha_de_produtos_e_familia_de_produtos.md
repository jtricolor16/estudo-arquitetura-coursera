# Linha de Produtos e Família de Produtos

Conceitualmente, ambas têm a mesma definição: desenvolvimento de sistemas pensando em reutilização de código através de uma arquitetura modular. Este tipo de estratégia é aconselhável quando o projeto é pensado para ter mais de um produto ou aplicação que compartilhará algumas características. Ao utilizar essa abordagem, os times envolvidos terão mais agilidade nas entregas, na medida em que boa parte dos componentes será reaproveitada; as interfaces com clientes ou experiência do usuário também tende a se beneficiar, já que o fluxo tende a ser o mesmo entre os produtos e o custo de desenvolvimento será reduzido.

Ao desenvolver linhas de produtos, é importante deixar bem segmentado os 3 tipos de componentes que tendem a fazer parte deste processo: os **comuns**, ou seja, aqueles que serão compartilhados entre os produtos. As **variações** que são aquelas que terão de passar por algum tipo de modificação para atender uma especificidade daquele produto (no caso do iPhone e do iPad, por exemplo, poderia ser o cuidado com componentes de renderização de layout no segundo, por ter uma tela maior). Por fim, os **exclusivos**, voltados para atender as necessidades únicas do produto em questão (voltando ao exemplo da Apple, seria a necessidade do iPhone realizar ligações).

Na construção dos times, aconselha-se o uso de duas equipes: a de **domínio de engenharia** e a de **engenharia de aplicação**. O primeiro cuida da parte de estabelecimento dos componentes comuns e de variação. Preocupa-se com questões macro da linha de produto. Foca na construção de uma arquitetura modular que atenda a todos os produtos. Testa todo o fluxo de integração. Já o segundo atua na implementação das estruturas criadas pelo primeiro time nos seus aplicativos. Podem ser definidos como instanciadores de componentes, como ocorre com a relação classes e objetos na programação OO. Eles também cuidam da criação e implementação de componentes exclusivos para a aplicação e de todo o fluxo de teste no sistema em que trabalham.

## Arquitetura de referência

Fundamental quando se pensa em linha de produtos. A capacidade modular da arquitetura elaborada é que dará tração ao processo de acoplamento de novas funcionalidades aos produtos. Há 3 técnicas que podem ser utilizadas nesse processo:

### Técnica de adaptação

### Técnica de substituição

### Técnica de extensão