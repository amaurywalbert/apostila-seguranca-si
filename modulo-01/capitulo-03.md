# Capítulo 3 – Ameaças, Vulnerabilidades, Ataques e Panorama de Ataques Modernos

## Objetivos do Capítulo
Ao final deste capítulo, o estudante será capaz de:
* Compreender os conceitos fundamentais de ameaça, vulnerabilidade, ataque e risco;
* Analisar o panorama atual dos ataques cibernéticos modernos;
* Identificar e classificar vetores de ataque contemporâneos;
* Compreender o papel do fator humano na exploração de sistemas;
* Analisar ataques como engenharia social, phishing e ransomware;
* Entender o conceito e a importância da Base de Computação Confiável (TCB);
* Relacionar ataques modernos às propriedades da Tríade da Segurança da Informação (CID).

## Competências Desenvolvidas (DCNs / ENADE)
* Identificar riscos associados ao uso de Sistemas de Informação;
* Avaliar vulnerabilidades técnicas, humanas e organizacionais;
* Analisar incidentes de segurança sob a ótica da Tríade CID;
* Relacionar arquitetura de sistemas, TCB e exposição a ataques;
* Interpretar cenários reais de incidentes de segurança.

---

## 3.1 Conceitos Fundamentais: Ameaça, Vulnerabilidade, Ataque e Risco
A correta compreensão desses conceitos é essencial para qualquer atividade em Segurança da Informação, sendo amplamente explorada em avaliações como o ENADE.

### Ameaça
Uma ameaça é qualquer evento, agente ou circunstância com potencial de causar dano a um ativo de informação.

**Exemplos de ameaças:**
* Cibercriminosos;
* Funcionários mal-intencionados;
* Malware;
* Falhas de energia;
* Desastres naturais;
* Erros humanos.

> **Observação:** A ameaça representa o **potencial** de dano, mesmo que nenhuma vulnerabilidade seja explorada naquele momento.

### Vulnerabilidade
Uma vulnerabilidade é uma fraqueza ou falha presente em um sistema, processo, configuração ou comportamento humano que pode ser explorada por uma ameaça.

**Exemplos de vulnerabilidades:**
* Software desatualizado;
* Senhas fracas ou reutilizadas;
* Permissões excessivas;
* Falta de treinamento dos usuários;
* Configurações incorretas de sistemas e redes.

> Vulnerabilidades existem antes do ataque e independem da existência de uma ameaça ativa.

### Ataque
Um ataque ocorre quando uma ameaça explora efetivamente uma vulnerabilidade, gerando impacto ao sistema ou à organização.
* Nem toda ameaça resulta em ataque, mas todo ataque envolve a exploração de uma vulnerabilidade.

### Risco
O risco representa a possibilidade de que uma ameaça explore uma vulnerabilidade, causando impacto negativo. De forma simplificada:

$$\text{Risco} = \text{Ameaça} \times \text{Vulnerabilidade} \times \text{Impacto}$$

A redução de qualquer um desses fatores diminui o risco global.

> 📌 **Atenção ENADE**
> Questões frequentemente exigem que o estudante identifique:
> * O que existia **antes** do incidente (ameaça e vulnerabilidade);
> * O que ocorreu **durante** o incidente (ataque).

---

## 3.2 Classificação das Ameaças à Segurança da Informação

### 3.2.1 Ameaças Internas e Externas
* **Ameaças internas:** Funcionários, prestadores de serviço, terceirizados e parceiros com acesso legítimo.
* **Ameaças externas:** Hackers, grupos de ransomware, organizações criminosas e agentes estatais.

> Ameaças internas são menos frequentes, porém geralmente causam impactos mais severos, devido ao acesso privilegiado.

### 3.2.2 Ameaças Intencionais e Acidentais
* **Intencionais:** Fraudes, espionagem, sabotagem, ataques cibernéticos.
* **Acidentais:** Erros humanos, falhas operacionais, desconhecimento técnico.

