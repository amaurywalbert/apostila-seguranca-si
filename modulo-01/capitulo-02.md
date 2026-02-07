# Capítulo 2 – Princípios e Propriedades de Segurança da Informação

## Objetivos do Capítulo
Ao final deste capítulo, o estudante será capaz de:
*   Compreender as propriedades fundamentais da Segurança da Informação;
*   Diferenciar princípios, propriedades e mecanismos de segurança;
*   Analisar conflitos e trade-offs entre confidencialidade, integridade e disponibilidade;
*   Relacionar princípios clássicos de segurança com sistemas reais;
*   Aplicar esses conceitos na análise de cenários práticos de segurança.

## Competências Desenvolvidas (DCNs / ENADE)
*   Identificar requisitos de segurança em Sistemas de Informação;
*   Avaliar riscos associados a falhas de segurança;
*   Aplicar princípios de segurança no projeto de sistemas computacionais;
*   Analisar incidentes sob a ótica da Tríade CID.

---

## 2.1 Introdução

A Segurança da Informação não se resume ao uso de ferramentas isoladas, como criptografia, antivírus ou firewalls. Esses mecanismos são meios, não fundamentos. A base da segurança está em propriedades conceituais e princípios clássicos que orientam o projeto, a implementação e a operação de sistemas computacionais seguros.

Sem o domínio desses fundamentos, é comum que organizações:
*   Adotem tecnologias inadequadas;
*   Implementem controles inconsistentes;
*   Criem uma falsa sensação de segurança;
*   Falhem em responder adequadamente a incidentes.

> 📌 **Visão central do capítulo:**
> Este capítulo estabelece a base conceitual obrigatória para todos os mecanismos técnicos estudados nos capítulos seguintes (criptografia, controle de acesso, redes, aplicações, SIEM, etc.).

---

## 2.2 A Tríade da Segurança da Informação (CID)

As propriedades fundamentais da Segurança da Informação são tradicionalmente representadas pela **Tríade CID**:
*   **Confidencialidade** (Confidentiality)
*   **Integridade** (Integrity)
*   **Disponibilidade** (Availability)

Esses três pilares servem como modelo mental para análise de riscos, incidentes e decisões de projeto.

### 2.2.1 Confidencialidade
A confidencialidade garante que a informação seja acessível apenas a entidades autorizadas, impedindo vazamentos, espionagem ou acesso indevido.

**Mecanismos comuns:**
*   Criptografia (dados em repouso e em trânsito);
*   Controle de acesso (autenticação e autorização);
*   Políticas de classificação da informação;
*   Segmentação de redes e isolamento de ambientes.

> 📌 **Exemplo real:**
> Em 2023, o vazamento de dados do INSS expôs informações pessoais de beneficiários. Embora os sistemas estivessem funcionando normalmente, a confidencialidade foi violada, caracterizando grave falha de segurança.

### 2.2.2 Integridade
A integridade assegura que a informação não seja alterada de forma indevida, seja por erro humano, falha de sistema ou ação maliciosa. Envolve a **correção dos dados** e a **confiabilidade da origem**.

**Mecanismos comuns:**
*   Funções de hash criptográficas (SHA-256, SHA-3);
*   Assinaturas digitais;
*   Controle de versões e logs de auditoria.

> 📌 **Exemplo real:**
> Fraudes em sistemas bancários frequentemente não envolvem vazamento de dados, mas alteração de valores. Nesses casos, a confidencialidade pode permanecer intacta, enquanto a integridade é comprometida.

### 2.2.3 Disponibilidade
A disponibilidade garante que sistemas e informações estejam acessíveis quando necessários aos usuários autorizados.

**Mecanismos comuns:**
*   Redundância de servidores e links;
*   Balanceamento de carga;
*   Backups e planos de recuperação de desastres;
*   Proteção contra ataques DoS/DDoS.

> 📌 **Exemplo real:**
> Em setembro de 2024, ataques DDoS motivados por razões políticas derrubaram sites de órgãos públicos brasileiros, incluindo o Tribunal de Contas da União (TCU), tornando serviços online essenciais temporariamente indisponíveis.

| Box – Atenção ENADE |
| :--- |
| Questões do ENADE frequentemente exploram cenários híbridos. Exemplo clássico: um ataque de **ransomware** compromete a **Disponibilidade** (dados inacessíveis) e a **Integridade** (dados alterados/cifrados). |

