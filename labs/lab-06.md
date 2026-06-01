# 🔐 Laboratório Prático – Análise de Riscos em Sistemas de Informação

## 📌 Tema

Identificação, análise e avaliação de riscos em sistemas de informação por meio da construção de uma matriz de risco baseada em ativos, vulnerabilidades, ameaças, impactos e controles de mitigação.

---

# 🎯 Objetivos do Laboratório

Ao final desta atividade, você será capaz de:

* Identificar ativos críticos em sistemas de informação;
* Reconhecer vulnerabilidades e ameaças relevantes;
* Avaliar probabilidade e impacto de riscos;
* Construir uma matriz de risco;
* Propor controles de mitigação adequados;
* Relacionar a gestão de riscos aos conceitos de SGSI, ISO 27005 e Governança de Segurança.

---

# 📚 Pré-requisitos

Antes de iniciar esta atividade, recomenda-se que o estudante tenha estudado os seguintes tópicos:

* Tríade CID (Confidencialidade, Integridade e Disponibilidade);
* Gestão de Segurança da Informação;
* Gestão de Riscos;
* Vulnerabilidades em Sistemas;
* Conceitos básicos da ISO/IEC 27001 e ISO/IEC 27005.

---

# 👥 Formação das Equipes

Esta atividade deverá ser realizada em equipes de até **4 integrantes**.

---

# 🧠 Cenário

Você faz parte da equipe de Segurança da Informação de uma organização que está implantando um novo sistema.

Antes da entrada em produção, a direção da empresa solicitou uma análise preliminar de riscos para identificar possíveis vulnerabilidades, ameaças e impactos que possam comprometer a operação do negócio.

Seu papel será atuar como analista de segurança e elaborar uma matriz de risco contendo os principais riscos identificados e suas respectivas medidas de mitigação.

---

# 💻 Etapa 1 – Escolha do Sistema

Cada equipe deverá escolher um sistema para análise.

O sistema pode ser:

* Real;
* Hipotético;
* Acadêmico;
* Desenvolvido em outra disciplina.

## Sugestões

* Sistema Bancário;
* Loja Virtual (E-commerce);
* Sistema Acadêmico;
* Sistema Hospitalar;
* Aplicativo de Delivery;
* Sistema de Biblioteca;
* API REST de Autenticação;
* Sistema de Controle de Estoque;
* Rede Corporativa;
* Sistema de Votação Online.

---

# 📝 Etapa 2 – Descrição do Sistema

Descreva brevemente o sistema escolhido.

A descrição deve conter:

* Objetivo do sistema;
* Principais funcionalidades;
* Dados armazenados;
* Usuários envolvidos;
* Infraestrutura utilizada.

## Exemplo

Um sistema de comércio eletrônico possui:

* Cadastro de clientes;
* Autenticação de usuários;
* Processamento de pedidos;
* Integração com pagamentos;
* Banco de dados contendo informações pessoais e histórico de compras.

---

# 🏢 Etapa 3 – Identificação dos Ativos

Identifique os principais ativos que precisam ser protegidos.

## Exemplos de Ativos

| Categoria      | Exemplos                   |
| -------------- | -------------------------- |
| Dados          | CPF, senhas, cartões       |
| Infraestrutura | Servidores, banco de dados |
| Software       | Backend, frontend, APIs    |
| Pessoas        | Usuários e administradores |
| Serviços       | Autenticação, pagamentos   |

---

# 🔍 Etapa 4 – Identificação de Vulnerabilidades

Analise o sistema e identifique possíveis vulnerabilidades.

## Exemplos

* Senhas fracas;
* SQL Injection;
* Cross-Site Scripting (XSS);
* Falta de backups;
* Ausência de autenticação multifator;
* Servidores desatualizados;
* Controle de acesso inadequado;
* Falta de criptografia;
* Configurações inseguras;
* Falhas de monitoramento.

---

# ⚠️ Etapa 5 – Identificação de Ameaças

Para cada vulnerabilidade identificada, descreva quais ameaças podem explorá-la.

## Exemplos

| Vulnerabilidade       | Ameaça                                    |
| --------------------- | ----------------------------------------- |
| Senha fraca           | Força bruta                               |
| SQL Injection         | Roubo de dados                            |
| Sem backup            | Ransomware                                |
| Sem MFA               | Credential Stuffing                       |
| Sistema desatualizado | Exploração de vulnerabilidades conhecidas |

---

# 📊 Etapa 6 – Avaliação de Impacto e Probabilidade

