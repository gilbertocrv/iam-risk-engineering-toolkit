# IAM Risk Engineering Toolkit

Modelo operacional para implementação de controle de acesso, análise de risco e auditabilidade com base na ISO/IEC 27001:2022, aplicado ao Microsoft Entra ID.

---

## O que este projeto resolve

Programas de IAM normalmente falham na execução, não no desenho.

Este toolkit foi construído para:

- Estruturar acessos antes da revisão (RBAC / PAM)
- Gerar evidência rastreável para auditoria
- Identificar e analisar conflitos de segregação de funções (SoD)
- Suportar decisões baseadas em risco

Ele conecta controles da ISO 27001 com a execução operacional de IAM.

---

## Modelo Central

RBAC → Estrutura  
PAM  → Criticidade  
SoD  → Risco  

---

## Ciclo Operacional de IAM

Identidade → Acesso → Evidência → Revisão → SoD → Decisão

- Identidade — usuário, service principal, identidade externa  
- Acesso — roles, grupos, entitlements  
- Evidência — rastreabilidade e artefatos de auditoria  
- Revisão — validação dos acessos atribuídos  
- SoD — análise de conflitos  
- Decisão — recertificação ou remediação  

---

## Como usar (5 minutos)

1. Abra o index.html  
2. Carregue os arquivos da pasta /samples  
3. Execute o fluxo:  
   - RBAC Role Mapper → estrutura de acesso  
   - PAM Inventory → contas críticas  
   - SoD Analyzer → conflitos de função  
4. Exporte os resultados como evidência  

Execução 100% local, sem backend.

---

## Arquitetura (visão simplificada)

Dados (CSV: roles, groups, sign-ins)  
        ↓  
Processamento (RBAC / PAM / ABAC)  
        ↓  
Análise de Risco (SoD)  
        ↓  
Geração de Evidência  
        ↓  
Suporte à Decisão  

---

## Mapeamento ISO/IEC 27001

| Controle | Descrição | Camada |
|---|---|---|
| 5.15 | Controle de Acesso | RBAC |
| 8.2 | Acesso Privilegiado | PAM |
| 5.3 | Segregação de Funções | SoD |
| 8.3 | Restrição de Acesso à Informação | RBAC |
| 5.18 | Revisão de Acessos | Governança de Roles |

---

## Estrutura do Repositório

iam-risk-engineering-toolkit/
│
├── index.html
│
├── docs/
│   ├── architecture.html
│   ├── data-model.html
│   └── concepts/
│       ├── access-model.html
│       ├── rbac.html
│       ├── pam.html
│       ├── sod.html
│       ├── abac.html
│       └── pbac.html
│
├── tools/
│   ├── rbac/
│   │   └── role-mapper.html
│   ├── pam/
│   │   └── pam-inventory.html
│   ├── sod/
│   │   ├── index.html
│   │   ├── sod-model.html
│   │   └── sod-risk-analyzer.html
│   ├── abac/
│   │   └── conditional-access-analyzer.html
│   └── pbac/
│       └── policy-simulator.html
│
└── samples/
    ├── roles.csv
    ├── groups.csv
    └── signins.csv

---

## Ferramentas no ciclo IAM

| Fase | Ferramenta |
|------|------------|
| Identidade / Acesso | RBAC Role Mapper |
| Criticidade | PAM Inventory |
| Evidência | Todas (exportação estruturada) |
| Revisão | Role Explosion Analyzer |
| SoD | SoD Conflict Analyzer |
| Decisão | PBAC Policy Simulator |

---

## Ferramentas

| Tool | Conceito | Controles ISO |
|---|---|---|
| RBAC Role Mapper | Classificação de roles, detecção de orfãos e acúmulo | 5.15 · 8.3 |
| PAM Inventory | Contas privilegiadas, MFA, inatividade, risco | 8.2 |
| SoD Conflict Analyzer | Conflitos, severidade e evidência exportável | 5.3 · 8.2 |
| Role Explosion Analyzer | Acúmulo, padrões atípicos, governança | 5.15 · 5.18 |
| Conditional Access Analyzer | Políticas CA e análise de lacunas | 5.15 |
| PBAC Policy Simulator | Simulação de decisão (Permit/Deny/Conditional) | 5.15 |

---

## Princípios

- A ISO define os controles; a execução depende do contexto
- Acesso precisa ser estruturado antes de ser revisado
- Sem evidência, risco não é verificável
- Risco precisa ser analisado antes da decisão

---

## O que este projeto demonstra

- Tradução de controles ISO 27001 em processos operacionais de IAM  
- Estruturação de acesso baseada em RBAC e PAM  
- Implementação prática de análise de SoD  
- Foco em auditabilidade e geração de evidência  
- Conhecimento aplicado em Microsoft Entra ID  

---

## Limitações

- Não há integração em tempo real com Microsoft Graph (uso de CSV)
- Não executa enforcement (análise e simulação apenas)
- Foco educacional e de prova de conceito (PoC)

---

## Posicionamento

Este projeto não é um produto nem um framework completo.

É um toolkit operacional projetado para:

- Traduzir governança em execução
- Estruturar ciclos de revisão de acesso
- Gerar evidência auditável
- Apoiar decisões baseadas em risco

---

## Escopo

- Uso educacional e demonstrativo  
- Execução local (sem backend)  
- Processamento no navegador  
- Foco em governança e operacionalização de IAM  

---

## Base Normativa

- ISO/IEC 27001:2022 — Controles 5.3, 5.15, 5.18, 8.2, 8.3  
- SC-300 — Microsoft Identity and Access Administrator  
- Microsoft Entra ID — documentação pública  

---

## Relacionado

- iam-operational-cycle-toolkit — ciclo de auditoria, recertificação e evidência  

---

## Autor

Gilberto Gonçalves dos Santos Filho  
IAM / Identity Governance Analyst — Access Control · SoD · Audit & Risk Modeling  

LinkedIn: https://linkedin.com/in/gilberto-filho-4430a3184  
GitHub: https://github.com/gilbertocrv
