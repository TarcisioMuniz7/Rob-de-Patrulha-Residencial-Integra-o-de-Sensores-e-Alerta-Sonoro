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

 - Placa Arduino Uno 
 - Placa Arduino Mega
 - Placa de Ensaio (Protoboard)
 - Sensor PIR
 - Sensor Ultrassônico
 - Duas Rodas, 2 Pilhas Grandes (Tamanho | Voltagem), e Estética

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

#define PIR 2
#define LED 3



void setup() {
	pinMode(PIR, INPUT);
	pinMode(LED, OUTPUT);
	Serial.begin(9600);
	
	
}	

void loop() {
	if (digitalRead(PIR == HIGH)) {
		digitalWrite(LED, HIGH);
	} else {
		digitalWrite(LED, LOW);
	}
	
	Serial.write("Algo quente ou alguém próximo a máquina");
}
~~~
</details>

> Recomendado a soldagem ao menos dos cabos de alimentação
> 
