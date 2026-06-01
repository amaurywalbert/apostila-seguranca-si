# Lista de Exercícios: Módulo 04 – Desenvolvimento Seguro, Vulnerabilidades e Testes de Segurança

Esta lista contempla os temas abordados nos capítulos 12, 13 e 14, incluindo desenvolvimento seguro de software, análise de vulnerabilidades e testes de segurança em aplicações.

---

## Questões Teóricas e Conceituais

### 1. Segurança no Desenvolvimento de Software
Explique por que a segurança deve ser integrada ao ciclo de vida do software (SDLC). Quais problemas podem surgir quando essa abordagem não é adotada?

---

### 2. Secure SDLC
Defina o conceito de Secure SDLC e descreva como ele contribui para a redução de vulnerabilidades em aplicações.

---

### 3. Security by Design
Explique o conceito de *Security by Design* e discuta sua relação com falhas arquiteturais em sistemas.

---

### 4. Superfície de Ataque
Defina o conceito de superfície de ataque e explique como arquiteturas modernas (APIs, microserviços e cloud) influenciam esse aspecto.

---

### 5. Vulnerabilidades em Aplicações
Explique o conceito de vulnerabilidade em aplicações e sua relação com ameaça e risco. Utilize a expressão:

Risco = Ameaça × Vulnerabilidade × Impacto

---

### 6. Classificação de Vulnerabilidades
Descreva as principais categorias de vulnerabilidades:

- Validação de entrada  
- Configuração  
- Controle de acesso  
- Criptografia  
- Sessão/autenticação  

---

### 7. OWASP Top 10
Explique o objetivo do OWASP Top 10 e sua importância para o desenvolvimento seguro. Qual mudança importante ocorreu nas versões mais recentes?

---

### 8. Testes de Segurança
Explique a diferença entre testes funcionais e testes de segurança. Por que ambos são necessários?

---

### 9. SAST vs DAST
Explique as diferenças entre SAST e DAST, destacando:

- Momento de uso  
- Tipo de análise  
- Vantagens e limitações  

---

### 10. Pentest
Descreva o que é um teste de invasão (pentest) e explique por que ele é importante na avaliação de segurança.

---

## Questões de Análise e Casos Reais

### 11. Análise de Código Vulnerável (SQL Injection)

Considere o seguinte código:
query = "SELECT * FROM usuarios WHERE login = '" + login + "' AND senha = '" + senha + "'"

*   Qual vulnerabilidade está presente?
*   Explique como ela pode ser explorada.
*   Proponha uma solução segura.

---

### 12. Falhas de Controle de Acesso

Considere o cenário:
/api/user?id=100


Um usuário altera o parâmetro para acessar dados de outro usuário.

*   Qual vulnerabilidade está presente?
*   A qual categoria do OWASP ela pertence?
*   Qual o impacto?

---

### 13. Configuração Insegura

Uma aplicação apresenta:

- Credenciais padrão  
- Serviços desnecessários ativos  
- Mensagens de erro detalhadas  

*   Identifique os riscos envolvidos.
*   Explique como essas falhas podem ser exploradas.
*   Proponha medidas de mitigação.

---

### 14. Cadeia de Suprimentos

Explique como vulnerabilidades em bibliotecas de terceiros podem comprometer aplicações. Relacione com um exemplo real (ex: Log4Shell).

---

### 15. Falhas Arquiteturais

Uma aplicação apresenta:

- Validação apenas no frontend  
- APIs expostas sem autenticação  
- Dados transmitidos sem criptografia  

*   Identifique as falhas.
*   Relacione com princípios de segurança violados.
*   Proponha melhorias.

---

### 16. SAST e DAST na Prática

Uma equipe utiliza apenas DAST em seus testes.

*   Quais riscos essa decisão pode trazer?
*   Quais vulnerabilidades podem não ser detectadas?
*   Como melhorar o processo?

---

### 17. Pentest e Limitações

Explique por que o pentest não deve ser a única técnica de avaliação de segurança. Quais são suas limitações?

---

### 18. Análise de Logs e Monitoramento

Explique a importância de logs e monitoramento na segurança de aplicações.

*   O que pode acontecer se esses mecanismos não existirem?
*   Relacione com OWASP Top 10.

---

### 19. SSRF em Ambientes Cloud

Descreva como funciona um ataque SSRF.

*   Por que ele é especialmente perigoso em ambientes de nuvem?
*   Quais recursos podem ser comprometidos?

---

### 20. Análise Integrada de Segurança

Considere um sistema com:

- API pública  
- Banco de dados  
- Autenticação simples (login/senha)  

Elabore uma análise contendo:

*   Principais ameaças  
*   Possíveis vulnerabilidades  
*   Tipos de testes recomendados (SAST, DAST, Pentest)  
*   Controles de segurança sugeridos  

---

### 21. Cenário Completo de Ataque

Considere um sistema com:

- Falta de validação de entrada  
- Ausência de controle de acesso  
- Logs inexistentes  

Descreva:

*   Como um atacante poderia explorar o sistema  
*   Etapas do ataque  
*   Impacto final  

---

## Questão Desafio (Nível Avançado)

### 22. Integração de Segurança no Desenvolvimento

Você é responsável por implantar segurança em um projeto de software.

Descreva um plano contendo:

*   Uso de Secure SDLC  
*   Aplicação de Security by Design  
*   Uso de ferramentas (SAST, DAST)  
*   Estratégia de pentest  
*   Monitoramento contínuo  

---

**Instruções:**
*   As respostas devem ser fundamentadas nos capítulos 12, 13 e 14.
*   Utilize exemplos práticos sempre que possível.
*   Em questões analíticas, justifique suas respostas de forma clara e estruturada.