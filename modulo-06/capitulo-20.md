# Capítulo 20 – Resposta a Incidentes e Análise de Malware

## Objetivos do Capítulo

Ao final deste capítulo, o estudante será capaz de:

* Compreender o conceito de incidente de segurança da informação;
* Reconhecer a importância de um processo estruturado de resposta a incidentes;
* Identificar as fases do ciclo de vida da resposta a incidentes;
* Entender os conceitos fundamentais da análise de malware;
* Relacionar resposta a incidentes, monitoramento, continuidade de negócios e recuperação de desastres;
* Avaliar impactos técnicos, organizacionais e legais decorrentes de incidentes de segurança. 

---

## Competências Desenvolvidas (DCNs / ENADE)

* Analisar eventos de segurança e classificá-los adequadamente;
* Aplicar conceitos de resposta a incidentes em ambientes organizacionais;
* Avaliar impactos sobre a confidencialidade, integridade e disponibilidade;
* Compreender o papel da análise de malware no tratamento de incidentes;
* Relacionar aspectos técnicos, gerenciais e legais da segurança da informação. 

---

# 20.1 Incidentes de Segurança

A operação segura de sistemas de informação não depende apenas da prevenção de ataques. Mesmo organizações que adotam boas práticas de segurança podem sofrer incidentes. Nesse contexto, torna-se essencial possuir capacidade de detectar, responder e recuperar-se rapidamente de eventos adversos.

Um **incidente de segurança da informação** é qualquer evento que comprometa ou tenha potencial de comprometer a confidencialidade, a integridade ou a disponibilidade das informações e dos sistemas. 

---

## Evento versus Incidente

Nem todo evento de segurança é necessariamente um incidente.

### Evento

Qualquer ocorrência observável em um sistema ou rede.

**Exemplos:**

* Login realizado com sucesso;
* Reinicialização de um servidor;
* Tentativa de acesso negada;
* Atualização de software.

---

### Incidente

Evento ou conjunto de eventos que gera impacto real ou potencial sobre a segurança.

**Exemplos:**

* Roubo de credenciais;
* Vazamento de dados;
* Ataque de ransomware;
* Comprometimento de contas;
* Negação de serviço (DoS/DDoS);
* Infecção por malware. 

---

| Box – Atenção ENADE                                                                                                                                                           |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| O ENADE frequentemente explora a diferença entre evento e incidente, exigindo que o estudante identifique quando uma ocorrência passa a representar risco real à organização. |

---

## Características dos Incidentes

Os incidentes podem variar em:

| Critério         | Exemplos                   |
| ---------------- | -------------------------- |
| Origem           | Interna ou externa         |
| Intencionalidade | Acidental ou maliciosa     |
| Impacto          | Baixo, médio ou alto       |
| Escopo           | Localizado ou generalizado |
| Duração          | Instantâneo ou persistente |

---

## Classificação de Incidentes

Uma classificação adequada auxilia na priorização das ações de resposta.

### Incidentes de Confidencialidade

Relacionados ao acesso indevido à informação.

**Exemplos:**

* Vazamento de dados;
* Roubo de credenciais;
* Espionagem corporativa.

---

### Incidentes de Integridade

Relacionados à alteração indevida de informações.

**Exemplos:**

* Modificação não autorizada de registros;
* Defacement de websites;
* Manipulação de bancos de dados.

---

### Incidentes de Disponibilidade

Relacionados à indisponibilidade de serviços.

**Exemplos:**

* Ataques DDoS;
* Ransomware;
* Falhas críticas de infraestrutura.

---

## Impactos Organizacionais

Os impactos de um incidente podem incluir:

* Interrupção de operações;
* Perdas financeiras;
* Danos reputacionais;
* Descumprimento regulatório;
* Responsabilidade legal;
* Perda de confiança de clientes e parceiros.

---

# 20.2 Ciclo de Vida da Resposta a Incidentes

A resposta a incidentes consiste em um conjunto organizado de atividades destinadas a identificar, conter, eliminar e recuperar-se de eventos de segurança.

O modelo mais amplamente utilizado é baseado nas recomendações do NIST e divide a resposta em fases sucessivas.

---

## Visão Geral do Processo

```text
Preparação
      ↓
Detecção e Análise
      ↓
Contenção
      ↓
Erradicação
      ↓
Recuperação
      ↓
Lições Aprendidas
```

📌 O objetivo não é apenas restaurar o ambiente, mas também reduzir a probabilidade de recorrência.

---

## Fase 1 – Preparação

A preparação ocorre antes de qualquer incidente.

Envolve:

* Políticas de resposta;
* Equipe responsável (CSIRT ou SOC);
* Ferramentas de monitoramento;
* Procedimentos documentados;
* Treinamentos;
* Exercícios simulados;
* Planos de comunicação.

---

### Equipes de Resposta

Diversas organizações mantêm equipes especializadas.

**CSIRT (Computer Security Incident Response Team)**

Responsável pela coordenação das atividades de resposta.

**SOC (Security Operations Center)**

Responsável pelo monitoramento contínuo e detecção de eventos.

---

