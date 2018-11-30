# Casos de uso

## 1. Diagrama de casos de uso

A principal parte do código utiliza um for, utilizando: i = 0 e a variável da lista com os pinos digitais correspondentes aos botões.

Identificando uma outra variável com o digitalRead de um pino digital, é possível criar um if dentro do for para isso, e um segundo if tendo como condição o estado do pino ser low. Nesse caso, haverá um sendNoteOn, utilizando as variáveis note[i], correspondente a nota, a velocity 127 (sendo 0 no caso do estado high) e o canal midi escolhido.

for 
(int i=0; 
i<botoes; i++) 
{
    estadobotao[i] = digitalRead(botao[i]);
  }
  for 
  (int i=0; i<botoes; i++) {

    if (estadobotao[i] != estadobotao[i]) 
    {
      if(estadobotao[i] == LOW) 
      {     
        MIDI.sendNoteOn(nota+i, 127, canalmidi);
      }
      else 
      {
        MIDI.sendNoteOn(nota+i, 0, canalmidi);
      }
    }