Avalie cada risco considerando:

## Probabilidade

Chance de ocorrência do evento.

## Impacto

Consequências para a organização caso o evento ocorra.

### Escala Sugerida

| Nível | Valor |
| ----- | ----- |
| Baixo | 1     |
| Médio | 2     |
| Alto  | 3     |

---

# 🧮 Etapa 7 – Construção da Matriz de Risco

Calcule o nível de risco utilizando:

```text
Risco = Probabilidade × Impacto
```

## Classificação Sugerida

| Resultado | Classificação |
| --------- | ------------- |
| 1 – 3     | Baixo         |
| 4 – 6     | Médio         |
| 7 – 9     | Alto          |

---

## Modelo de Matriz de Risco

| Ativo          | Vulnerabilidade | Ameaça         | Probabilidade | Impacto | Risco | Mitigação           |
| -------------- | --------------- | -------------- | ------------- | ------- | ----- | ------------------- |
| Banco de Dados | SQL Injection   | Roubo de dados | 3             | 3       | 9     | Prepared Statements |
| Login          | Senha fraca     | Força bruta    | 3             | 2       | 6     | MFA e Rate Limiting |
| Servidor       | Sem Backup      | Ransomware     | 2             | 3       | 6     | Política de Backup  |

---

# 🛡️ Etapa 8 – Propostas de Mitigação

Para cada risco identificado, proponha medidas de tratamento.

As medidas podem envolver:

## Controles Técnicos

Exemplos:

* Firewall;
* Criptografia;
* MFA;
* Backup;
* Atualização de sistemas.

---

## Controles Administrativos

Exemplos:

* Políticas de segurança;
* Treinamentos;
* Procedimentos operacionais;
* Gestão de fornecedores.

---

## Melhorias de Processo

Exemplos:

* Gestão de vulnerabilidades;
* Gestão de mudanças;
* Monitoramento contínuo;
* Auditorias periódicas.

---

# 📌 Exemplos de Mitigação

| Problema               | Mitigação                 |
| ---------------------- | ------------------------- |
| SQL Injection          | Prepared Statements       |
| Phishing               | Treinamento e MFA         |
| Servidor desatualizado | Gestão de patches         |
| Falta de backup        | Política de backup        |
| Senhas fracas          | Política de senhas fortes |

---

# 🔎 Etapa 9 – Análise dos Resultados

Após concluir a matriz, responda:

1. Quais riscos apresentaram maior criticidade?
2. Quais ativos são mais importantes para o negócio?
3. Existem riscos que poderiam ser aceitos?
4. Quais controles possuem melhor custo-benefício?
5. Como a organização poderia melhorar sua maturidade em segurança?

---

# 📄 Entregáveis

## 1. Matriz de Risco

A equipe deverá entregar uma matriz contendo:

* Descrição do sistema;
* Ativos identificados;
* Vulnerabilidades;
* Ameaças;
* Probabilidade;
* Impacto;
* Nível de risco;
* Mitigações propostas.

---

## 2. Relatório Simplificado

Máximo de 3 páginas contendo:

* Introdução;
* Descrição do sistema;
* Principais riscos;
* Matriz de risco;
* Conclusões.

---

## 3. Apresentação (Opcional)

Caso solicitado pelo professor:

* Máximo de 5 slides;
* Apresentação de até 10 minutos.

---

# 💡 Dicas para Desenvolvimento

* Escolha um sistema simples de compreender;
* Utilize vulnerabilidades estudadas em aula;
* Considere impactos financeiros, operacionais e reputacionais;
* Evite listar riscos sem justificativa;
* Priorize qualidade da análise em vez da quantidade.

---

# ⚠️ Atenção

Nem toda vulnerabilidade gera o mesmo impacto.

Da mesma forma, nem todo risco precisa necessariamente ser eliminado.

Em muitos cenários organizacionais, riscos podem ser:

* Mitigados;
* Transferidos;
* Aceitos;
* Evitados.

O papel da gestão de riscos é apoiar decisões conscientes e alinhadas aos objetivos do negócio.

---

# 🧠 Reflexão Final

A gestão de riscos é um dos pilares da Segurança da Informação moderna. Organizações não conseguem eliminar completamente todas as ameaças, mas podem identificar, avaliar e tratar riscos de forma sistemática.

A construção de uma matriz de risco permite transformar problemas abstratos em decisões concretas, auxiliando gestores e profissionais de segurança a direcionarem recursos para aquilo que realmente importa.