## Fase 2 – Detecção e Análise

Consiste na identificação e validação de possíveis incidentes.

Fontes comuns:

* Logs;
* SIEM;
* IDS/IPS;
* Antivírus;
* EDR/XDR;
* Relatos de usuários.

---

### Perguntas Importantes

* O incidente realmente ocorreu?
* Qual seu impacto?
* Quais ativos foram afetados?
* O ataque ainda está em andamento?
* Existe risco de propagação?

---

### Priorização

Incidentes costumam ser classificados por criticidade:

| Nível   | Descrição                       |
| ------- | ------------------------------- |
| Baixo   | Impacto limitado                |
| Médio   | Afeta parte da operação         |
| Alto    | Impacto significativo           |
| Crítico | Compromete processos essenciais |

---

## Fase 3 – Contenção

O objetivo é impedir que o incidente se espalhe.

### Exemplos

* Isolar servidores comprometidos;
* Desconectar estações infectadas;
* Bloquear contas suspeitas;
* Filtrar tráfego malicioso;
* Segmentar a rede.

---

### Contenção de Curto Prazo

Ações imediatas para limitar danos.

**Exemplo:**

```text
Host comprometido
↓
Desconectar da rede
↓
Preservar evidências
```

---

### Contenção de Longo Prazo

Implementação de controles permanentes para impedir reincidência.

---

## Fase 4 – Erradicação

Consiste em remover a causa raiz do incidente.

### Exemplos

* Remoção de malware;
* Correção de vulnerabilidades;
* Revogação de credenciais comprometidas;
* Atualização de sistemas;
* Reconfiguração de serviços.

---

## Fase 5 – Recuperação

Objetiva restaurar a operação normal.

Atividades típicas:

* Restauração de backups;
* Reinstalação de sistemas;
* Validação de integridade;
* Testes operacionais;
* Monitoramento reforçado.

---

## Fase 6 – Lições Aprendidas

Muitas organizações encerram o incidente após a recuperação, mas a fase mais importante frequentemente ocorre depois.

Deve-se analisar:

* O que ocorreu;
* Como ocorreu;
* O que funcionou bem;
* O que falhou;
* Como evitar recorrência.

---

### Relatório Pós-Incidente

Um relatório deve registrar:

* Linha do tempo;
* Sistemas afetados;
* Impactos;
* Ações executadas;
* Custos;
* Recomendações.

---

| Box – Reflexão                                                                                                                |
| :---------------------------------------------------------------------------------------------------------------------------- |
| Incidentes inevitavelmente ocorrerão. Organizações maduras diferenciam-se pela rapidez e eficiência com que respondem a eles. |

---

# 20.3 Análise de Malware

Malware é qualquer software desenvolvido com objetivos maliciosos.

A análise de malware busca compreender:

* Como o código funciona;
* Como se propaga;
* Quais danos causa;
* Como detectá-lo;
* Como removê-lo.

A análise auxilia diretamente a resposta a incidentes e a mitigação de ataques. 

---

## Principais Categorias de Malware

### Vírus

Necessitam de um hospedeiro para se propagar.

---

### Worms

Propagam-se automaticamente pela rede.

---

### Cavalos de Troia (Trojans)

Disfarçam-se como software legítimo.

---

### Spyware

Coletam informações sem consentimento.

---

### Ransomware

Criptografam arquivos e exigem pagamento.

---

### Rootkits

Ocultam a presença de invasores no sistema.

---

### Botnets

Transformam dispositivos comprometidos em uma rede controlada remotamente.

---

## Objetivos dos Malwares

* Roubo de informações;
* Espionagem;
* Sabotagem;
* Fraude financeira;
* Extorsão;
* Controle remoto de sistemas.

---

## Processo de Análise de Malware

A análise pode ocorrer em diferentes níveis.

---

## Análise Estática

Realizada sem executar o malware.

### Técnicas

* Cálculo de hash;
* Identificação de strings;
* Inspeção de binários;
* Análise de cabeçalhos;
* Verificação de assinaturas digitais.

### Vantagens

* Menor risco;
* Rápida execução.

### Limitações

* Pode não revelar comportamentos ocultos.

---

## Análise Dinâmica

Consiste em executar o malware em ambiente controlado.

### Observa-se

* Processos criados;
* Alterações em arquivos;
* Modificações no registro;
* Conexões de rede;
* Persistência.

---

### Sandbox

Ambiente isolado utilizado para execução segura.

Exemplos:

* Cuckoo Sandbox;
* Any.Run;
* Joe Sandbox.

---

## Indicadores de Comprometimento (IoCs)

Durante a análise são identificados elementos úteis para detecção futura.

### Exemplos

* Hashes de arquivos;
* Endereços IP maliciosos;
* Domínios suspeitos;
* Chaves de registro;
* Processos específicos.

---

## Caso Real – WannaCry

O ransomware WannaCry, em 2017, explorou a vulnerabilidade EternalBlue para propagar-se automaticamente.

Impactos:

* Hospitais;
* Universidades;
* Empresas;
* Órgãos governamentais.

Lições aprendidas:

