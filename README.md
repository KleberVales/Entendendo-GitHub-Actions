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
   2. Ambientes e Contextos – Uso de variáveis, secrets e configurações.
   3. Usando Actions Prontas – Exploração do GitHub Marketplace.
   4. Escrevendo suas próprias Actions – Criando Docker-based e JavaScript Actions.

      



      
