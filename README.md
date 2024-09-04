# AMR Modelling

Este repositório contém a modelagem de um sistema AMR (Autonomous Mobile Robot) usando a linguagem AADL (Architecture Analysis & Design Language).

## Índice

- [Introdução](#introdução)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Uso](#uso)
- [Detalhes do Modelo](#Detalhes-do-modelo)

## Introdução

O objetivo deste projeto é fornecer um modelo detalhado de um sistema AMR, incluindo a arquitetura e o comportamento dos componentes do sistema. Utilizamos AADL para descrever a arquitetura e gerar diagramas e documentação.

## Estrutura do Projeto

Abaixo está a estrutura principal do projeto:

- **AMR_Model.aadl**: Arquivo principal do modelo AADL que descreve o sistema AMR.
- **diagrams/**: Contém diagramas gerados a partir do modelo AADL.
  - `AMR_sys.aadl_diagram`: Diagrama do sistema AMR.
  - `AMR_sys_AMRSystem_impl.aadl_diagram`: Implementação do sistema AMR.
  - `AMR_sys_Controller_impl.aadl_diagram`: Implementação do controlador do sistema.
  - `AMR_sys_MainProcessor_impl.aadl_diagram`: Implementação do processador principal.
- **docs/html/**: Documentação gerada em formato HTML.
  - `README.html`: Introdução e visão geral do sistema.
  - `images/`: Imagens associadas aos resultados de simulações e diagramas.

## Requisitos

Certifique-se de ter o seguinte software instalado:

- **AADL Toolset**: Para editar e analisar os modelos AADL.
- **Graphviz**: Para gerar diagramas a partir dos modelos.

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/amr-modelling.git
cd amr-modelling
```

## Uso

1. Abra o arquivo `AMR_Model.aadl` no OSATE (Open Source AADL Tool Environment), que é uma plataforma para editar, analisar e verificar modelos AADL.
2. Utilize o OSATE para analisar o sistema AMR, visualizar as propriedades dos componentes e suas interconexões.

## Detalhes do Modelo

O projeto e definido no arquivo `AMR_Model.aadl` que define a arquitetura de um sistema AMR (Autonomous Mobile Robot) com os seguintes componentes:

- **AMRSystem**: O sistema principal que possui uma propriedade de limite de peso (`WeightLimit`) de 2,5 kg.
- **Componentes do Sistema**:
  - **Lidar Sensor (`my_lidar_sensor`)**: Sensor de detecção de obstáculos.
  - **Wheels Actuator (`my_wheels_actuator`)**: Atuador que controla as rodas do robô.
  - **Controller (`my_controller`)**: Processa dados do sensor e controla o atuador.
  - **HWConnection (`my_bus`)**: Barramento de hardware para comunicação entre componentes.
  - **Main Processor (`my_processor`)**: Processador principal para execução do controlador.
- **Conexões e Comunicação**:
  - Conexões de portas são estabelecidas entre o sensor Lidar e o controlador, e entre o controlador e o atuador das rodas, permitindo o fluxo de dados para detecção de obstáculos e controle das rodas.
  - Acessos ao barramento definem como os componentes interagem com o `my_bus`.

Este modelo fornece uma visão abrangente da arquitetura de um sistema AMR, permitindo análises de desempenho, segurança e outras propriedades de sistemas usando o OSATE.
