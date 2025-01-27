# Entendendo GitHub Actions

## 🔹 Fundamentos do GitHub Actions

### O que é GitHub Actions? – Introdução e conceitos básicos.
   
   O GitHub Actions é uma plataforma de automação de fluxos de trabalho (CI/CD) integrada ao GitHub. Com ele, você pode criar scripts automatizados que são executados em resposta a eventos em seus repositórios, como pushes, pull requests, issues, entre outros.

   1. 1️⃣ Workflow (Fluxo de Trabalho)

      - É um conjunto de instruções que define uma automação.
      - Cada workflow é configurado em um arquivo YAML dentro do repositório (pasta .github/workflows/).
     
   2. 2️⃣ Eventos (Triggers)
      
      - São as ações que disparam um workflow, como:

        * push → Quando há um novo commit.
        * pull_request → Quando há uma nova PR aberta ou atualizada.
        * schedule → Execução programada (tipo um cron job).
        * workflow_dispatch → Execução manual.
          
   3. 3️⃣ Jobs (Tarefas)

      - Cada workflow contém jobs, que são conjuntos de etapas executados em um runner.
      - Um workflow pode ter vários jobs rodando paralelamente ou em sequência.
        
   4. 4️⃣ Steps (Passos)

      - São os comandos individuais dentro de um job.
      - Cada step pode executar comandos shell (run) ou utilizar uma action pronta (uses).

   5. 5️⃣ Actions

      - São scripts reutilizáveis que executam tarefas dentro dos steps.
      - Podem ser criadas do zero ou baixadas do GitHub Marketplace.
      - Exemplo: actions/checkout@v4 → Faz o checkout do código no repositório.
        
   6. 6️⃣ Runners

      - São as máquinas que executam os workflows.
      - O GitHub disponibiliza runners gratuitos na nuvem, mas também é possível configurar runners auto-hospedados.
     
   ## 🔹 Criação e Configuração de Workflows

   1. Criando um Workflow Básico – Exemplo prático de um arquivo .github/workflows/main.yml.
      exemplo prático de um arquivo GitHub Actions Workflow que será salvo em: 📂 .github/workflows/main.yml

   ### 📝 Arquivo main.yml

   ```
name: Meu Primeiro Workflow

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout do Código
        uses: actions/checkout@v4

      - name: Configurar Ambiente Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 18

      - name: Rodar Script de Teste
        run: echo "Hello, GitHub Actions!"
```

### 🔹 O que esse Workflow faz?
- ✅ Roda automaticamente quando há um push ou pull request na branch main.
- ✅ Faz o checkout do código do repositório.


   3. Ambientes e Contextos – Uso de variáveis, secrets e configurações.
   4. Usando Actions Prontas – Exploração do GitHub Marketplace.
   5. Escrevendo suas próprias Actions – Criando Docker-based e JavaScript Actions.
   6. Reutilização de Workflows – Estratégias para compartilhar código entre projetos.

      



      