> Relatórios como o *Verizon DBIR* indicam que o erro humano está presente em grande parte dos incidentes.

---

## 3.3 Vulnerabilidades em Sistemas de Informação
As vulnerabilidades podem surgir em diferentes camadas do sistema.

### 3.3.1 Tipos de Vulnerabilidades
* **Software:** Falhas de programação, injeção de código, estouro de buffer;
* **Configuração:** Senhas fracas, serviços desnecessários ativos, permissões excessivas;
* **Hardware:** Falhas arquiteturais ou físicas;
* **Humanas:** Falta de treinamento, engenharia social, descumprimento de políticas.

> **Erro comum:** Investir apenas em ferramentas técnicas e ignorar vulnerabilidades humanas e organizacionais.

---

## 3.4 Tipos de Ataques segundo a Tríade CID

### 3.4.1 Ataques à Confidencialidade
* Phishing;
* Spyware;
* Interceptação de tráfego;
* Vazamentos de dados.

### 3.4.2 Ataques à Integridade
* Injeção de código (SQL, comandos);
* Alteração de registros;
* Defacement de websites.

### 3.4.3 Ataques à Disponibilidade
* DoS/DDoS;
* Ransomware;
* Consumo excessivo de recursos.

### 3.4.4 Ataques à Autenticidade
* Spoofing;
* Falsificação de mensagens;
* Man-in-the-Middle.

---

## 3.5 Panorama Atual dos Ataques Cibernéticos
O cenário contemporâneo de ataques é caracterizado por:
* Alto grau de organização;
* Motivação financeira, política ou estratégica;
* Cadeias completas de exploração;
* Combinação de falhas técnicas, humanas e organizacionais.

O cibercrime opera hoje como modelo de negócio, com serviços como:
* *Ransomware-as-a-Service* (RaaS);
* *Phishing-as-a-Service* (PhaaS);
* Malware modular;
* Exploração automatizada de vulnerabilidades conhecidas.

---

## 3.6 Vetores de Ataque Modernos
Um vetor de ataque é o caminho utilizado pelo atacante para explorar uma vulnerabilidade.

**Vetores comuns atualmente:**
* Engenharia social;
* Phishing e comprometimento de credenciais;
* Ransomware;
* Ataques à cadeia de suprimentos (*Supply Chain*);
* Dispositivos pessoais, IoT e trabalho remoto.

> O foco deslocou-se de falhas puramente técnicas para vetores híbridos.

---

## 3.7 Engenharia Social como Vetor Crítico
A engenharia social explora características humanas como confiança, medo, urgência, curiosidade e autoridade.

**Técnicas comuns:**
* Phishing;
* Spear phishing;
* Whaling;
* Vishing;
* Smishing;
* Pretexting.

> Controles técnicos robustos podem ser contornados por ataques bem-sucedidos de engenharia social.

> **Exemplo real – Ataque ao Twitter (2020):** Funcionários foram enganados por engenharia social, permitindo acesso a sistemas internos e comprometimento de contas de alto perfil.

---

## 3.8 Phishing e Comprometimento de Credenciais
O phishing é hoje a principal porta de entrada para ataques corporativos.

**Características modernas:**
* Mensagens altamente personalizadas;
* Uso de dados vazados;
* Clones perfeitos de páginas legítimas;
* Uso de HTTPS com certificados válidos.

Credenciais comprometidas são reutilizadas para acessar VPNs, e-mails corporativos e serviços em nuvem.

---

## 3.9 Ransomware como Modelo de Negócio
O ransomware evoluiu para um ecossistema criminoso estruturado.

**Características:**
* Criptografia forte;
* Exfiltração de dados (dupla extorsão);
* Ameaça de vazamento público;
* Pagamentos em criptomoedas.

**Principais alvos:** Hospitais, prefeituras, universidades e infraestruturas críticas.

