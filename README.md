# 🛡️ Hardening e Proteção de Perímetro com IA Generativa

Este repositório contém o projeto prático desenvolvido para o desafio da **DIO**, focado no uso da Inteligência Artificial como ferramenta de aprendizado ativo. Aqui, explorei a aplicação de técnicas de **Hardening** e segurança de infraestrutura utilizando o **NotebookLM**.

## 🎯 Contexto e Objetivos
Como profissional de TI e entusiasta de Cibersegurança (FIAP), meu objetivo foi criar um caderno de estudos que unisse a teoria da gestão de infraestrutura com a prática de defesa cibernética.
* **Objetivo:** Consolidar procedimentos de segurança para servidores Windows/Linux e entender como a IA pode acelerar a triagem de vulnerabilidades.

## 📚 Curadoria de Fontes
Para garantir a precisão técnica, utilizei o NotebookLM alimentado pelas seguintes fontes:
1. **NIST SP 800-123**: Guia de Segurança para Servidores de Propósito Geral.
2. **CIS Benchmarks**: Padrões da indústria para configurações seguras.
3. **OWASP Infrastructure Guide**: Focado em mitigar ataques de rede.

## 🧠 Engenharia de Prompts e "Cicatrizes"
O uso da IA exigiu um processo de refinamento constante para evitar respostas genéricas.

### Estratégia de Prompting
* **Prompt 1 (Iniciante):** "Como proteger um servidor de TI?" (Resposta muito ampla).
* **Prompt 2 (Especialista):** "Com base no guia NIST, liste os 5 principais serviços que devem ser desabilitados em um Windows Server 2022 para reduzir a superfície de ataque e forneça os comandos PowerShell correspondentes."

### Cicatrizes (Troubleshooting)
* **Dificuldade:** Inicialmente, a IA sugeriu o uso de protocolos antigos por erro de interpretação de contexto. 
* **Correção:** Forcei o modelo a validar as informações cruzando os dados do PDF do CIS Benchmark, o que corrigiu a sugestão para os padrões atuais de segurança (TLS 1.3).

## 📖 Miniguia de Estudo (Entrega Final)

### 🚀 Laboratório Prático de Hardening

#### 1. Segurança em Windows (PowerShell)
Comando para desabilitar o SMBv1, prevenindo ataques de movimentação lateral:
```powershell
Disable-WindowsOptionalFeature -Online -FeatureName SMB1Protocol -Language en-US
