# CaaS - Compliance as a Service

[![Framework][Streamlit-Badge]][Streamlit-URL]
[![Python][Python-Badge]][Python-URL]
[![License][License-Badge]][License-URL]

Uma aplicação web segura construída com Streamlit para analisar e validar documentos fiscais em formato XML, com sistema de autenticação e IA para análise de conformidade.

## 🎥 Demonstração e Apresentação

* **[Assista ao Vídeo de Demonstração](https://drive.google.com/file/d/1dkfoGFEWArM0pINu1_IwV9Vpu4axMyvk/view?usp=drive_link)**
* **[Acesse a Apresentação (Slides)](https://docs.google.com/presentation/d/1c6EfH-Z35j395XopAMwlj9c0gUG0pbxR/edit?usp=drive_link&ouid=113255689135294023890&rtpof=true&sd=true)**
* **[Acesse a Demonstração (Aplicação)](https://projetofinalfirstclassagents.streamlit.app/)**

## 🚀 Principais Funcionalidades

Este projeto oferece um conjunto robusto de ferramentas para análise e conformidade fiscal, combinando extração de dados com a potência da IA generativa.

### Análise e Extração
* **Extração de Dados XML:** Carregue um ou mais arquivos XML fiscais para extrair e organizar as informações de forma estruturada.
* **Análise Tributária com IA:** Utiliza o Gemini para analisar os dados extraídos, identificar possíveis inconsistências, riscos fiscais e oportunidades de otimização.
* **Validação de Regras:** O sistema valida os documentos com base em um conjunto de regras fiscais pré-definidas (armazenadas em `banco_de_regras.json`).

### Segurança e Criptografia (Compliance as a Service)
* **Proteção Automática:** Criptografia automática de dados sensíveis como CPFs, CNPJs e valores financeiros no momento da extração.
* **Guardrails de Segurança:** Proteção integrada contra ataques de *injection* (XSS, SQL, Command Injection).
* **Busca Segura:** Implementa um sistema de *hash* que permite buscas em dados sensíveis sem a necessidade de descriptografá-los.
* **Visualização Protegida:** Dados sensíveis são automaticamente mascarados na interface web para proteger a informação durante a visualização.
* **Auditoria Completa:** Registro e auditoria de operações de segurança.

### Relatórios e Interface
* **Geração de Relatórios:** Exporte os dados brutos extraídos e os relatórios de análise da IA para os formatos **Excel** e **PDF**.
* **Interface Web Intuitiva:** Sistema de *drag-and-drop* para upload fácil de arquivos.

## 🛠️ Tecnologias Utilizadas

* **Framework Web:** Streamlit
* **Análise de Dados:** Pandas
* **Processamento XML:** xml.etree.ElementTree
* **Criptografia:** Cryptography
* **Inteligência Artificial:** Google Generative AI (Gemini)

## 📋 Pré-requisitos

Para executar este projeto, você precisará de:

* Python 3.8 ou superior
* `pip` (gerenciador de pacotes do Python)
* Uma **API Key** do Google Gemini

## 🔧 Instalação

1.  Clone este repositório:
    ```bash
    git clone [URL-DO-SEU-REPOSITORIO-AQUI]
    ```
2.  Navegue até o diretório do projeto:
    ```bash
    cd xmlreader-main
    ```
3.  Instale as dependências necessárias:
    ```bash
    pip install -r requirements.txt
    ```

## ▶️ Como Usar

### 1. Configuração da API Key (Google Gemini)

Antes de executar, você precisa de uma API Key do Google Gemini:

* Acesse o **[Google AI Studio](https://makersuite.google.com/app/apikey)** para gerar uma nova chave.
* Os modelos suportados pela aplicação são `Gemini-1.5-pro` e `Gemini-1.5-flash`.

### 2. Execução da Aplicação

1.  No seu terminal, execute a aplicação Streamlit:
    ```bash
    streamlit run app.py
    ```
2.  A aplicação será aberta no seu navegador. Na tela de boas-vindas, clique em "Entrar".
3.  Na tela de login, insira seu nome e a **API Key do Gemini** que você gerou.
4.  Na tela principal, faça o upload de um ou mais arquivos XML fiscais.
5.  Navegue pelas abas para visualizar os dados extraídos e executar a análise de conformidade com IA.
6.  Use as opções de exportação para baixar os resultados em Excel ou PDF.

## 📁 Estrutura do Projeto

```
caas-main/
├── app.py
├── criptografia.py
├── encryption.key
├── listar_modelos_gemini.py
├── README.md
├── requirements.txt
├── utils.py
├── .streamlit/
│   └── config.toml
├── agents/
│   ├── __init__.py
│   ├── analista.py
│   ├── orquestrador.py
│   ├── tributarista.py
│   └── validador.py
├── assets/
│   ├── banco_de_regras.json
│   └── LOGO.png
└── view/
    ├── login.py
    ├── main.py
    └── welcome.py
```

## 🛠️ Tecnologias Utilizadas

- **Streamlit**: Framework para aplicações web em Python
- **Pandas**: Manipulação e análise de dados
- **xml.etree.ElementTree**: Processamento de arquivos XML
- **Cryptography**: Criptografia de dados sensíveis
- **Google Generative AI**: Integração com Gemini.

## 📄 Licença

Este projeto está licenciado sob a Licença MIT.