---

## 3.10 Ataques à Cadeia de Suprimentos
Exploram a confiança entre organizações, comprometendo bibliotecas, atualizações de software ou fornecedores de serviços. Um único comprometimento pode afetar milhares de organizações.

---

## 3.11 Relação entre Vetores Modernos e Tríade CID

| Vetor de Ataque | Confidencialidade | Integridade | Disponibilidade |
| :--- | :---: | :---: | :---: |
| **Phishing** | ✔️ | | |
| **Ransomware** | | ✔️ | ✔️ |
| **Engenharia Social** | ✔️ | ✔️ | ✔️ |
| **DDoS** | | | ✔️ |
| **Supply Chain** | ✔️ | ✔️ | ✔️ |

---

## 3.12 Base de Computação Confiável (TCB)
A **Base de Computação Confiável** (*Trusted Computing Base – TCB*) é o conjunto mínimo de componentes cuja falha compromete toda a segurança do sistema.

**Componentes típicos:**
* Hardware;
* Firmware;
* Sistema operacional;
* Mecanismos de autenticação;
* Controle de acesso;
* Auditoria e logs.

> Quanto maior a TCB, maior a superfície de ataque.

**TCB e Ataques Modernos:**
Ataques modernos buscam escalada de privilégios, comprometimento do sistema operacional e acesso a mecanismos de autenticação. O objetivo é atingir a TCB, pois isso garante controle total do sistema.

---

## 3.13 Implicações Práticas para Organizações
A análise do panorama moderno revela que:
1.  Ferramentas isoladas não são suficientes;
2.  O fator humano é crítico;
3.  Arquiteturas seguras e TCB mínima são essenciais;
4.  Treinamento, governança e processos são tão importantes quanto tecnologia.

---

## Resumo do Capítulo
* **Ameaças** representam potencial de dano;
* **Vulnerabilidades** são fraquezas exploráveis;
* **Ataques** concretizam riscos;
* O cenário atual é organizado, persistente e híbrido;
* Engenharia social e phishing são vetores centrais;
* Ransomware opera como modelo de negócio;
* Ataques à cadeia de suprimentos ampliam impactos;
* A **TCB** define o núcleo crítico da segurança;
* Minimizar a TCB reduz significativamente riscos.

---

## Referências e Leituras Complementares

* **Verizon – Data Breach Investigations Report (DBIR):** [Relatório Anual de Investigações de Violação de Dados](https://www.verizon.com/business/resources/reports/dbir/)
* **Ataque ao Twitter (2020):** [Matéria sobre como o fator humano foi o elo fraco no incidente do Twitter](https://olhardigital.com.br/2020/07/16/seguranca/ataque-ao-twitter-prova-que-pessoas-sao-o-elo-fraco-de-sistemas-de-seguranca/)
* **Ataques a Hospitais:** [Alerta da ISH Tecnologia sobre ciberataques a hospitais brasileiros](https://itsection.com.br/2025/09/30/ish-tecnologia-alerta-para-ciberataques-a-hospitais-brasileiros)

## Leituras Complementares
Para aprofundar os conhecimentos em frameworks e tendências globais de ameaças:

* **ENISA – Threat Landscape:** [Relatório de panorama de ameaças da agência da União Europeia](https://www.enisa.europa.eu/topics/threat-risk-management/threats-and-trends)
* **NIST – Cybersecurity Framework:** [Framework de referência para gestão de riscos de cibersegurança](https://www.nist.gov/cyberframework)
* **OWASP Foundation:** [Referência para Threat Modeling e o Top 10 vulnerabilidades](https://owasp.org)
* **MITRE ATT&CK Framework:** [Base de conhecimento global de táticas e técnicas de adversários](https://attack.mitre.org)
* **CISA – Ransomware Guidance:** [Guia oficial do governo dos EUA para prevenção e resposta a Ransomware](https://www.cisa.gov/ransomware)