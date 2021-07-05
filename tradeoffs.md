# TRADE-OFFS

## Atributos de Qualidade

Um projeto de arquitetura de software não pode ser simplesmente classificado como bom ou ruim. O contexto (requisitos e necessidades) deve ser considerado no momento da escolha do melhor estilo arquitetural. Diferentemente dos padrões de projeto, focados nos requisitos funcionais e nas métricas direcionadas à qualidade do software, a arquitetura do projeto deve englobar também os requisitos não funcionais e atender a stakeholders que vão além dos desenvolvedores. Por exemplo, enquanto o grupo de programadores está preocupado com a capacidade de manutenção do projeto ou com a cobertura de testes, os usuários finais querem que o serviço esteja sempre disponível e sem problemas de usabilidade.

Como não é possível ter uma relação simplesmente maniqueísta com arquitetura de software, opta-se por utilizar os atributos de qualidade para definir se, em dado contexto, as escolhas efetuadas atingem os objetivos almejados por todos os interessados no desenvolvimento do projeto de software. Há alguns pontos importantes a serem considerados na ótica do desenvolvedor:
* Manutenibilidade: Capacidade do sistema receber manutenção;
* Reusabilidade: Reaproveitar componentes na criação/correção de funcionalidades;
* Flexibilidade: Capacidade do sistema se adaptar às mudanças nos requerimentos;
* Modificabilidade: Considera se o sistema pode ter funcionalidades adicionadas ou removidas com o menor custo possível;
* Testabilidade: Verifica se os testes possuem cobertura adequada e se são executados rapidamente;
* Integrigade Conceitual: Preocupa-se com a integridade entre os padrões utilizados no sistema (uso de camelCase, identação etc).

Além dos atributos de qualidade dos desenvolvedores, há também os voltados para atender as necessidades dos usuários. São eles:
* Disponibilidade: Tempo em que o sistema segue em produção sem sofrer qualquer tipo de interrupção, ou seja, estar acessível aos usuários;
* Interoperabilidade: Protocolos de comunicação com clientes ou serviços que necessitem se comunicar com o nosso. Devem ser respeitados os protocolos de comunicação e de interface acordados;
* Segurança: Preocupa-se com o acesso a dados. Somente usuários autorizados devem ter acessos a dados inerentes ao interesse daquela área (definição de acesso com base em perfil);
* Performance: Calcular o tempo de resposta e quantidade de requisições simultâneas suportadas pela aplicação. É importante respeitar os valores acordados nos requisitos utilizando o menor custo possível. Há também a preocupação de a solução ser escalável para o caso de aumento repentino no tráfego;
* Usabilidade: O quão apto o sistema está a fazer com que os usuários consigam usá-lo da maneira adequada e também a suportar as dificuldades que possam vir a ser encontradas por eles.

Cumprir todos os pontos descritos acima é fundamental para definir se um projeto de software está apto a receber melhorias e correções sem muito custo e também sem afetar o seu objetivo de negócio (aspectos funcionais e não funcionais).

É importante salientar que, sempre que for possível, deve-se optar pela solução arquitetural mais simples, considerando os requisitos apresentados.

Outro ponto fundamental é documentar as escolhas e modelos arquiteturais utilizados. Isso fará com que toda a empresa tenha acesso à tomada de decisão e, consequentemente, a companhia não ficará desorientada caso um desenvolvedor ou arquiteto responsável deixe-a.

Aconselha-se que a empresa tenha um guia que possa nortear a definição de arquiteturas para os sistemas que venham a ser desenvolvidos. Alguns dos pontos que devem ser considerados são:
* Valorizar a importância dos atributos de qualidade;
* Envolver o líder técnico nas definições arquiteturais;
* Apresentar o que foi acordado para os diferentes grupos de stakeholders.

Quanto à parte de integridade conceitual, há de se ressaltar:
* O cuidado com a separação de responsabilidades (respeitando os pacotes preestabelecidos);
* Preocupar-se com o reaproveitamento de funções antes de implementar novas (sempre verificar se não há algo que já resolva o problema);
* Deixar claro o conjunto de regras ou requisitos necessários ou usados (memória, largura de banda ou threads).

## Analizando e Avaliando Arquiteturas

Como já apresentado, os atributos de qualiade são métricas importantes para definir e avaliar uma arquitetura de software. No entanto, elas não devem ser utilizadas isoladamente. É fundamental quantificar as métricas na prática. Por isso, utiliza-se dois tipos de cenários de qualidade para avaliar o comportamento arquitetural do sistema: o **geral** e o **específico**.

O primeiro cenário pode ser utilizado para praticamente qualquer sistema. Contempla uma abordagem mais generalista e se preocupa com os problemas comuns a praticamente todos os softwares. Em contrapartida, o segundo foca mais nas especificidades da aplicação analisada. No seu fluxo de execução, há a **origem do estímulo**, ou seja, o que irá gerar um estímulo ou uma solicitação ao sistema; o próprio **estímulo**, que pode ser uma requisição (http, cron, evento) que fomentará o retorno de uma resposta do sistema; o **ambiente** que compreende ao modo como o sistema irá receber o estímulo, como lidará com as falhas e outras situações adversas; o **artefato** que é o componente do sistema afetado pelo estímulo; a **resposta** que nada mais é do que o retorno oferecido por aquele artefato após ser "estimulado" (exceção, logs, alerta de segurança etc); e, por fim, as **medidas de resposta**, que englobam as métricas do sistema que oferecerão insumos para uma análise mais profundada dos resultados. É de suma importância mapear os cenários em que o sistema pode ficar indisponível. Nesse tipo de auditoria, o foco é identificar os pontos fracos da implementação arquitetural.

