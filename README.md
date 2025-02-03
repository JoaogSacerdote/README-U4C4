# Projeto BitDogLab - Controle de Matriz de LEDs WS2812

## Descrição
Este projeto foi desenvolvido para controlar uma matriz de LEDs WS2812 (5x5) conectada a um Raspberry Pi Pico ou placa compatível (como a BitDogLab). O programa permite incrementar ou decrementar um número exibido na matriz de LEDs usando dois botões físicos. Além disso, o LED RGB integrado pisca continuamente 5 vezes por segundo para indicar que o sistema está funcionando.

### Funcionalidades
- **Botão A (GPIO 5):** Incrementa o número exibido na matriz de LEDs.
- **Botão B (GPIO 6):** Decrementa o número exibido na matriz de LEDs.
- **Matriz de LEDs WS2812:** Exibe números de 0 a 9 em cores diferentes.
- **LED RGB:** Pisca o LED vermelho 5 vezes por segundo.
- **Debouncing:** Implementado para evitar leituras múltiplas indesejadas dos botões.

---

## Requisitos

### Hardware
- Raspberry Pi Pico ou placa compatível (como BitDogLab).
- Matriz de LEDs WS2812 (5x5) conectada ao pino GPIO 7.
- Dois botões conectados aos pinos GPIO 5 e GPIO 6.
- LED RGB conectado aos pinos GPIO 13 (vermelho), GPIO 12 (verde) e GPIO 11 (azul).

### Software
- **CMake** (versão 3.13 ou superior).
- **Pico SDK** (versão 2.1.0 ou superior).
- **Toolchain GCC** para ARM Cortex-M0+.
- **Ninja** (opcional, mas recomendado para compilação rápida).

---

## Estrutura do Projeto

tarefa-U4C4/
├── CMakeLists.txt # Configuração do CMake
├── main.c # Código principal do projeto
├── ws2812.pio.h # Programa PIO para controle dos LEDs WS2812
├── build/ # Diretório de compilação (gerado automaticamente)
└── README.md # Documentação do projeto



---

## Instruções de Configuração

### 1. Instale as Ferramentas Necessárias
Certifique-se de que as seguintes ferramentas estão instaladas no seu sistema:
- **CMake**: [Download](https://cmake.org/download/)
- **Pico SDK**: [Repositório Oficial](https://github.com/raspberrypi/pico-sdk)
- **Toolchain GCC**: [Download](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)

### 2. Clone o Projeto
Clone este repositório para o seu computador:
```bash
git clone https://github.com/seu-usuario/tarefa-U4C4.git
cd tarefa-U4C4