---

## 2.3 Propriedades Complementares de Segurança

### 2.3.1 Autenticidade
Garante que uma entidade (usuário, sistema ou serviço) é realmente quem afirma ser.
*   **Mecanismos:** Certificados digitais, autenticação multifator (MFA), tokens criptográficos.

### 2.3.2 Não Repúdio (Irretratabilidade)
Assegura que uma entidade não possa negar uma ação realizada. Essencial em contextos legais e financeiros.
*   **Exemplo:** Assinaturas digitais realizadas com certificados da ICP-Brasil possuem validade jurídica no Brasil (Lei nº 14.063/2020).

---

## 2.4 Princípios Clássicos de Segurança

### 2.4.1 Princípio do Privilégio Mínimo
Cada usuário ou processo deve possuir apenas os privilégios estritamente necessários.
> 📌 **Exemplo real:** Em 2025, um vazamento massivo de credenciais teve seu impacto ampliado porque aplicações internas rodavam com permissões administrativas padrão, permitindo a extração de dados sem restrição.

### 2.4.2 Princípio da Separação de Privilégios
O acesso a recursos críticos deve exigir mais de uma condição ou autorização (ex: aprovação dupla para transferências).

### 2.4.3 Princípio da Mediação Completa
Todo acesso a recursos deve ser verificado continuamente pelos mecanismos de segurança, sem exceções.

### 2.4.4 Princípio do Default Seguro
Se um acesso não estiver explicitamente permitido, ele deve ser negado por padrão ("Negar por padrão").

### 2.4.5 Princípio do Projeto Aberto
A segurança não deve depender do sigilo do algoritmo, mas da robustez do projeto e do segredo das chaves (Princípio de Kerckhoffs).

| Box – Erro Comum |
| :--- |
| Conceder privilégios excessivos “por conveniência” é uma das principais causas de falhas graves em segurança da informação. |

---

## 2.5 Conflitos e Trade-offs entre Segurança e Usabilidade

Na prática, as propriedades de segurança entram em conflito:
*   **Mais segurança** → menor usabilidade;
*   **Mais disponibilidade** → maior superfície de ataque;
*   **Mais controles** → maior custo operacional.

> 📌 Um bom projeto de segurança busca equilíbrio, não a maximização isolada de um único pilar.

---

## 2.6 Segurança Física, Lógica e Administrativa

*   **Segurança Física:** Controle de acesso a ambientes, datacenters, câmeras.
*   **Segurança Lógica:** Mecanismos técnicos (software, hardware, criptografia).
*   **Segurança Administrativa:** Políticas, normas, procedimentos e treinamentos.

> 📌 **Fato crítico:** Falhas administrativas frequentemente anulam controles técnicos robustos.

---

## 2.7 Relação entre Segurança, Risco e Continuidade

A Segurança da Informação está diretamente ligada à gestão de riscos:
**Risco = Ameaça × Vulnerabilidade × Impacto**

A mitigação envolve: **Prevenção**, **Detecção**, **Resposta** e **Recuperação**.

---

## Resumo do Capítulo
*   A Tríade CID define as propriedades fundamentais;
*   Propriedades complementares ampliam confiança e rastreabilidade;
*   Princípios clássicos orientam decisões técnicas e organizacionais;
*   Segurança envolve trade-offs e deve ser tratada de forma sistêmica.

---

## Referências e Leituras Complementares
*   [Vazamento de dados do INSS (G1)](https://g1.globo.com/economia/noticia/2024/06/24/inss-confirma-indicios-de-que-informacoes-de-beneficiarios-foram-expostas-em-vazamento.ghtml)
*   [Ataques DDoS contra Órgãos Públicos Brasileiros](https://safelabs.com.br/relatorio-de-seguranca-ataques-ddos-contra-orgaos-publicos-brasileiros)
*   [Brasil sofreu mais de 500 mil ataques DDoS em 2025](https://www.tecmundo.com.br/seguranca/406655-brasil-sofreu-mais-de-500-mil-ataques-ddos-na-primeira-metade-de-2025.htm)
*   STALLINGS, W.; BROWN, L. Computer Security: Principles and Practice.
*   SÊMOLA, M. Gestão da Segurança da Informação.
