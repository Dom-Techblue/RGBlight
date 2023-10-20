## RGBlight
#OBJETIVO DO TRABALHO

Desenvolver uma lâmpada de ambiente com efeito "mood" usando três LEDs, um vermelho, um verde e um azul. Neste projeto, a combinação das cores dos LEDs será responsável por criar as cores do arco-íris.

Observação: Uma lâmpada de ambiente "mood" é uma solução estética destinada a iluminar o ambiente com o propósito de refletir e definir a atmosfera (mood) do espaço, em vez de servir como a principal fonte de iluminação.

#APLICAÇÃO

Com o intuito didático, abordaremos o estudo do PWM (Modulação por Largura de Pulso), os valores RGB (Vermelho, Verde e Azul) e suas aplicações em efeitos com LEDs.

O PWM é uma técnica que modula a largura dos pulsos de um sinal elétrico para controlar a intensidade luminosa ou a velocidade de motores, por exemplo. No contexto dos LEDs RGB, o PWM é usado para ajustar a intensidade de cada cor (vermelho, verde e azul), permitindo a criação de diversas cores e tons.

Os LEDs RGB são componentes que emitem luz nas cores vermelha, verde e azul. Combinando essas cores em proporções diferentes, podemos obter uma ampla gama de cores, incluindo todas as cores do espectro visível.

As aplicações práticas desses conceitos incluem a criação de efeitos de iluminação coloridos. Por exemplo, ao ajustar o PWM em um LED RGB, você pode criar efeitos como transições suaves de cor, cores pulsantes e até mesmo simular a iluminação de um "mood lamp" mencionado anteriormente. Isso é comumente usado em projetos de iluminação de ambientes, sinalização colorida, efeitos visuais em espetáculos, entre outros.

O estudo desses conceitos é fundamental para entender como os dispositivos eletrônicos podem controlar e personalizar a cor e a intensidade da luz em uma ampla variedade de aplicações, tornando-os valiosos tanto para fins didáticos quanto para a criação de projetos criativos de iluminação.

#COMPONENTES USADOS
| COMPONENTES | QUANTIDADE | OBSERVAÇÃO|
| :---         |     :---:      |          ---: |
| LED 5mm  | 3  | vermelho, verde, azul   |
| Protoboard   | 1      | 400 pontos   |
| Resistor   | 3    | 1 resistor de 200Ω e 2 de 100Ω   |
| Arduino UNO    | 1       | -----------  |

#COMO FUNCIONA
1- Após iniciar o programa, a mistura das cores dos 3 LEDs (vermelho, verde e azul) gera as cores do arco-íris que vão se alterando lentamente e de forma aleatória.
2- Essa combinação de cores é alcançada ao regular a luminosidade de cada um dos três LEDs usando a técnica de PWM (Modulação por Largura de Pulso), o que resulta em diferentes valores RGB, ou seja, cores distintas. Esse efeito opera de maneira semelhante à composição de um monitor de computador, que é composto por minúsculos pontos vermelhos, verdes e azuis.
3-Difundindo a luz usando um cilindro de papel (folha A4), é possível criar uma agradável mistura de cores. Os LEDs podem ser inseridos em qualquer objeto com capacidade de difusão de luz, ou então é possível refletir a luz usando um material difusor reflexivo. Um  exemplo interessante é posicionar as luzes no interior de uma pequena garrafa de plástico (de preferência, com plástico mais fino), para obter melhores resultados.

Um valor RGB de (255,0,0) representa vermelho puro, (0,255,0) é verde puro e (0,0,255) indica azul puro. Combinando esses valores, é possível criar uma ampla variedade de cores. Mesmo ao alternar simplesmente os LED's entre ligado e desligado, sem ajustar a intensidade luminosa, é possível obter cores diversas.
Ao controlar a luminosidade usando PWM, é possível criar uma variedade ainda mais ampla de cores. Posicionando os LED's próximos uns dos outros e mesclando seus valores, por exemplo, através de um cilíndro de papel, o espectro de luz gerado pelas três cores combinadas resulta em uma cor única. o número toal de cores disponíveis, utilizando PWM com uma faixa de valores de 0 a 255 para cada cor, é de 16.777.216 cores (256 x 256 x 256).

#CORES DO ARCO-ÍRIS
Neste projeto utilizamos as cores do arco-íris definidas como:

| #FF0000 | RGB (255, 0, 0)|
| --- | --- |
| #FF7F00 | RGB (255, 127, 0) |
| #FFFF00 | RGB (255, 255, 0) |

