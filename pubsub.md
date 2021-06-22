# Pubsub

Apesar de conceitualmente ser bem semelhante à orientada a eventos, a do tipo **publish-subscribe** tem uma diferença fundamental: um componente do tipo publish sempre publicará o evento e o do tipo consumer sempre receberá esse evento. Ou seja, não é possível que um único componente desempenhe os dois papéis. No entanto, bem como a orientada a eventos, também possui um baxíssimo acoplamento entre as funcionalidades.

O pubsub funciona da seguinte maneira: um componente do tipo publisher irpá conter um conjunto de consumers que desejam ouvir/receber suas mensagens. Assim que uma informação é publicada no publish, automaticamente todos os seus consumers serão invocados. Esse tipo de link entre publish e subscribe pode ser feito através de protocolos de internet ou até mesmo usando o event bus, como ocorre na orientada a eventos. Caso esta seja a opção a similaridade entre os dois estilos de arquitetura de software serão ainda mais acentuadas.

Alguns exemplos de implementações que usam pusub são: RSS feeds, listas de e-mails que desejam receber alguma newsletter e listas de usupários que desejam receber push notifications.