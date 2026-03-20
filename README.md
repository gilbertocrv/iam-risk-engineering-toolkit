# IAM Risk Engineering Toolkit

Ferramentas e documentação para estruturar controle de acesso, classificar privilégio, detectar conflitos de segregação e modelar políticas baseadas em atributos e contexto.

**GitHub Pages:** `https://gilbertocrv.github.io/iam-risk-engineering-toolkit`

Complementa o [iam-operational-cycle-toolkit](https://github.com/gilbertocrv/iam-operational-cycle-toolkit) — enquanto o ciclo operacional valida se o acesso está sendo controlado, este repositório define a estrutura sobre a qual esse ciclo opera.

---

## Estrutura

```
iam-risk-engineering-toolkit/
│
├── index.html
│
├── docs/
│   ├── architecture.html
│   └── concepts/
│       ├── access-model.html     # visão geral do modelo
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
```

---

## Ferramentas

| Ferramenta | Conceito | Controles ISO |
|---|---|---|
| RBAC Role Mapper | Classifica roles/grupos · detecta órfãos · multi-role | 5.15 · 8.3 |
| PAM Inventory | Tiers 0–2 · MFA · inatividade · risco por conta | 8.2 |
| SoD Conflict Analyzer | 10 conflitos documentados · severidade · evidência exportável | 5.3 · 8.2 |
| Role Explosion Analyzer | Órfãos · acumulação · grupos atípicos | 5.15 · 5.18 |
| Conditional Access Analyzer | Inventário de políticas CA · lacunas · import JSON Graph API | 5.15 |
| PBAC Policy Simulator | Define políticas · simula Permit / Deny / Conditional · log CSV | 5.15 |

---

## Conceitos documentados

| Conceito | Função | ISO |
|---|---|---|
| RBAC | Organizar acesso por função | 5.15 · 8.3 |
| PAM | Controlar privilégio por tier | 8.2 |
| SoD | Detectar combinações de risco | 5.3 |
| ABAC | Acesso por atributo contextual | 5.15 |
| PBAC | Decisão centralizada por política | 5.15 |

---

## Base normativa

- **ISO/IEC 27001:2022** — 5.3, 5.15, 5.18, 8.2, 8.3
- **SC-300** — Microsoft Identity and Access Administrator
- **Microsoft Entra ID** — documentação pública de roles, grupos e Conditional Access

*Conteúdo educacional independente. Todo o processamento ocorre localmente no navegador. Não substitui consultoria técnica especializada.*

---

## Autor

**Gilberto Gonçalves dos Santos Filho**
Analista de Governança de Identidades — IAM · PAM · GRC

[![LinkedIn](https://img.shields.io/badge/LinkedIn-gilberto--filho-0077b5?style=flat-square&logo=linkedin)](https://linkedin.com/in/gilberto-filho-4430a3184)
[![GitHub](https://img.shields.io/badge/GitHub-gilbertocrv-333?style=flat-square&logo=github)](https://github.com/gilbertocrv)
