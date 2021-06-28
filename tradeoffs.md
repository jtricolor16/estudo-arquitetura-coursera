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
