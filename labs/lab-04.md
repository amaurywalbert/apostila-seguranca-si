# 🔐 Laboratório Prático – Testes de Segurança em Aplicações (Cap. 14)


## 📌 Tema
Identificação e exploração controlada de vulnerabilidades em aplicações web utilizando ferramentas de análise (DAST) e técnicas básicas de *penetration testing*.

---

## 🎯 Objetivos do Laboratório

Ao final desta atividade, você será capaz de:

- Identificar vulnerabilidades reais em aplicações web  
- Utilizar ferramentas como OWASP ZAP e Burp Suite  
- Interceptar e analisar requisições HTTP  
- Explorar vulnerabilidades de forma controlada  
- Propor medidas de mitigação  
- Relacionar vulnerabilidades ao OWASP Top 10  

---

## 📚 Pré-requisitos

Antes de iniciar, você deve possuir:

- Conhecimentos básicos de HTTP:
  - Métodos (GET, POST)
  - Headers
  - Parâmetros de requisição
- Noções de aplicações web
- Ambiente virtual ou máquina isolada (recomendado)

---

## 🧪 Ambiente do Laboratório

Utilize uma das aplicações vulneráveis abaixo:

- OWASP Juice Shop  
- DVWA (Damn Vulnerable Web Application)

### 🔧 Sugestão de Setup (Docker)

```bash
docker run -d -p 3000:3000 bkimminich/juice-shop
```
id="3h9h2a"

Acesse: http://localhost:3000

---

⚠️ **Importante:**  
Essas aplicações são propositalmente vulneráveis.  
**Nunca execute esses testes em sistemas reais sem autorização.**

---

## 🧠 Cenário

Você foi contratado como analista de segurança para avaliar uma aplicação web antes de sua entrada em produção.

Seu objetivo é:

- Identificar vulnerabilidades críticas  
- Explorar possíveis falhas  
- Avaliar o impacto  
- Propor soluções  

---

# 🔍 Atividade 1 – Reconhecimento da Aplicação

## Objetivo
Mapear a superfície de ataque da aplicação.

## Passos

1. Acesse a aplicação no navegador  
2. Navegue pelas funcionalidades principais:

- Login  
- Cadastro  
- Busca  
- Carrinho  

3. Identifique:

- Campos de entrada (inputs)  
- URLs relevantes  
- Parâmetros manipuláveis  
- Funcionalidades sensíveis  

## 🔎 O que observar

- URLs com parâmetros (`?id=1`)  
- Formulários  
- APIs chamadas pelo frontend (DevTools → Network)  

## 📌 Perguntas

- Quais são os principais pontos de entrada?  
- Existe alguma funcionalidade crítica exposta?  

---

# 🕵️ Atividade 2 – Interceptação de Requisições

## Ferramenta
Burp Suite

## 🔧 Configuração

1. Abra o Burp Suite  
2. Vá em **Proxy → Options**  
3. Configure:

IP: 127.0.0.1
Porta: 8080


4. Configure o navegador para usar esse proxy  

## ▶️ Execução

1. Ative **Intercept ON**  
2. Realize uma ação (ex: login)  
3. Observe a requisição interceptada  

## 🔎 Analise

- Método HTTP (GET/POST)  
- Parâmetros enviados  
- Cookies (session, tokens)  
- Headers  

## 📌 Perguntas

- Dados sensíveis estão sendo enviados em texto claro?  
- Existe algum token previsível?  

---

# 💉 Atividade 3 – Teste de SQL Injection

## Objetivo
Explorar falha de validação de entrada.

## Entrada de teste
' OR '1'='1


## ▶️ Passos

1. Localize campo de login ou busca  
2. Insira o payload  
3. Envie a requisição  

## 🔎 Resultados esperados

- Login indevido  
- Retorno inesperado de dados  
- Erros de banco  

## 📌 Perguntas

- A aplicação validou a entrada?  
- Qual o impacto dessa vulnerabilidade?  

---

# ⚠️ Atividade 4 – Teste de XSS

## Objetivo
Verificar falha de sanitização de entrada.

## Entrada de teste

```html
<script>alert('XSS')</script>
``` id="j5h7nd"

## ▶️ Passos

1. Insira o código em campos de entrada  
2. Submeta o formulário  

## 🔎 Resultados esperados

- Execução do script  
- Pop-up no navegador  

## 📌 Perguntas

- O sistema sanitiza a entrada?  
- Qual o impacto para outros usuários?  

---

# 🤖 Atividade 5 – Varredura Automatizada (DAST)

## Ferramenta
OWASP ZAP

## ▶️ Passos

1. Inicie o ZAP  
2. Configure o proxy  
3. Acesse a aplicação via navegador  

### Execução

- Spider (mapear aplicação)  
- Active Scan (buscar vulnerabilidades)  

## 🔎 Resultados

- Lista de vulnerabilidades  
- Classificação por severidade  

## 📌 Perguntas

- Quais vulnerabilidades foram encontradas?  
- Elas correspondem ao OWASP Top 10?  

---

# 🧱 Atividade 6 – Análise Arquitetural

## Objetivo
Identificar falhas estruturais.

## 🔎 Avalie

- Separação de camadas  
- Exposição de endpoints  
- Validação de entrada  
- Configurações de segurança  

## 📌 Perguntas

- Existem APIs expostas sem autenticação?  
- O backend valida os dados corretamente?  

---

# 🛠️ Atividade 7 – Mitigações

## Objetivo
Propor soluções de segurança.

## Para cada vulnerabilidade, descreva:

- Correção técnica  
- Boa prática associada  
- Ferramenta de prevenção  

## Exemplos

- SQL Injection → Prepared Statements  
- XSS → Sanitização de entrada  
- Controle de acesso → RBAC  

---

# 📄 Entregáveis

Cada grupo deve entregar:

## 1. Relatório Técnico

- Vulnerabilidades encontradas  
- Evidências (prints/logs)  
- Classificação (OWASP Top 10)  
- Impacto  
- Mitigações  

## 2. Conclusão

- Nível de segurança da aplicação  
- Principais riscos identificados  

---

# ⚖️ Boas Práticas e Ética

⚠️ Este laboratório deve ser realizado apenas em ambientes controlados.

- Não testar sistemas reais sem autorização  
- Respeitar legislação vigente (ex: LGPD)  
- Seguir princípios éticos da segurança da informação  

---

# 🚀 Extensões (Opcional – Avançado)

- Testar IDOR (Broken Access Control)  
- Explorar autenticação fraca  
- Analisar tokens JWT  
- Simular ataque de força bruta  

---

# 💼 Conexão com o Mercado

Este laboratório simula atividades reais de:

- Analista de Segurança  
- Pentester  
- Engenheiro DevSecOps  

Ferramentas utilizadas são amplamente empregadas na indústria.

---

# ✔ Resultado Esperado

Ao final, o aluno deverá ser capaz de:

- Pensar como um atacante  
- Identificar vulnerabilidades reais  
- Utilizar ferramentas profissionais  
- Propor soluções de segurança  