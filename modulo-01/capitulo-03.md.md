# Capítulo 3 – Ameaças, Vulnerabilidades e Ataques

## Objetivos do Capítulo
Ao final deste capítulo, o estudante será capaz de:
*   Compreender os conceitos fundamentais de ameaça, vulnerabilidade, ataque e risco;
*   Diferenciar ameaças internas e externas aos Sistemas de Informação;
*   Classificar vulnerabilidades quanto à sua origem e impacto;
*   Reconhecer os principais tipos de ataques em ambientes computacionais;
*   Analisar incidentes de segurança de forma estruturada e sistemática.

## Competências Desenvolvidas (DCNs / ENADE)
*   Identificar riscos associados ao uso de Sistemas de Informação;
*   Avaliar vulnerabilidades técnicas, humanas e organizacionais;
*   Analisar incidentes sob a ótica da Tríade CID;
*   Relacionar ameaças, vulnerabilidades e impactos organizacionais.

---

## 3.1 Conceitos Fundamentais: Ameaça, Vulnerabilidade, Ataque e Risco

A correta compreensão dos conceitos de ameaça, vulnerabilidade, ataque e risco é essencial para qualquer atividade relacionada à Segurança da Informação. Esses conceitos formam a base do raciocínio em gestão de riscos, resposta a incidentes e definição de controles de segurança.

### Ameaça
Uma ameaça é qualquer evento, agente ou circunstância com potencial de causar dano a um ativo de informação.
*   **Exemplos:** Cibercriminosos, funcionários mal-intencionados, malware, falhas de energia, desastres naturais e erros humanos.
> 📌 **Importante:** A ameaça representa o potencial de dano, mesmo que nenhuma vulnerabilidade seja explorada naquele momento.

### Vulnerabilidade
Uma vulnerabilidade é uma fraqueza ou falha presente em um sistema, processo, configuração ou comportamento humano que pode ser explorada por uma ameaça.
*   **Exemplos:** Software desatualizado, senhas fracas, permissões excessivas, falta de treinamento e configurações incorretas.
> 📌 Vulnerabilidades existem antes do ataque e independem da presença imediata de uma ameaça ativa.

### Ataque
Um ataque ocorre quando uma ameaça explora efetivamente uma vulnerabilidade, gerando impacto ao sistema ou à organização.
> 📌 Nem toda ameaça resulta em ataque, mas todo ataque envolve uma ameaça explorando uma vulnerabilidade.

### Risco
O risco representa a possibilidade de que uma ameaça explore uma vulnerabilidade, causando impacto negativo à organização.
> **Risco = Ameaça × Vulnerabilidade × Impacto**
> 📌 Se qualquer um desses fatores for reduzido, o risco global diminui.

| Box – Atenção ENADE |
| :--- |
| O ENADE frequentemente explora relações causais entre ameaça, vulnerabilidade e ataque. É comum exigir que o estudante identifique qual elemento estava presente antes do incidente e qual foi explorado durante o ataque. |

---

## 3.2 Ameaças à Segurança da Informação

### 3.2.1 Ameaças Internas e Externas
*   **Ameaças internas:** Originam-se dentro da organização (funcionários, prestadores de serviço, parceiros).
    *   *Exemplo real:* Vazamentos de dados ocorridos devido ao uso indevido de acessos legítimos por funcionários.
*   **Ameaças externas:** Originam-se fora da organização (hackers, grupos de ransomware, agentes estatais).
> 📌 Estudos apontam que ameaças internas, embora menos frequentes, costumam causar impactos mais severos devido ao acesso privilegiado.

### 3.2.2 Ameaças Intencionais e Acidentais
*   **Intencionais:** Ações deliberadas como fraudes, espionagem, sabotagem e ataques cibernéticos.
*   **Acidentais:** Decorrentes de erro humano, falhas operacionais ou desconhecimento técnico.
> 📌 **Dado relevante:** Relatórios como o Verizon DBIR indicam que o erro humano está presente em uma parcela significativa dos incidentes de segurança.

