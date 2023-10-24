## RGBlight
##OBJETIVO DO TRABALHO

Desenvolver uma lâmpada de ambiente com efeito "mood" usando três LEDs, um vermelho, um verde e um azul. Neste projeto, a combinação das cores dos LEDs será responsável por criar as cores do arco-íris.

Observação: Uma lâmpada de ambiente "mood" é uma solução estética destinada a iluminar o ambiente com o propósito de refletir e definir a atmosfera (mood) do espaço, em vez de servir como a principal fonte de iluminação.

##APLICAÇÃO

Com o intuito didático, abordaremos o estudo do PWM (Modulação por Largura de Pulso), os valores RGB (Vermelho, Verde e Azul) e suas aplicações em efeitos com LEDs.

O PWM é uma técnica que modula a largura dos pulsos de um sinal elétrico para controlar a intensidade luminosa ou a velocidade de motores, por exemplo. No contexto dos LEDs RGB, o PWM é usado para ajustar a intensidade de cada cor (vermelho, verde e azul), permitindo a criação de diversas cores e tons.

Os LEDs RGB são componentes que emitem luz nas cores vermelha, verde e azul. Combinando essas cores em proporções diferentes, podemos obter uma ampla gama de cores, incluindo todas as cores do espectro visível.

As aplicações práticas desses conceitos incluem a criação de efeitos de iluminação coloridos. Por exemplo, ao ajustar o PWM em um LED RGB, você pode criar efeitos como transições suaves de cor, cores pulsantes e até mesmo simular a iluminação de um "mood lamp" mencionado anteriormente. Isso é comumente usado em projetos de iluminação de ambientes, sinalização colorida, efeitos visuais em espetáculos, entre outros.

O estudo desses conceitos é fundamental para entender como os dispositivos eletrônicos podem controlar e personalizar a cor e a intensidade da luz em uma ampla variedade de aplicações, tornando-os valiosos tanto para fins didáticos quanto para a criação de projetos criativos de iluminação.

##COMPONENTES USADOS
| COMPONENTES | QUANTIDADE | OBSERVAÇÃO|
| :---         |     :---:      |          ---: |
| LED 5mm  | 3  | vermelho, verde, azul   |
| Protoboard   | 1      | 400 pontos   |
| Resistor   | 3    | 1 resistor de 200Ω e 2 de 100Ω   |
| Arduino UNO    | 1       | -----------  |

##COMO FUNCIONA

1- Após iniciar o programa, a mistura das cores dos 3 LEDs (vermelho, verde e azul) gera as cores do arco-íris que vão se alterando lentamente e de forma aleatória.
2- Essa combinação de cores é alcançada ao regular a luminosidade de cada um dos três LEDs usando a técnica de PWM (Modulação por Largura de Pulso), o que resulta em diferentes valores RGB, ou seja, cores distintas. Esse efeito opera de maneira semelhante à composição de um monitor de computador, que é composto por minúsculos pontos vermelhos, verdes e azuis.
3-Difundindo a luz usando um cilindro de papel (folha A4), é possível criar uma agradável mistura de cores. Os LEDs podem ser inseridos em qualquer objeto com capacidade de difusão de luz, ou então é possível refletir a luz usando um material difusor reflexivo. Um  exemplo interessante é posicionar as luzes no interior de uma pequena garrafa de plástico (de preferência, com plástico mais fino), para obter melhores resultados.

Um valor RGB de (255,0,0) representa vermelho puro, (0,255,0) é verde puro e (0,0,255) indica azul puro. Combinando esses valores, é possível criar uma ampla variedade de cores. Mesmo ao alternar simplesmente os LED's entre ligado e desligado, sem ajustar a intensidade luminosa, é possível obter cores diversas.
Ao controlar a luminosidade usando PWM, é possível criar uma variedade ainda mais ampla de cores. Posicionando os LED's próximos uns dos outros e mesclando seus valores, por exemplo, através de um cilíndro de papel, o espectro de luz gerado pelas três cores combinadas resulta em uma cor única. o número toal de cores disponíveis, utilizando PWM com uma faixa de valores de 0 a 255 para cada cor, é de 16.777.216 cores (256 x 256 x 256).

##CORES DO ARCO-ÍRIS

Neste projeto utilizamos as cores do arco-íris definidas como...

| #FF0000 | RGB (255, 0, 0) | vermelho |
| :---         |     :---:      |          ---: |
#FF7F00 | RGB (255, 127, 0) | laranja |
| #FFFF00 | RGB (255, 255, 0) | amarelo |
| #FFFF00 | RGB (0, 255, 0) | verde |
| #0000FF | RGB (0, 0, 255) | azul | 
| #4B0082 | RGB (75, 0, 130) | roxo |
| #8F00FF | RGB (143, 0, 255) | violeta|







##EXPLICAÇÃO DO CÓDIGO

Foi declarado as variáveis COR[], INC[], red, green, blue, redPin, greenPin e bluePin;

float COR1[3];
float COR2[3];
float INC[3];
 
