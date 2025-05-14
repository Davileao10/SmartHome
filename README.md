# 🔌 SmartHome com Raspberry Pi Pico W

Projeto de automação residencial utilizando o **Raspberry Pi Pico W** com MicroPython. A ideia é controlar dispositivos como **LEDs RGB** e **buzzers** através de uma **interface web** simples e responsiva, diretamente pelo navegador.

## 🚀 Funcionalidades

- Controle remoto via Wi-Fi (servidor web embarcado)
- Interface web intuitiva para:
  - Ajuste de cor e intensidade do LED RGB
  - Acionamento de um buzzer via botão virtual
- Código limpo e comentado, ideal para fins didáticos

## 📷 Interface Web

<div align="center">
  <img src="screenshot.png" alt="Interface Web" width="500"/>
</div>

## 🧰 Tecnologias utilizadas

- [Raspberry Pi Pico W](https://www.raspberrypi.com/products/raspberry-pi-pico-w/)
- MicroPython
- HTML + CSS (embarcado no código .py)
- Python `socket` para servidor web local

## 📦 Como rodar o projeto

### 1. Requisitos

- Raspberry Pi Pico W
- Firmware MicroPython atualizado
- Editor com suporte a MicroPython (ex: Thonny)

### 2. Clone o repositório

```bash
git clone https://github.com/Davileao10/SmartHome.git
````

### 3. Transfira os arquivos `.py` para a Pico W

Use o Thonny ou outra IDE compatível com MicroPython para enviar os arquivos para o dispositivo.

### 4. Configure sua rede Wi-Fi

No arquivo `main.py`, altere:

```python
SSID = "SEU_SSID"
PASSWORD = "SUA_SENHA"
```

### 5. Execute o script

Rode o `main.py`. O terminal irá exibir o IP local da sua placa. Acesse este IP via navegador para controlar os dispositivos.

## 📁 Estrutura do projeto

```
SmartHome/
├── index.html         # Página web (embarcada no código)
├── main.py            # Código principal (servidor + lógica de controle)
├── utils.py           # Funções auxiliares
└── README.md          # Este arquivo
```

## 💡 Futuras melhorias

* Integração com sensores (temperatura, luminosidade etc.)
* Controle por comandos de voz (via browser)
* Dashboard com status em tempo real

## 📸 Demonstração

<!-- Se tiver vídeo no YouTube ou GIF, coloque aqui -->

Feito com 💻 por [Davi Nascimento Leão](https://github.com/Davileao10)

