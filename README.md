# ☕ AtendeAI — Assistente Virtual Inteligente

![Status](https://img.shields.io/badge/Status-Concluído-success)
![n8n](https://img.shields.io/badge/Automação-n8n-orange)
![IA](https://img.shields.io/badge/IA-Groq-blue)
![Projeto](https://img.shields.io/badge/Projeto-Portfólio-purple)

## 📌 Sobre o projeto

O **AtendeAI** é um protótipo de assistente virtual inteligente desenvolvido para automatizar o atendimento ao cliente de uma cafeteria fictícia chamada **Nuvem Café**.

O projeto utiliza Inteligência Artificial Generativa para interpretar mensagens dos clientes e produzir respostas naturais, considerando uma base de conhecimento previamente definida.

A proposta é demonstrar como ferramentas de automação e modelos de linguagem podem ser integrados para criar soluções de atendimento mais rápidas, organizadas e consistentes.

## 🎯 Objetivos

- Desenvolver um fluxo automatizado de atendimento.
- Integrar um modelo de Inteligência Artificial Generativa.
- Utilizar uma base de conhecimento para orientar as respostas.
- Reduzir respostas inventadas pela IA.
- Tratar dúvidas, reclamações e solicitações dos clientes.
- Aplicar conceitos de integração de APIs e automação de processos.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| n8n | Construção e automação do workflow |
| Groq API | Integração com modelo de IA |
| OpenAI GPT-OSS 120B | Modelo de linguagem utilizado |
| JSON | Estruturação e transferência de dados |
| HTTP Request | Comunicação com a API |
| Webhook | Recebimento das mensagens |
| Postman | Testes das requisições |

## ⚙️ Arquitetura do projeto

O fluxo foi desenvolvido no n8n e organizado nas seguintes etapas:

1. **Webhook:** recebe a mensagem enviada pelo cliente.
2. **Edit Fields:** organiza os dados recebidos.
3. **Base de Conhecimento:** disponibiliza as informações conhecidas da loja.
4. **Preparar Mensagem:** combina a pergunta do cliente com o contexto da loja.
5. **HTTP Request:** envia a solicitação à API da Groq.
6. **Respond to Webhook:** retorna a resposta gerada pela IA.

## 🧠 Base de conhecimento

O assistente utiliza uma estrutura JSON para armazenar informações da cafeteria, como:

- Horários de funcionamento.
- Produtos.
- Preços.
- Canais de contato.
- Política de troca.
- Política de reembolso.

Informações não cadastradas não devem ser inventadas pelo assistente.

## 🧪 Testes realizados

Foram realizados cinco testes funcionais:

| Teste | Cenário | Resultado |
|---|---|---|
| T01 | Consulta sobre funcionamento aos sábados | Aprovado |
| T02 | Consulta sobre produtos e preços indisponíveis | Aprovado |
| T03 | Reclamação sobre pedido incorreto | Aprovado |
| T04 | Solicitação de WhatsApp não cadastrado | Aprovado |
| T05 | Tentativa de induzir a IA a inventar preços | Aprovado |

**Resultado: 5 de 5 testes aprovados.**

## 🔒 Cuidados e regras de comportamento

O assistente foi configurado para:

- Não inventar preços, produtos ou informações.
- Utilizar somente os dados disponíveis na base de conhecimento.
- Manter comunicação educada e objetiva.
- Demonstrar empatia em situações de reclamação.
- Não afirmar que realizou ações que não foram implementadas.

## ⚠️ Limitações atuais

Este projeto é um protótipo funcional para demonstração.

Atualmente, não possui:
- Integração com WhatsApp.
- Consulta real de pedidos.
- Encaminhamento automático para atendentes.
- Banco de dados persistente para histórico de conversas.
- Processamento real de reembolsos ou trocas.

## 🚀 Possíveis melhorias futuras

- Integrar WhatsApp Business.
- Criar um painel administrativo.
- Implementar histórico de conversas.
- Adicionar banco de dados.
- Criar encaminhamento real para atendimento humano.
- Expandir a base de conhecimento.
- Implementar métricas de atendimento.

## 📂 Estrutura do repositório

```text
AtendeAI/
├── documentacao/
├── evidencias/
│   └── AtendeAI.xlsx
├── Workflow/
│   └── AtendeAI.json
├── base_conhecimento.json
├── Doc-AtendeAI.docx
└── README.md
```

## 📚 Aprendizados

Durante o desenvolvimento, foram praticados conceitos de:

- Inteligência Artificial Generativa.
- Engenharia de prompts.
- Automação de workflows.
- Integração de APIs REST.
- Requisições HTTP.
- Manipulação de dados JSON.
- Testes funcionais.
- Segurança no armazenamento de credenciais.

---

**Desenvolvido como projeto de portfólio para demonstrar conhecimentos em Inteligência Artificial Generativa, automação e integração de APIs.**