# agente-cadastro-clinica

Agente de IA que conduz o cadastro de pacientes e o registro do resultado de exame em conversa, estrutura os dados e grava tudo em planilha, sem digitação manual pela equipe. Desenvolvido para uma clínica oftalmológica parceira e publicado aqui em versão sanitizada.

## Problema

O cadastro era feito no papel e redigitado depois. Isso gerava fila no balcão, erro de transcrição no grau e histórico do paciente espalhado entre cadernos e planilhas soltas.

## Como funciona

**1. Coleta.** O agente conduz a conversa e pede os dados de cadastro um a um, confirmando o que entendeu.

**2. Estruturação.** A resposta livre é convertida em JSON com campos fixos, inclusive os valores do exame.

**3. Validação.** Campos fora do formato esperado voltam para confirmação antes de seguir.

**4. Gravação.** O registro vai para a planilha da clínica, com data e origem do atendimento.

## Stack

n8n · LLM · Google Sheets · WhatsApp Business API

## Dados pessoais

O fluxo trata dado de paciente, então nada de real é versionado aqui. O repositório contém apenas a estrutura do agente, o schema dos campos e exemplos fictícios. Credenciais ficam em variáveis de ambiente.

## Como usar

Importe `workflow.json` no n8n, copie `.env.example` para `.env` e preencha as credenciais.
