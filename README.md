# 🚀 SGA - Sistema de Gestão de Saúde Acadêmica

> **⚠️ Nota de Privacidade:** Este é um repositório de **Vitrine Tecnológica (Showcase)**. Devido a restrições de propriedade intelectual acadêmica (TCC) e proteção de dados reais de saúde (LGPD), o código-fonte original está mantido em um repositório privado. O objetivo desta página é demonstrar a arquitetura, a modelagem de banco de dados e as soluções de engenharia aplicadas no projeto.

---

## 🎯 O Problema e a Solução (Visão de Negócios)

**O Cenário:** O registro de atendimentos na clínica-escola era fragmentado e baseado em papel. Isso dificultava o rastreamento do histórico clínico dos pacientes, gerava risco de perda de informações sensíveis e atrasava o processo de avaliação dos alunos pelos professores preceptores.

**A Solução:** Desenvolvi uma aplicação web robusta que digitaliza e centraliza os prontuários clínicos. O sistema estabelece um fluxo de aprovação acadêmica seguro, garante a integridade dos dados de saúde e automatiza a geração de documentos oficiais, modernizando toda a operação administrativa e pedagógica da clínica.

---

## 💻 Stack Tecnológica e Arquitetura

Este projeto foi construído utilizando as seguintes tecnologias, focando em segurança, escalabilidade e manutenibilidade:

* **Back-End:** Python 3.x, Framework Django
* **Front-End:** HTML5, CSS3, JavaScript, Bootstrap 5 (UI/UX Responsiva)
* **Geração de Documentos:** Biblioteca `xhtml2pdf` para relatórios médicos
* **Banco de Dados:** SQLite (Ambiente de Desenvolvimento) / Preparado para migração PostgreSQL em Produção
* **Padrão de Arquitetura:** MVT (Model-View-Template) - Padrão do ecossistema Django
* **Controle de Versão:** Git & GitHub

---

## ⚙️ Principais Funcionalidades Desenvolvidas

* **Autenticação e Controle de Acesso:** Sistema de login com diferentes níveis de permissão (Alunos e Professores Avaliadores).
* **Gestão de Pacientes (CRUD):** Cadastro completo com dados demográficos, CNS (Cartão SUS) e histórico clínico centralizado.
* **Prontuário Eletrônico com Fluxo Pedagógico:** Registro de anamnese, sinais vitais e conduta com trava de segurança de status (Rascunho, Aguardando Validação, Corrigir e Aprovado). Prontuários aprovados são blindados contra edição.
* **Motor de Busca Dinâmico:** Pesquisa otimizada de pacientes por Nome, CPF ou Cartão SUS, com paginação de resultados.
* **Geração de Prontuários em PDF:** Exportação automatizada dos registros clínicos para formato A4 oficial da instituição, pronto para assinatura física e arquivamento legal.

---

## 🗄️ Modelagem do Banco de Dados (Engenharia de Dados)

A estrutura do banco de dados foi projetada seguindo as formas normais para evitar redundância e garantir a integridade referencial do prontuário do paciente.

*(Adicione aqui uma imagem do seu Diagrama de Entidade-Relacionamento - DER)*
![Diagrama do Banco de Dados](link-da-imagem-do-diagrama-aqui.jpg)

**Estruturas Principais:**
* **Tabela `Paciente`:** Armazena os dados demográficos. Possui relacionamento 1:N com a tabela de Prontuários (Um paciente possui vários registros clínicos ao longo do tempo).
* **Tabela `Prontuario`:** Coração do sistema. Aplica chaves estrangeiras (Foreign Keys) ligando o registro médico ao `Paciente`, ao `User` (Aluno que criou) e ao `User` (Professor que avaliou), garantindo a rastreabilidade total de quem fez o quê no sistema.

---

## 🖥️ Telas e Interface (UI/UX)

Abaixo estão capturas de tela do sistema em ambiente de produção/teste, demonstrando a usabilidade da aplicação e o foco na experiência do usuário (Clean Design).

### Ficha do Paciente e Histórico Clínico
![Ficha do Paciente]([link-do-print-aqui.jpg](https://github.com/esdr4sb0rges/docs-tcc-sistema-gestao/blob/557409a44f4d300fc3d834a0ecf756636d790569/Captura%20de%20tela%202026-03-19%20173442.png))

### Formulário de Prontuário Médico
*(Suba o print da tela onde o aluno preenche a anamnese e os sinais vitais)*
![Formulário de Prontuário](link-do-print-aqui.jpg)

### Documento Oficial Gerado (PDF)
![Prontuário em PDF](https://github.com/esdr4sb0rges/docs-tcc-sistema-gestao/blob/main/pdf_paciente.png?raw=true)

---

## 👨‍💻 Desenvolvedor e Arquiteto do Sistema

Desenvolvido e arquitetado por **Esdras Borges**.
* **Email:** esdrasbm16@gmail.com
* **Posicionamento:** Desenvolvedor Back-End & Consultor Estratégico, focado em criar soluções tecnológicas escaláveis que resolvem gargalos operacionais reais.