Veja, abaixo, um exemplo do que foi descrito até o momento para cenários genéricos:

### Origem do estímulo
* Usuário final;
* Sistemas internos;
* Sistemas externos.

### Estímulo
* Preenchimento errado do usuário;
* Exceções por conta de falha de contrato;
* Número elevado de requisições;
* Exceções internas;
* Cargas pesadas.

### Ambiente
* Funcionamento normal;
* Queda;
* Desatifação;
* Recuperação do erro;
* Processamento da requisição.

### Artefato
* Servidor do sistema;
* Processos do sistema.

### Resposta
* Exceções de logs;
* Notificação de usuários;
* Notificações de sistemas externos;
* Redistribuição do processamento de dados;
* Redistribuição das requisições (loadbalancer).

### Medidas de Resposta
* Tempo de reinício;
* Tempo de recuperação;
* Duração da request;
* Tempo para completar um processo;
* Tempo para ativar o processo de recuperação.

Analisando um cenário específico, todo o fluxo seria considerado na execução de um processo. Por exemplo, numa aplicação web, consideraríamos como estímulo de resposta um cliente, como estímulo a requisição deste cliente, como ambiente o local em que o servidor está armazenado (máximo de requisições suportadas), como artefato o servidor web, como resposta o retorno do comportamento do serviço ao cliente (se a solicitação foi atendida ou não) e como medida de resposta a duração do fluxo.

## Architecture Trade-off Analysis Method (ATAM)

É uma abordagem utilizada para permitir que o processo de construção e definição arquitetural possas ser analisado, avaliado e documentado a fim de dar visibilidade a todos os interessados. Para alcançar tais resultados, alguns passos precisam ser respeitados.

Inicialmente, é aconselhável validar bem o processo entre o conjunto de pessoas que detêm informações necessárias para julgar o que foi feito. O primeiro crivo será feito pelos próprios designers da arquitetura, que estão atuando diretamente no projeto. Em seguida, pares com contribuições menores, mas que fazem parte da empreitada, serão chamados a validar o fluxo. Por fim, profissionais que estão fora do contexto do projeto. Essa equipe é classificada como **time de avaliação**. 

O próximo passo é convocar as pessoas que tomam decisões acerca de projetos arquiteturais e de negócios para validarem: **tomadores de decisão do projeto** (tech leads, arquitetos de software, product manager).

Por fim, convocam-se os **interessados na arquitetura**, que de fato é o grupo que fará uso da solução (outros desenvolvedores, usuários, equipe de suporte).

O objetivo de utilizar o ATAM é garantir uma harmonia entre as necessidades de negócio e os requisitos tecnológicos. Devido a esta importante característica, ter um envolvimento amplo e multidisciplinar ajudar a validar se pontos de sensíveis de qualidade são respeitados e, se necessário, definir quais desses itens terão prioridade em relação aos outros.

Para alcançar tais resultados, aconselha-se o uso de nove etapas:
1- Apresentar o ATAM. Contextualizar o time de avaliação sobre os objetivos e expectativas do ATAM.
2- Fazer o mesmo com a equipe de tomada de decisão, focando nos requisitos voltados a essa responsabilidade, sem deixar de passar por uma visão geral dos objetivos do ATAM.
3- Apresentar esse mesmo processo para o grupo dos interessados na arquitetura.
4- Identificar as abordagens arquiteturais através da documentação e das análises construídas até o momento a fim de dar mais visibilidade do que está sendo feito.
5- Definir uma árvore com os atributos de qualidade a fim de tornar ainda mais claros os objetivos da implementação unindo requisitos técnicos (funcionais) e os de negócio (não funcionais) a fim de definir qual o grau de exigência será necessário dispor em cada um deles. Essa classificação pode ser feita considerando letras (H - high, M - Medium, L - Low).
6- Analisar os enfoques da arquitetura a fim de compreender os pontos sensíveis e o que deve ser priorizado, a fim de deixar claro, e documentado, o que foi identificado nesse passo e o que deve ser priorizado.
7- Realizar uma sessão de brainstorm entre os envolvidos a fim de definir os cenários de qualidade para a definição de prioridades. Neste momento, deve-se atentar para o fato de que diferentes fluxos podem ser identificados. Se isso ocorrer, significa que a arquitetura não está sendo apresentada aos verdadeiros interessados no projeto, já que falta foco na priorização.
8- Redesenhar a árvore com os atributos de qualidade, agora orientados ao fluxo e já considerando o mapeamento dos riscos e objetivos feitos após a apresentação do primeiro esquema.
9- Por fim, chega-se a etapa de apresentação dos resultados, contando com as priorizações, riscos, pontos sensíveis, e demais itens que ajudem a identificar os cenários de sucesso e de atenção.

O uso do ATAM tem valor para tornar o processo de construção arquitetural evolutivo e perene, além de dar maior garantia de que os pontos levantados foram analisados pelos principais interessados o que, dessa forma, reduz significativamente a chance de haver um desacordo entre o combinado e o projetado.
