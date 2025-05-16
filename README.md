# Robô de Patrulha Residencial (Integração de Sensores e Alerta Sonoro)
Robô de segurança residencial com Arduino, capaz de detectar presença com sensores PIR, e ultrassônico. Emite alarme sonoro ao identificar intrusos e se move autonomamente para monitorar diferentes áreas da casa.
<h2> Imagem em Miniatura [EDITADA] </h2>

![430x430](https://github.com/user-attachments/assets/3fcf40a7-da7c-41e9-9e30-e49a3ae93f52)



>[!Note]
> É necessário compreender o uso da ponte-H para o funcionamento dos motores.

 
 ### Projeto - Robô Patrulha
---
 ## Info

 Projeto desenvolvido por:

 ## Componentes
### Placas
 - Placa Arduino Uno 
 - Placa Arduino Esp
 - Placa de Ensaio (Mini Protoboard)
   
### Sensores
 - Sensor PIR
 - Sensor Ultrassônico
   
### Atuadores
 - Dois Motores DC (3v-6v)
 - Buzzer Ativo
 - Ponte H 
 - Suporte a Pilhas
 -  2 Pilhas Grandes (Tamanho | Voltagem)
   
### Estética
 - Chassi
 - Duas Rodas + Uma Roda Boba
   
>[!Note]
> Faltam apenas os Jumpers Macho. Basta ver quantos pinos possuem os sensores para o Cálculo (e o Buzzer).

 ## Objetivo

 Monitorar ambiente ao redor, desviar de obstáculos frontais, e detectar presença de seres vivos ou objetos por meio do calor/temperatura.

 ## Funções

 -- Correr automaticamente para frente enquanto não houver obstáculos detectados.
 
 -- Detecção a um raio de 3m a 7m.
 
 -- Desviar de obstáculos a frente do robô (ultrassõnico) menormente previsível.

 ## Contribuições

 ``` bash
 #Clone o projeto
 $ git clone

```

<h2> Imagens em Tamanho Maior [EDITADA]</h2>

![820x917_](https://github.com/user-attachments/assets/74cfa81d-6869-4b4c-a858-b1584da04868)

<details>
  <summary>
<h2> Imagem Original [EDITADA] </h2> </summary>

![Foto do robô (Editada) (2)](https://github.com/user-attachments/assets/25fde635-f954-4c63-bb62-54488ad9be7c)

</details>

 ## Referências





#### Testes (Código)
<details> <!-- Permite o uso de uma seção interativa -->
  
<summary> Rodas (a fazer) </summary> <!-- Título da Seção Interativa -->
<h1> Teste das Rodas </h1>
<h2> C++ </h2>

 ~~~C++

void setup() {
}
~~~
</details> <!-- Identifica Final da Seção Interativa -->

<details>
<summary> PIR </summary>
<h1> Teste do Sensor PIR</h1>
<h2> C++ </h2>
  
~~~C++

/* Código - Teste - PIR 
Produzido para:
 
-- Melhor configuração da sensibilidade
-- Calibração do Sensor
-- Análise de erros físicos ou bugs */

#define PIR 2 // Pino de dados do PIR
#define LED 3 // Pino de alimentação da LED 

/* Não ligue a LED sem Resistor  | Não necessita do LED para o Teste*/

void setup() {

	pinMode(PIR, INPUT); // Define PIR (Conexão ao Pino) para Entrada de Dados ao Arduino
	pinMode(LED, OUTPUT); // Define LED para Saída de Dados do Arduino
	Serial.begin(9600); // Conexão Serial para Amostra/Avaliação dos Dados
}	

void loop() {

	if (digitalRead(PIR == HIGH)) {        // Se o sensor PIR ler e reagir com impulso elétrico alto.. (Detectar calor)
		digitalWrite(LED, HIGH);      // Envie (write) energia (HIGH) máxima da porta 2 (LED) do arduino (5v)  para LED  // Liga a LED  
		Serial.write("Algo quente ou alguém próximo a máquina"); // Enviar mensagem para Monitor Serial  //Confirme no Monitor Serial (Computador + IDE)
	} else {
		digitalWrite(LED, LOW); //Envie a energia mínima (LOW) do Arduino (0v) da porta 2 (LED) para a LED // Desliga a LED
		}
}
	
	
~~~
</details>

> Recomendado a soldagem ao menos dos cabos de alimentação
> 
