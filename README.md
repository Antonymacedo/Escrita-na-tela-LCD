# Escrita na tela LCD
Texto escrito em uma tela LCD

__Materiais__

 ●Tela LCD

 ●Potenciometro

 ●Arduino Uno

 ![Opera Instantâneo_2024-12-12_212413_www tinkercad com](https://github.com/user-attachments/assets/c672b9b5-98b2-437a-8b14-ac83267646e4)

# Esquema de Conexão:

__Display LCD 16x2:__

Pinos de Controle:

RS: Conecte ao pino digital 12 do Arduino.

E: Conecte ao pino digital 11 do Arduino.

Pinos de Dados:

D4, D5, D6, D7: Conecte aos pinos digitais 5, 4, 3, 2 do Arduino, respectivamente.

__Pino de Contraste:__

Conecte o meio do potenciômetro ao pino V0 do LCD, um terminal ao GND e o outro ao 5V.

# Código

```
#include <LiquidCrystal.h> //Inclui a biblioteca do LiquidCrytal
LiquidCrystal lcd(12, 11, 5, 4, 3, 2); // Declara as portas de saída para o LCD
void setup() {
  lcd.begin(16, 2); //Inicia a escrita no LCD
  lcd.print("GITHUB ANTONY");//Exibe a mensagem que irá imprimir
}
void loop() {
  lcd.setCursor(0, 1); //Define o cursor em (0,1)
  lcd.print(millis()/1000); //Faz a contagem do tempo e o mostra na tela do LCD
  lcd.print("s"); //Escreve a letra s para representar os segundos
}
```
__Projeto no simulador__

https://www.tinkercad.com/things/8pVD0WnAPAc-display-lcd-16x2
