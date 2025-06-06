# 🚗 Medidor de Pressão de Pneus com STM32 (Projeto Integrador III – FATEC Jundiaí)

Este repositório apresenta o desenvolvimento de um **medidor eletrônico de pressão de pneus**, utilizando microcontroladores da família **STM32** (modelo STM32C011F6P6), sensores digitais, display OLED e desenvolvimento em linguagem C/C++ com a IDE STM32CubeIDE.

Projeto realizado como parte da disciplina **Projeto Integrador III** do curso de **Sistemas Embarcados** da FATEC Jundiaí, em parceria com a **STMicroelectronics** e a **TEX Tecnologia**.

---

## 📌 Objetivo

Desenvolver um **MVP funcional** de um dispositivo portátil capaz de medir com precisão a pressão dos pneus de um veículo, com exibição clara das informações, operação intuitiva e custo compatível com o mercado.

---

## 🔧 Componentes Utilizados

| Componente                     | Finalidade                                           |
|-------------------------------|------------------------------------------------------|
| STM32C011F6P6                 | Microcontrolador principal                          |
| Display OLED 128x64          | Exibição de pressão e unidade (psi/bar)             |
| Sensor BMP280                 | Sensor de temperatura e pressão barométrica         |
| Sensor de Pressão SMP3011     | Leitura digital de pressão (até 40 psi)             |
| Cabos Dupont (M-M/F-F)        | Conexões elétricas                                  |
| Protoboard                    | Montagem do circuito sem solda                      |
| ST-Link V2                    | Programação da placa STM32 via USB                  |
| Computador c/ STM32CubeIDE    | Desenvolvimento e upload do firmware                |

---

## 🛠️ Requisitos do Sistema

### ✅ Requisitos Funcionais

- Leitura da pressão em tempo real;
- Exibição no display OLED com unidade (psi/bar);
- Alerta visual para pressão inadequada;
- Função de calibração;
- Detecção automática de conexão com o pneu.

### ⚙️ Requisitos Não-Funcionais

- Precisão inferior a 5%;
- Tempo de resposta < 2s;
- Interface amigável e intuitiva;
- Tolerância IP65 (resistente à água/poeira);
- Operação entre 0ºC a 45ºC;
- Baixo consumo de energia;
- Portabilidade (leve e compacto).

---

## 📈 Planejamento do Projeto

- Planejamento e cronograma com **GanttProject**;
- Análise **SWOT** para identificação de forças, fraquezas, oportunidades e ameaças;
- Modelagem com **diagramas de blocos, caso de uso e diagrama de estados**;
- Implementação inicial com LED blink e exibição de texto no OLED;
- Desenvolvimento final com leitura do sensor de pressão e exibição da medição.

---

## 🧩 Arquitetura do Sistema

- O **STM32** atua como controlador central.
- Os sensores **BMP280** e **SMP3011** se comunicam via **I²C**.
- O display OLED exibe os valores e alertas para o usuário.
- Fonte de alimentação via USB ou bateria.
- O firmware foi desenvolvido em **C/C++** utilizando a **STM32CubeIDE**, com uso de biblioteca HAL.

---

## 💡 Desafios Enfrentados

- Substituição do sensor BMP280 pelo BMP180 em testes;
- Limitações de memória e ausência de unidade FPU no STM32C0;
- Adaptação da biblioteca do sensor SMP3011, originalmente feita para ESP32, para compatibilidade com HAL da STM32 (com apoio do Prof. Cláudio).

---

## 💾 Software Utilizado

- **STM32CubeIDE** – para configuração dos pinos, clock, periféricos e desenvolvimento do código.
- **GanttProject** – para planejamento e cronograma.
- **Fusion 360 / Lucidchart** – para diagramação e design.

---

## 🧪 Resultados

- O protótipo funcional realiza a leitura da pressão em tempo real.
- Permite a seleção da unidade e emite alertas visuais.
- Testado com sensor SMP3011 e display OLED com interface limpa.
- A arquitetura e modularização permitem futuras expansões.


---

## 📚 Referências

- [STM32 – STMicroelectronics](https://www.st.com/)
- [BMP280 – Bosch Sensor](https://www.bosch-sensortec.com/)
- [SMP3011 Sensor](https://pressuretemperaturesensor.sell.everychina.com/)
- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)

---

## 📄 Licença

Este projeto é de uso **educacional e acadêmico** no âmbito da FATEC Jundiaí – 2025.
