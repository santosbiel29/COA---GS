# 🛰️ Space Weather Guardian
### Sistema IoT para Monitoramento de Cápsula Espacial
**Global Solution 2026 — 1º Semestre | FIAP | Engenharia de Software — IoT**

---

## 👥 Equipe

| Nome | RM |
|---|---|
| Gabriel de Almeida Santos | 569395 |
| Guilherme Henrique Garbelini | 571150 |
| Herbert Soares de Jesus | 571507 |

**Turma:** 1CCPX — Ciências da Computação

---

## 🔗 Links do Projeto

- 🔌 **Simulação Wokwi:** [https://wokwi.com/projects/466208128232216577]
- 📹 **Vídeo explicativo:** [https://www.canva.com/design/DAHMB-1-BUA/MGShLrv7glRTg1B3hdJhSQ/edit]
- 📄 **Relatório técnico:** [https://docs.google.com/document/d/1SYhxWepQdwf5EM8MQxGJdt6_F-i2r5cIUpyMKob0uvo/edit?usp=sharing]

---

## 📋 Sobre o Projeto

O **Space Weather Guardian** é um sistema IoT embarcado para monitoramento em tempo real das condições internas de uma cápsula espacial simulada. O sistema coleta dados de temperatura, luminosidade e vibração, processa essas informações localmente e comunica o estado operacional através de um display LCD e um LED RGB com três níveis de alerta.

### Equação de Alertas

```
CRÍTICO  → temperatura > 40°C  OU  vibração > 20
ATENÇÃO  → temperatura > 30°C  OU  luminosidade < 1000
NORMAL   → todos os parâmetros dentro dos limites
```

---

## 🧩 Componentes Utilizados

| Componente | Função |
|---|---|
| ESP32 DevKit V1 | Microcontrolador principal |
| DHT22 | Sensor de temperatura e umidade |
| Sensor LDR (analógico) | Sensor de luminosidade |
| MPU6050 | Sensor de vibração/aceleração |
| Display LCD I2C 16x2 | Exibição dos dados em tempo real |
| LED RGB | Indicador visual de estado operacional |

---

## ⚡ Pinagem

| Componente | Pino ESP32 |
|---|---|
| DHT22 (dados) | GPIO 15 |
| LDR (analógico) | GPIO 34 |
| MPU6050 SDA | GPIO 21 |
| MPU6050 SCL | GPIO 22 |
| LCD SDA | GPIO 21 |
| LCD SCL | GPIO 22 |
| LED Vermelho | GPIO 25 |
| LED Verde | GPIO 26 |
| LED Azul | GPIO 27 |

---

## 💻 Como Executar

1. Acesse a simulação no Wokwi: https://wokwi.com/projects/466208128232216577
2. Clique em **"Play"** para iniciar a simulação
3. Observe o display LCD alternando entre as telas de dados
4. Interaja com os sensores no painel do Wokwi para testar os alertas
5. Acompanhe os valores no **Monitor Serial** (115200 baud)

---

## 📊 Estados Operacionais

| Estado | LED | Condição | LCD |
|---|---|---|---|
| ✅ Normal | 🟢 Verde | Temp ≤ 30°C, Luz ≥ 1000, Vibração ≤ 20 | `Status: OK` |
| ⚠️ Atenção | 🟡 Amarelo | Temp > 30°C ou Luz < 1000 | `Status: ATENCAO` |
| 🚨 Crítico | 🔴 Vermelho | Temp > 40°C ou Vibração > 20 | `Status: CRITICO` |

---

## 🗂️ Estrutura do Repositório

```
space-weather-guardian/
├── README.md
├── sketch.ino          # Código fonte principal
├── relatorio/
│   └── SpaceWeatherGuardian_Relatorio.pdf
└── docs/
    ├── circuito.png
    ├── estado_normal.png
    ├── estado_atencao.png
    └── estado_critico.png
```

---

## 🌍 ODS Relacionados

- **ODS 9** — Indústria, Inovação e Infraestrutura
- **ODS 11** — Cidades e Comunidades Sustentáveis
- **ODS 13** — Ação Contra a Mudança Global do Clima

---

## 📄 Licença

Projeto desenvolvido para fins acadêmicos — FIAP Global Solution 2026.
