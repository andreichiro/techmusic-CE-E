Equipamentos utilizados:

Arduino uno, cabos, 6 push buttons, breadboard;

Montagem  do hardware:

Os push buttons são botões que completam o circuito quando o botão é pressionado. É necessário conectar o lado esquerdo superior de cada push button com a voltagem LOW, localizada na parte superior da breadboard.

Depois disso, basta conectar o lado superior direito de cada push button com um pino digital correspondente.

Funcionamento do hardware:

Ao acionar um botão, será ativada a voltagem low. Isso significa que será necessário implementar um input pullup, identificando o low como o botão pressionado, com a vantagem de protegermos o circuito de receber uma carga high sem um resistor, já que o pullup nos permite utilizar os resistores do arduino; nesse circuito, não há outras peças para proteger, mas a estrutura do projeto conta com possíveis boas práticas para iniciantes em arduino. 

Utilizando uma lista, podemos preencher todos os pinos digitais e facilitamos nosso código, tornando-o mais modular e didático. Assim, construiremos uma condicional que verifica e compara os dois estados possíveis de cada botão, ou seja, high ou low, identificando o low com um botão pressionado, desde que esse esteja especificado em nossa lista. Além disso, essa variável nos ajuda a determinar um estado inicial, evitando o algoritmo de certa forma aleatorio de estado inicial.

Essa condicional estará dentro de um comando for, usando a variável de nossa lista com um digitalRead que também utilizará essa mesma variável; é por isso - pensando nesse código - que montamos o circuito apenas com push buttons conectados com pinos digitais especificados como input pullups, e fios conectados ao ground.  

Apesar da simplicidade do circuito, é possível considerar que sua estrutura foi refletida previamente, tentando traduzir uma estrutura de código para um circuito funcional e que transforma os envios dos botões, captados no digitalRead, em NoteOns que especificam a nota, velocity e canal midi correspondente, onde utilizamos uma escala cromática - 36, 37, 38, 39, 40, 41. 

No entanto, o código permite que se personalize a escala, adicionando uma informação byte com o cc mais baixo a ser utilizado.

É possível visualizar o vídeo do arduino funcionando, bem como o circuito no Tinkercad.
