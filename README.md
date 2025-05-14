````markdown
# 🔌 SmartHome com Raspberry Pi Pico W (C SDK)

Projeto de automação residencial utilizando o **Raspberry Pi Pico W** com o **SDK oficial em C**. O sistema cria um **servidor web embarcado** que permite controlar LEDs RGB e um buzzer por meio de uma interface web acessada via Wi-Fi.

## 🚀 Funcionalidades

- Servidor HTTP embarcado
- Interface web para:
  - Controle de LED RGB
  - Acionamento de um buzzer (intensidade)
- Conexão Wi-Fi utilizando o `pico-cyw43-driver`
- Baixo consumo e alta responsividade

## 🧰 Tecnologias Utilizadas

- Raspberry Pi Pico W
- [pico-sdk](https://github.com/raspberrypi/pico-sdk)
- [pico-extras](https://github.com/raspberrypi/pico-extras)
- HTML + CSS embutidos como strings em C
- Servidor web leve baseado em sockets

## 📦 Como Rodar o Projeto

### 1. Requisitos

* Raspberry Pi Pico W
* Toolchain ARM (`arm-none-eabi-gcc`)
* `cmake`, `make`, e `git` instalados
* SDK do Raspberry Pi Pico e extras

### 2. Clone os repositórios

```bash
git clone https://github.com/Davileao10/SmartHome.git
cd SmartHome
git submodule update --init
```

> Certifique-se de que `pico-sdk` está configurado corretamente como submódulo ou no caminho esperado pelo `CMakeLists.txt`.

### 3. Compile o projeto

```bash
mkdir build
cd build
cmake ..
make
```

### 4. Grave o firmware

Conecte o Pico W em modo BOOTSEL e copie o arquivo `.uf2` gerado para ele.

### 5. Acesse a interface

Ao ligar o dispositivo, o IP será mostrado via `printf` na UART (use um terminal serial como `minicom` ou `screen`). Acesse o IP no navegador.