---

## 3.3 Vulnerabilidades em Sistemas de Informação

### 3.3.1 Classificação das Vulnerabilidades
*   **Vulnerabilidades de software:** Erros de programação, falhas de validação, injeção de código (ex: OWASP Top 10).
*   **Vulnerabilidades de configuração:** Senhas padrão, serviços desnecessários ativos, firewalls mal configurados.
*   **Vulnerabilidades de hardware:** Falhas arquiteturais (ex: Spectre e Meltdown), componentes comprometidos.
*   **Vulnerabilidades humanas:** Falta de treinamento, engenharia social, descumprimento de políticas.

| Box – Erro Comum |
| :--- |
| Investir apenas em ferramentas técnicas, ignorando vulnerabilidades humanas e organizacionais, é uma das principais causas de falhas graves em Segurança da Informação. |

---

## 3.4 Tipos de Ataques

### 3.4.1 Ataques à Confidencialidade
Visam obter acesso não autorizado à informação.
*   **Exemplos:** Interceptação de tráfego, spyware, phishing, vazamento de bases de dados.

### 3.4.2 Ataques à Integridade
Visam alterar dados ou sistemas de forma indevida.
*   **Exemplos:** Injeção de SQL, alteração de registros, defacement de websites.

### 3.4.3 Ataques à Disponibilidade
Visam tornar sistemas ou serviços indisponíveis.
*   **Exemplos:** Ataques DoS/DDoS, ransomware, consumo excessivo de recursos.

### 3.4.4 Ataques à Autenticidade
Visam falsificar identidades ou comunicações.
*   **Exemplos:** Spoofing, falsificação de mensagens, ataques Man-in-the-Middle.

---

## 3.5 Vetores de Ataque Modernos

Um vetor de ataque é o caminho utilizado pelo atacante para explorar uma vulnerabilidade. Vetores comuns incluem:
*   Engenharia social;
*   Exploração de aplicações web;
*   Ataques à cadeia de suprimentos;
*   Credenciais comprometidas;
*   Dispositivos pessoais e IoT.

---

## 3.6 Engenharia Social como Vetor Crítico

A engenharia social explora o fator humano, considerado hoje o elo mais fraco da segurança. Técnicas comuns incluem **Phishing**, **Spear phishing**, **Vishing** e **Pretexting**.
*   *Exemplo real:* O ataque ao Twitter (2020) explorou engenharia social para comprometer contas de alto perfil.

| Box – Conexão com o Mercado |
| :--- |
| Treinamento e conscientização em segurança são controles essenciais, exigidos por normas como a ISO/IEC 27001. |

---

## 3.7 Base de Computação Confiável (TCB)

A **Base de Computação Confiável (Trusted Computing Base – TCB)** corresponde ao conjunto de componentes críticos cuja falha compromete a segurança de todo o sistema. Inclui hardware, sistema operacional, mecanismos de autenticação e componentes de auditoria.
> 📌 **Regra prática:** Quanto maior a TCB, maior a superfície de risco. Por isso, sistemas seguros buscam minimizar a TCB.

---

## Resumo do Capítulo
*   Ameaças representam o potencial de dano;
*   Vulnerabilidades são fraquezas exploráveis;
*   Ataques concretizam riscos ao explorar vulnerabilidades;
*   O risco depende da combinação entre ameaça, vulnerabilidade e impacto;
*   O fator humano é um dos principais vetores de ataque.

---

## Referências e Leituras Complementares
*   STALLINGS, W.; BROWN, L. Computer Security: Principles and Practice.
*   PFLEEGER, C. P.; PFLEEGER, S. L. Security in Computing.
*   [OWASP Top 10](https://owasp.org/www-project-top-ten/)
*   [Verizon Data Breach Investigations Report (DBIR)](https://www.verizon.com/business/resources/reports/dbir/)
*   [ENISA Threat Landscape](https://www.enisa.europa.eu/topics/threat-risk-management/threats-and-trends)
