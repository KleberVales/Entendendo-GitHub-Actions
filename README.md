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
      Um workflow pode ter vários jobs rodando paralelamente ou em sequência.
