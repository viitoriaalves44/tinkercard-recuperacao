# Internet das Coisas (IoT) + Arduino

![IoT](https://img.shields.io/badge/IoT-Arduino-blue)
![Arduino](https://img.shields.io/badge/Arduino-Education-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Sobre o Repositório

Este repositório reúne conteúdos teóricos e práticos sobre Internet das Coisas (IoT) utilizando Arduino, abordando desde conceitos básicos até aplicações reais conectadas à internet.

O material foi organizado para estudantes, pesquisadores, desenvolvedores iniciantes e profissionais que desejam compreender o funcionamento de sistemas embarcados conectados.

---

# Objetivos

Ao concluir este conteúdo você será capaz de:

- Entender os conceitos fundamentais da IoT.
- Programar placas Arduino.
- Trabalhar com sensores e atuadores.
- Compreender protocolos de comunicação.
- Conectar dispositivos à internet.
- Utilizar plataformas em nuvem.
- Desenvolver projetos IoT completos.
- Entender o fluxo de dados em ambientes IoT.

---

# Estrutura de Estudos

## 1. Introdução à IoT

### O que é Internet das Coisas?

Internet das Coisas (Internet of Things - IoT) é um paradigma tecnológico que permite que objetos físicos coletem, processem e compartilhem informações através da internet.

### Exemplos

- Casas inteligentes
- Agricultura inteligente
- Indústria 4.0
- Cidades inteligentes
- Monitoramento ambiental
- Saúde conectada

### Benefícios

- Automação
- Monitoramento remoto
- Eficiência operacional
- Redução de custos
- Tomada de decisão baseada em dados

---

# 2. Introdução ao Arduino

Arduino é uma plataforma de prototipagem eletrônica composta por hardware e software livres.

## Principais Placas

### Arduino Uno

- ATmega328P
- 14 portas digitais
- 6 portas analógicas

### Arduino Mega

- Mais memória
- Mais portas de entrada e saída

### ESP8266 e ESP32

Muito utilizados em IoT devido à conectividade Wi-Fi integrada.

---

# Estrutura Básica de Programa

```cpp
void setup() {

}

void loop() {

}
```

## Setup

Executado apenas uma vez.

## Loop

Executado continuamente.

---

# 3. Eletrônica Básica

## Grandezas Fundamentais

### Tensão

Medida em Volts (V).

### Corrente

Medida em Ampères (A).

### Resistência

Medida em Ohms (Ω).

---

## Lei de Ohm

```text
V = R x I
```

Onde:

- V = Tensão
- R = Resistência
- I = Corrente

---

# 4. Sensores

Sensores convertem grandezas físicas em sinais elétricos.

## Sensores Mais Utilizados

### DHT11

Mede:

- Temperatura
- Umidade

### LDR

Mede luminosidade.

### HC-SR04

Mede distância.

### MQ-2

Detecta gases e fumaça.

---

# Exemplo DHT11

```cpp
#include <DHT.h>

#define DHTPIN 2
#define DHTTYPE DHT11

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(9600);
  dht.begin();
}

void loop() {

  float temperatura = dht.readTemperature();
  float umidade = dht.readHumidity();

  Serial.print("Temperatura: ");
  Serial.println(temperatura);

  Serial.print("Umidade: ");
  Serial.println(umidade);

  delay(2000);
}
```

---

# 5. Atuadores

Atuadores realizam ações físicas.

## Exemplos

- LEDs
- Relés
- Motores
- Servo motores
- Buzzer

---

# Exemplo Blink

```cpp
void setup() {
 pinMode(13, OUTPUT);
}

void loop() {

 digitalWrite(13, HIGH);
 delay(1000);

 digitalWrite(13, LOW);
 delay(1000);

}
```

---

# 6. Comunicação em IoT

A comunicação conecta dispositivos, servidores e usuários.

## Tecnologias

### Wi-Fi

Mais utilizada em ambientes domésticos.

### Bluetooth

Comunicação de curta distância.

### ZigBee

Baixo consumo energético.

### LoRa

Longa distância.

---

# Protocolos

## HTTP

Base da web moderna.

## MQTT

Protocolo leve para IoT.

## CoAP

Utilizado em dispositivos restritos.

---

# MQTT

Arquitetura:

```text
Publisher
     ↓
Broker
     ↓
Subscriber
```

Vantagens:

- Leve
- Rápido
- Pouco consumo de banda

---

# 7. Computação em Nuvem

Serviços frequentemente usados em IoT:

## ThingSpeak

Armazenamento e gráficos.

## Firebase

Banco de dados em tempo real.

## Blynk

Controle por aplicativo móvel.

## AWS IoT

Infraestrutura escalável para dispositivos.

---

# 8. Projetos Práticos

## Projeto 1

Monitoramento de Temperatura

Componentes:

- Arduino
- DHT11
- ESP8266

Objetivo:

Enviar temperatura para a internet.

---

## Projeto 2

Casa Inteligente

Componentes:

- ESP32
- Relé
- Aplicativo móvel

Objetivo:

Controlar dispositivos remotamente.

---

## Projeto 3

Irrigação Inteligente

Componentes:

- Sensor de umidade do solo
- Relé
- Bomba d'água

Objetivo:

Automatizar irrigação.

---

# Exercícios

## Básico

1. Piscar LED.
2. Ler botão.
3. Acender LED por botão.

## Intermediário

1. Ler temperatura.
2. Ler distância.
3. Controlar servo motor.

## Avançado

1. Enviar dados via MQTT.
2. Criar dashboard.
3. Desenvolver automação residencial.

---

# Próximo Conteúdo

O arquivo READMEfinal.md apresenta a arquitetura completa da Internet das Coisas e explica detalhadamente como os dados circulam em sistemas IoT.
