# Documentação da Linguagem Go - Projeto CTT AP2

## Integrantes do Grupo
- Nicolas Lima
- Hector Borges
- Kayque Rodrigues
- Gabriella Correa

## Site Publicado
[https://impacta-gb.github.io/projeto-ctt-ap2-nexus/](https://impacta-gb.github.io/projeto-ctt-ap2-nexus/)

---

## Sobre o Projeto

Este projeto consiste em uma documentação completa da linguagem de programação **Go**, gerada estaticamente com a ferramenta **Zensical** e publicada no **GitHub Pages**.

O principal objetivo não foi apenas criar o conteúdo, mas sim **aplicar um fluxo de trabalho profissional** de desenvolvimento colaborativo.

---

## Fluxo de Trabalho Colaborativo

### Estrutura de Branches
- `main` – branch principal **protegida** (não aceita commits diretos)
- `feat/*` – branches para novas funcionalidades/documentação

### Processo de Revisão
1. Cada desenvolvedor cria uma branch a partir da `main`
2. Desenvolve o conteúdo
3. Abre um **Pull Request (PR)** para a `main`
4. **Outro membro** revisa e aprova
5. Após aprovação, faz o merge

---

## Pipeline de CI/CD

### Arquitetura do Workflow

O pipeline está dividido em **3 jobs**:

#### Job 1: `validate` (Validação cruzada)
- **Executa em:** `pull_request` para `main`
- **Objetivo:** Garantir que o PR não quebra o site antes da aprovação
- **Estratégia:** Matrix com duas versões do Python (3.10 e 3.11)
- **Otimização:** Cache do pip

#### Job 2: `build_site` (Build + Artefato)
- **Executa em:** `push` para `main` ou `schedule`
- **Objetivo:** Gerar os arquivos HTML estáticos
- **Saída:** Upload do artefato `site-output`

#### Job 3: `deploy_site` (Publicação condicional)
- **Executa SOMENTE quando:** `push` para `main` ou `schedule`
- **NUNCA executa em:** `pull_request`
- **Objetivo:** Publicar no GitHub Pages

### Gatilhos (Triggers)
```yaml
on:
  pull_request:
    branches: [main]
  push:
    branches: [main]
  schedule:
    - cron: '0 0 * * 0'
