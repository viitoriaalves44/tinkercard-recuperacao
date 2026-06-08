# Comunicação e Relação de Dados na Internet das Coisas (IoT)

## Introdução

A Internet das Coisas é baseada na troca contínua de informações entre dispositivos físicos, sistemas computacionais, redes de comunicação e usuários.

Todo sistema IoT possui um fluxo de dados que permite monitoramento, automação e tomada de decisão em tempo real.

---

# Arquitetura Geral da IoT

```text
Sensores
    ↓
Microcontrolador
    ↓
Rede de Comunicação
    ↓
Internet
    ↓
Servidor/Nuvem
    ↓
Banco de Dados
    ↓
Aplicação
    ↓
Usuário
```

---

# Camadas da Arquitetura IoT

## Camada Física

Responsável pela coleta de dados.

Exemplos:

- Sensores
- Atuadores
- Dispositivos embarcados

### Dados coletados

- Temperatura
- Umidade
- Luminosidade
- Distância
- Pressão
- Movimento

---

## Camada de Processamento Local

Representada por dispositivos como:

- Arduino
- ESP8266
- ESP32

Funções:

- Ler sensores
- Filtrar informações
- Tomar decisões simples
- Preparar dados para envio

Exemplo:

```cpp
if(temperatura > 30){
   ligarVentilador();
}
```

---

## Camada de Comunicação

Responsável pela transmissão dos dados.

Tecnologias:

### Wi-Fi

Alta velocidade.

### Bluetooth

Curta distância.

### ZigBee

Baixo consumo.

### LoRa

Longa distância.

### Ethernet

Alta estabilidade.

---

# Protocolos Utilizados

## HTTP

Modelo:

```text
Cliente → Servidor
```

Muito utilizado para APIs REST.

---

## MQTT

Modelo:

```text
Publisher
     ↓
Broker
     ↓
Subscriber
```

Características:

- Leve
- Eficiente
- Ideal para IoT

---

## CoAP

Utilizado em dispositivos de baixa capacidade computacional.

---

# Fluxo Completo dos Dados

Exemplo de monitoramento de temperatura.

```text
Sensor DHT11
       ↓
Arduino/ESP32
       ↓
Wi-Fi
       ↓
Broker MQTT
       ↓
Servidor
       ↓
Banco de Dados
       ↓
Dashboard
       ↓
Usuário
```

---

# Exemplo Real

Um sensor detecta:

```text
Temperatura = 32°C
Umidade = 65%
```

O dispositivo envia:

```json
{
  "temperatura": 32,
  "umidade": 65
}
```

O servidor armazena.

O dashboard exibe.

O usuário visualiza.

---

# Ciclo de Vida dos Dados

## 1. Geração

Os sensores produzem informações.

Exemplo:

```text
28°C
```

---

## 2. Coleta

Arduino captura o valor.

---

## 3. Transmissão

Os dados são enviados para rede.

---

## 4. Armazenamento

Os dados ficam registrados.

Exemplos:

- Firebase
- MySQL
- PostgreSQL
- MongoDB

---

## 5. Processamento

Os sistemas analisam os dados.

Exemplos:

- Estatísticas
- Alertas
- Machine Learning

---

## 6. Visualização

Os dados são apresentados em:

- Dashboards
- Aplicativos
- Sistemas Web

---

## 7. Ação

O sistema toma decisões.

Exemplo:

```text
Temperatura > 30°C
        ↓
Aciona ventilador
```

---

# Comunicação entre Dispositivos

## Device-to-Device (D2D)

```text
Sensor
   ↓
Arduino
```

---

## Device-to-Cloud

```text
ESP32
   ↓
Internet
   ↓
Cloud
```

---

## Device-to-Gateway

```text
Sensor
   ↓
Gateway
   ↓
Internet
```

---

# Segurança na Comunicação IoT

Boas práticas:

- HTTPS
- TLS/SSL
- Certificados digitais
- Autenticação
- Criptografia de dados

---

# Desafios da IoT

## Escalabilidade

Grande número de dispositivos.

## Segurança

Proteção contra invasões.

## Disponibilidade

Garantir funcionamento contínuo.

## Integridade

Garantir que os dados não sejam alterados.

---

# Relação Entre os Dados na IoT

Os dados possuem dependência direta entre as camadas.

Exemplo:

```text
Temperatura
       ↓
Processamento
       ↓
Análise
       ↓
Tomada de decisão
       ↓
Ação física
```

Portanto, um dado coletado por um sensor pode gerar ações automáticas em dispositivos conectados.

---

# Exemplo Completo de Automação Residencial

```text
Sensor de Temperatura
          ↓
ESP32
          ↓
MQTT
          ↓
Servidor
          ↓
Dashboard
          ↓
Regra de Automação
          ↓
Relé
          ↓
Ventilador
```

Quando a temperatura ultrapassa o limite configurado:

1. O sensor mede.
2. O ESP32 processa.
3. O MQTT envia.
4. O servidor analisa.
5. A automação é acionada.
6. O ventilador liga automaticamente.

---

# Conclusão

A Internet das Coisas integra sensores, dispositivos embarcados, redes de comunicação, servidores e aplicações para transformar dados do mundo físico em informações úteis.

O fluxo de dados ocorre continuamente desde a coleta até a ação final, permitindo monitoramento, automação, análise e tomada de decisão em tempo real. Dessa forma, a IoT se torna uma das principais tecnologias da transformação digital e da Indústria 4.0.