int red, green, blue;
int redPin = 11;
int greenPin = 10;
int bluePin = 9;

1.1 Foi utilizado as variáveis tipo ‘float’ e ‘int’;
1.2 As variáveis red, green e blue, tipo inteiro, se referem aos valores RGB a serem armazenados;
1.3 As variáveis arrays COR1[3], COR2[3] e INC[3], tipo float, se referem aos valores RGB e o valor de Incremento;
1.4  As variáveis tipo inteiro redPin, greenPin e bluePin, se referem aos LEDs 5mm de alto brilho conectados nos pinos 11, 10 e 9 do controlador Arduino.

Na estrutura void setup(), realizamos o seguinte:

 void setup()
{
  COR1[0] = 0;
  COR1[1] = 0;
  COR1[2] = 0;
 
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
}

2.1 Foi configurado os valores da array COR1[] com zero para todos os seus elementos, o que resulta no conjunto de valores iniciais do modelo RGB da lâmpada, onde todos os componentes estão definidos como zero, representando assim o estado inicial da lâmpada, ou seja, a lâmpada está desligada;

2.2 Foram configuradas as variáveis redPin, greenPin e bluePin como saídas do controlador Arduino, usando o modo "OUTPUT", e as conectamos aos pinos 11, 10 e 9, respectivamente. Isso permite que o Arduino controle as saídas nessas portas, que geralmente estão associadas às cores vermelha, verde e azul de um sistema de iluminação RGB. Essa configuração é importante para controlar as cores da lâmpada ou qualquer outro dispositivo RGB conectado ao Arduino.

Na estrutura void loop(), temos o seguinte código:

void loop()
{
  setColor(COR2[0] = 255, COR2[1] = 0, COR2[2] = 0 );  // vermelho
  delay(1500);
  setColor(COR2[0] = 255, COR2[1] = 117, COR2[2] = 10);  // laranja
  delay(1500);
  setColor(COR2[0] = 255, COR2[1] = 255, COR2[2] = 0 );  // amarelo
  delay(1500);
  setColor(COR2[0] = 0, COR2[1] = 255, COR2[2] = 0 );  // verde
  delay(1500);
  setColor(COR2[0] = 0, COR2[1] = 0, COR2[2] = 255 );  // azul
  delay(1500);
  setColor(COR2[0] = 75, COR2[1] = 0, COR2[2] = 130);  // índigo
  delay(1500);
  setColor(COR2[0] = 143, COR2[1] = 0, COR2[2] = 143);  // roxo
}

Nesse trecho do código, o loop é iniciado com a chamada da função setColor() para diferentes cores, o que controla as saídas dos pinos correspondentes e muda a cor da lâmpada. 

3.1. A função setColor() é chamada para definir a cor vermelha, onde o LED vermelho está ligado com 100% de brilho (255), o LED verde e azul estão desligados (0).

3.2. Após definir a cor, há um atraso de 1500 milissegundos (1,5 segundos) usando a função delay(1500).

3.3. Em seguida, a função setColor() é chamada novamente para definir a próxima cor, e esse processo se repete para as diferentes cores do arco-íris.

Quanto à função setColor(), temos o seguinte código:

void setColor(int red, int green, int blue)
{
  for (int x=0; x<3; x++) 
  {
  INC[x] = (COR1[x] - COR2[x]) / 256;
  }
  for (int x=0; x<256; x++) 
  {
    red = int(COR1[0]);
    green = int(COR1[1]);
    blue = int(COR1[2]);
    analogWrite (redPin, red);
    analogWrite (greenPin, green);
    analogWrite (bluePin, blue);
    delay(20);
    COR1[0] -= INC[0];
    COR1[1] -= INC[1];
    COR1[2] -= INC[2];
  }  
}

4.1. O primeiro loop "for" é usado para calcular os valores de incremento (INC[x]) para os canais red, green e blue, permitindo uma transição suave entre as cores. Isso é feito calculando a diferença entre os valores iniciais (COR1[x]) e finais (COR2[x]) e dividindo essa diferença por 256.

for (int x=0; x<3; x++) 
  {
  INC[x] = (COR1[x] - COR2[x]) / 256;
  }


4.2. O segundo loop "for" executa 256 vezes para fazer a transição de cor. Ele atualiza os valores de red, green e blue com base nos valores em COR1[], escreve esses valores nos pinos correspondentes usando a função analogWrite() para controlar o brilho dos LEDs e, em seguida, aguarda 20 milissegundos antes de atualizar os valores de COR1[] para a próxima etapa da transição.

for (int x=0; x<256; x++) 
  {
    red = int(COR1[0]);
    green = int(COR1[1]);
    blue = int(COR1[2]);
    analogWrite (redPin, red);
    analogWrite (greenPin, green);
    analogWrite (bluePin, blue);
    delay(20);
    COR1[0] -= INC[0];
    COR1[1] -= INC[1];
    COR1[2] -= INC[2];
  }  


4.3. Após 256 passos, a cor terá mudado gradualmente de uma cor para outra, e o programa volta ao loop da função loop() para definir a próxima cor do arco-íris.