* Importância de atualizações;
* Gestão de vulnerabilidades;
* Backups confiáveis;
* Resposta rápida a incidentes.

---

## Caso Real – NotPetya

Inicialmente classificado como ransomware, o NotPetya possuía características destrutivas e causou bilhões de dólares em prejuízos globais.

O caso demonstrou que:

* Nem todo ransomware visa lucro;
* Cadeias de suprimentos podem ser exploradas;
* Recuperação pode ser extremamente complexa.

---

# 20.4 Continuidade de Negócios e Recuperação de Desastres

A resposta a incidentes não termina com a remoção da ameaça.

Organizações precisam garantir a continuidade das operações mesmo diante de eventos graves.

---

## Continuidade de Negócios (Business Continuity)

Conjunto de estratégias destinadas a manter processos essenciais funcionando durante crises.

Objetivos:

* Minimizar interrupções;
* Preservar serviços críticos;
* Reduzir impactos financeiros;
* Garantir atendimento a clientes.

---

## Recuperação de Desastres (Disaster Recovery)

Foca especificamente na restauração de infraestrutura e sistemas.

Inclui:

* Servidores;
* Redes;
* Bancos de dados;
* Aplicações;
* Ambientes em nuvem.

---

## Plano de Continuidade de Negócios (PCN)

Deve definir:

* Processos críticos;
* Responsáveis;
* Recursos necessários;
* Estratégias alternativas;
* Procedimentos de comunicação.

---

## Plano de Recuperação de Desastres (PRD)

Deve contemplar:

* Procedimentos de recuperação;
* Backups;
* Ambientes redundantes;
* Testes periódicos;
* Critérios de retorno à operação normal.

---

## Métricas Importantes

### RTO – Recovery Time Objective

Tempo máximo aceitável para restaurar um serviço.

### RPO – Recovery Point Objective

Quantidade máxima aceitável de perda de dados.

---

### Exemplo

| Sistema              | RTO      | RPO        |
| -------------------- | -------- | ---------- |
| ERP Financeiro       | 2 horas  | 15 minutos |
| Portal Institucional | 8 horas  | 1 hora     |
| Sistema de RH        | 12 horas | 4 horas    |

---

## Relação com Segurança da Informação

A continuidade de negócios está diretamente relacionada à disponibilidade, um dos pilares da Tríade CID.

Sem planejamento adequado:

* Ataques podem paralisar operações;
* Dados podem ser perdidos;
* Serviços podem permanecer indisponíveis por longos períodos.

---

# 20.5 Boas Práticas em Resposta a Incidentes

Recomenda-se que organizações:

* Possuam plano formal de resposta a incidentes;
* Definam papéis e responsabilidades;
* Mantenham inventário atualizado de ativos;
* Realizem exercícios periódicos;
* Coletem e preservem evidências;
* Monitorem continuamente o ambiente;
* Integrem SIEM e processos de resposta;
* Atualizem procedimentos após cada incidente;
* Utilizem inteligência de ameaças;
* Treinem usuários regularmente.

---

# Conexão com Normas e Frameworks

## NIST SP 800-61

Referência internacional para tratamento de incidentes.

Define:

* Preparação;
* Detecção;
* Contenção;
* Erradicação;
* Recuperação.

---

## ISO/IEC 27001

Exige processos formais para:

* Gestão de incidentes;
* Tratamento de eventos;
* Melhoria contínua.

---

## LGPD

Incidentes envolvendo dados pessoais podem exigir:

* Avaliação de impacto;
* Comunicação à autoridade competente;
* Comunicação aos titulares afetados.

---

# Resumo do Capítulo

* Incidentes representam eventos que afetam a segurança da informação;
* A resposta a incidentes deve seguir processo estruturado;
* O ciclo envolve preparação, detecção, contenção, erradicação, recuperação e lições aprendidas;
* A análise de malware auxilia na compreensão e mitigação de ataques;
* Continuidade de negócios e recuperação de desastres reduzem impactos operacionais;
* A melhoria contínua é parte essencial da maturidade em segurança. 

---

# Referências e Leituras Complementares

* [NIST SP 800-61 Rev. 3 – *Computer Security Incident Handling Guide*](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
* [NIST SP 800-34 – *Contingency Planning Guide for Federal Information Systems* ](https://csrc.nist.gov/pubs/sp/800/34/r1/upd1/final)
* [ISO/IEC 27035 – *Information Security Incident Management* ](https://www.iso.org/standard/78973.html)
* [ISO/IEC 27001 – *Information Security Management Systems*](https://www.iso.org/standard/27001)
* [MITRE ATT&CK Framework](https://attack.mitre.org)
* [CISA – Incident Response Resources](https://www.cisa.gov/resources-tools/services/cyber-incident-response)
* STALLINGS, W.; BROWN, L. *Computer Security: Principles and Practice*
* SÊMOLA, M. *Gestão da Segurança da Informação*
* [ENISA Threat Landscape](https://www.enisa.europa.eu/publications/enisa-threat-landscape-2025)
* [Verizon Data Breach Investigations Report (DBIR)](https://www.verizon.com/business/resources/reports/dbir/)
