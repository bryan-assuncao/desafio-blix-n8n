---

# Desafio Blix - Automação n8n

Este é um workflow simples criado no n8n para automatizar o recebimento de dados de um formulário.

O objetivo é capturar as informações, organizá-las em diferentes plataformas (Google Sheets e Trello) e notificar um responsável por e-mail.

* **Vídeo (Demonstração):**
    [Link](https://youtu.be/F94dCV6dcA4)
  
* **Formulário (Google Forms):**
    [Link](https://docs.google.com/forms/d/e/1FAIpQLSfNNvwrKnl7xtZceSy2jPgQM-A4eGoFoxmiUzC_9tYDsxsNZA/viewform)

  

## 🚀 Como Funciona o Workflow

O fluxo é disparado assim que um formulário é enviado e segue estes passos:

1.  **Webhook (Gatilho):**
    * O workflow começa com um Webhook que fica "ouvindo" (esperando) por dados enviados via `POST`. Assim que o formulário é preenchido, os dados chegam aqui.

2.  **Google Sheets (Append row in sheet):**
    * Os dados recebidos (Nome, E-mail, Telefone, Assunto, etc.) são automaticamente adicionados como uma nova linha em uma planilha do Google Sheets.

3.  **Trello (Criar Card):**
    * Usando os mesmos dados, um novo card é criado em um quadro específico do Trello. A descrição do card é formatada para incluir todos os detalhes do formulário, facilitando a visualização.

4.  **Gmail (Send a message):**
    * Por fim, um e-mail de notificação (formatado em HTML) é enviado para o administrador, avisando que um novo formulário foi preenchido, incluindo o nome da pessoa e a data.

## 🔗 Links Úteis

Aqui estão os links para as ferramentas usadas nesta automação:

* **Google Sheets (Planilha):**
    [Link](https://docs.google.com/spreadsheets/d/1TMy2Y554RelTQXhDr8h8dBLrhCCKu3kIdWxjGqdySgU/edit?usp=sharing)

* **Trello (Quadro):**
    [Link](https://trello.com/invite/b/69027a3d56a8b7ea7305d9c9/ATTI6b166072b44f8080d95fb1f7bf8f0a679997350C/blix)
