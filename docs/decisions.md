# Registro de Decisões Técnicas

Este documento registra decisões técnicas importantes tomadas durante o desenvolvimento do projeto.

O objetivo é preservar o contexto das escolhas realizadas, facilitando manutenção, revisão e entrada de novos integrantes.

> Registre apenas decisões relevantes. Alterações pequenas ou rotineiras não precisam ser documentadas aqui.

## Como registrar uma decisão

Para cada decisão importante, utilize o modelo abaixo.

---

## DEC-001 — Título da decisão

**Data:** AAAA-MM-DD  
**Status:** Proposta | Aprovada | Substituída | Cancelada  
**Responsável:** Nome ou equipe responsável

### Contexto

Explique o problema, necessidade ou situação que levou à decisão.

### Decisão

Descreva objetivamente o que foi decidido.

### Justificativa

Explique por que essa opção foi escolhida.

### Alternativas consideradas

Liste outras opções avaliadas, quando aplicável.

- Alternativa 1
- Alternativa 2

### Consequências

Registre os principais impactos da decisão.

**Benefícios:**

- A definir.

**Limitações ou riscos:**

- A definir.

### Referências

Inclua Issues, Pull Requests, documentos, Fichas de Requisição ou outras referências relacionadas.

Exemplo:

```text
Ficha: RQS-ATV-...
Issue: #10
Pull Request: #15
```

---

## Exemplo simplificado

## DEC-002 — Utilização de GitHub Actions para CI

**Data:** 2026-07-22  
**Status:** Aprovada  
**Responsável:** Orion AeroDesign

### Contexto

Foi necessário definir uma ferramenta padrão para executar verificações automáticas nos Pull Requests.

### Decisão

Utilizar GitHub Actions como ferramenta padrão de Integração Contínua nos repositórios da organização.

### Justificativa

A ferramenta possui integração nativa com os repositórios GitHub e permite automatizar build, lint, testes e outras validações.

### Alternativas consideradas

- Ferramentas externas de CI;
- execução apenas manual das verificações.

### Consequências

**Benefícios:**

- execução automática das verificações;
- integração com Pull Requests;
- histórico das execuções.

**Limitações ou riscos:**

- cada projeto deverá adaptar a CI à sua tecnologia.

### Referências

```text
Ficha: RQS-ATV-GECO-REP-261001
```
