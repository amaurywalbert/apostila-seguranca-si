🔐 Laboratório Prático – Testes de Segurança em Aplicações (Cap. 14)
📌 Tema
Identificação e exploração controlada de vulnerabilidades em aplicações web utilizando ferramentas de análise (DAST) e técnicas básicas de pentest.
---
🎯 Objetivos do Laboratório
Ao final desta atividade, você será capaz de:
Identificar vulnerabilidades reais em aplicações web
Utilizar ferramentas como OWASP ZAP e Burp Suite
Explorar vulnerabilidades de forma controlada
Propor medidas de mitigação
Relacionar vulnerabilidades ao OWASP Top 10
---
📚 Pré-requisitos
Conhecimentos básicos de HTTP (GET/POST, headers)
Noções de aplicações web
Ambiente virtual ou controlado
---
🧪 Ambiente do Laboratório
Recomenda-se utilizar aplicações vulneráveis intencionais:
OWASP Juice Shop
DVWA (Damn Vulnerable Web Application)
⚠️ Essas aplicações são projetadas para fins educacionais.
---
🧠 Cenário
Você foi contratado como analista de segurança para avaliar uma aplicação web antes de sua entrada em produção. Seu objetivo é identificar vulnerabilidades críticas.
---
🔍 Atividade 1 – Reconhecimento da Aplicação
Passos
Acesse a aplicação (Juice Shop ou DVWA)
Navegue pelas funcionalidades:
Login
Cadastro
Busca
Carrinho
Identifique:
Campos de entrada
URLs relevantes
Parâmetros manipuláveis
---
🕵️ Atividade 2 – Interceptação de Requisições
Ferramenta: Burp Suite
Passos
Configure o proxy: 127.0.0.1:8080
Ative o intercept
Realize um login
Analise:
Método HTTP
Parâmetros
Cookies
---
💉 Atividade 3 – SQL Injection
Entrada de teste
' OR '1'='1
---
⚠️ Atividade 4 – XSS
Entrada de teste
<script>alert('XSS')</script>
---
🤖 Atividade 5 – Varredura Automatizada (DAST)
Ferramenta: OWASP ZAP
---
🧱 Atividade 6 – Análise Arquitetural
Identifique falhas estruturais da aplicação.
---
🛠️ Atividade 7 – Mitigações
Descreva correções e boas práticas.
---
📄 Entregáveis
Relatório técnico com vulnerabilidades, evidências, impacto e mitigação.
---
⚖️ Ética
Utilizar apenas ambientes controlados.