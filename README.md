# RoboCognitionHub

![Build Status](https://img.shields.io/badge/status-WIP-orange.svg) 
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Visão Geral do Projeto

Este repositório visa desenvolver um framework para **Interação Humano-Robô (HRI)** avançada, focando na comunicação verbal e na **cognição de robôs através de Large Language Models (LLMs)**. Nosso objetivo é permitir que robôs humanoides ou múltiplos robôs entendam comandos de voz (STT), respondam naturalmente (TTS) e usem a inteligação dos LLMs para gerenciar e executar suas ações de forma contextualizada.

Este projeto é um esforço de pesquisa colaborativo, onde exploraremos a integração de modelos de fala com capacidades de LLM para criar uma interface de comando e controle mais intuitiva e inteligente para sistemas robóticos.

## Recursos e Funcionalidades Planejadas

- **Comunicação Verbal (STT/TTS):** Integração e avaliação de modelos como `whisper-large-v3` e `playai-tts`.
- **Cognição e Gerenciamento de Ações:** Utilização de LLMs para interpretar comandos, planejar e executar sequências de ações robóticas.
- **Interface ROS:** Conectividade com sistemas robóticos via Robot Operating System.
- **Estrutura Modular:** Design para facilitar a experimentação e substituição de componentes de STT, TTS e LLM.

## Como Começar

Siga estas instruções para configurar e rodar o projeto localmente.

### Pré-requisitos

* Python 3.8+
* Git
* [ROS (Robot Operating System)](http://wiki.ros.org/ROS/Installation) - Versão `[especificar versão]`
* Uma conta e chave de API para serviços externos (ex: Groq, ElevenLabs, OpenAI) configuradas conforme `config/credentials.example.yaml`.

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/EAI-IA/RoboCognitionHub.git](https://github.com/EAI-IA/RoboCognitionHub.git)
    cd RoboCognitionHub
    ```
2.  **Crie e ative um ambiente virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate # No Linux/macOS
    # venv\Scripts\activate   # No Windows
    ```
3.  **Instale as dependências Python:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Configuração de Credenciais:**
    Crie um arquivo `config/credentials.yaml` com suas chaves de API, seguindo o exemplo em `config/credentials.example.yaml`. **Não commite seu arquivo `credentials.yaml`!**

### Como Rodar Experimentos

Para executar um experimento específico, navegue até a pasta `experiments/` e use os scripts fornecidos. Exemplo:

```bash
python experiments/stt_tts_models/whisper_v3_test.py
```

Para detalhes sobre cada experimento, consulte os respectivos arquivos dentro da pasta `experiments/`