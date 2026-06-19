# Análise ATS — Currículo (PDF)

**Arquivo analisado:** `CVs/Currículo.pdf` (versão atual)  
**Fonte de edição:** `CVs/Currículo.html`  
**Data da análise:** maio de 2026  
**Método:** extração automática de texto (simulação de leitura ATS) + revisão de conteúdo

---

## Resumo executivo

| Pergunta | Resposta |
|----------|----------|
| O PDF está apto para ATS? | **Sim.** Texto selecionável, 1 página, ~3.065 caracteres extraídos. |
| O currículo está bem para dev Full Stack no BR? | **Sim.** Stack, liderança e processo bem representados. |
| Por que antes deu 42 e depois 83? | PDF antigo **sem texto** (~806 KB) vs. PDF atual **legível** (~104 KB); revisores e critérios diferentes. |
| Nota única confiável? | **Não.** Use como checklist; teste sempre com a **vaga colada**. |
| Faixa estimada (PDF atual + vaga) | **75–90** |
| Faixa estimada (PDF atual, sem vaga) | **65–80** |

**Conclusão:** o currículo evoluiu de um problema de **exportação** para um documento **tecnicamente sólido para ATS**. O foco agora é **match por vaga** e pequenos refinamentos opcionais de layout (GitHub na linha de projetos, colunas do rodapé).

---

## Diagnóstico técnico do PDF

| Indicador | Resultado | Interpretação |
|-----------|-----------|---------------|
| Páginas | 1 | Ideal para triagem |
| Texto extraído | ~3.065 caracteres | Conteúdo completo indexável |
| Tamanho do arquivo | ~104 KB | Típico de PDF com camada de texto |
| Pesquisa (Ctrl+F) | Funciona | Mesmo comportamento esperado do ATS |
| Acentuação PT-BR | Preservada | liderança, persistência, etc. |

### Histórico (por que as notas variaram)

| Versão | Sintoma | Efeito no ATS |
|--------|---------|---------------|
| PDF antigo (~806 KB) | Não dava para buscar palavras | Extração vazia → nota **muito baixa (~42)** |
| PDF atual (~104 KB) | Texto selecionável | Keywords indexadas → nota **compatível com ~83** em revisores que leem bem |

**Regra de ouro:** após cada edição no HTML, exportar PDF e testar **Ctrl+F** por `React`, `Scrum` e `AGX`.

---

## O que o ATS lê do seu PDF (estrutura)

Ordem aproximada da extração linear:

1. **Identificação** — nome, headline, Sorocaba, contato, links  
2. **Resumo profissional** — Full Stack, hands-on, liderança, JavaScript, React, TypeScript, Node.js, MongoDB, SQL, C#, Scrum, Jira  
3. **Competências** — 4 blocos (front, back, liderança/processo, ferramentas + IA)  
4. **Experiência** — AGX Software \| Jul 2024 - Presente, cargo, 4 bullets  
5. **Projetos** — Deprecated-Finder, MedIT (TCC), Repo-Workspace  
6. **Formação + certificações** — duas colunas no layout visual  
7. **Idiomas** — PT nativo, EN intermediário  

### Correções já refletidas no PDF

- `AGX Software | Jul 2024 - Presente` (não cola mais como `AGX SoftwareJul`)  
- Separadores ASCII (`|`, `-`) em vez de `·` e `–`  
- **Scrum**, **Tailwind CSS**, **CI/CD**, **Postman** presentes  
- **TechMoto** removido (mais espaço visual no rodapé; C# permanece em competências)

---

## Palavras-chave detectadas no PDF

### Stack e desenvolvimento

| Categoria | Termos |
|-----------|--------|
| Front-end | React.js, TypeScript, JavaScript, HTML5, CSS3, **Tailwind CSS**, Sass, Less, Ant Design, responsividade |
| Back-end / dados | Node.js, **APIs REST**, C# (.NET), MongoDB, SQL, Python |
| Ferramentas | Git, GitHub, **Postman**, Jira, VS Code, Cursor, Figma, Notion, Yarn |
| Automação / IA | n8n, agentes de IA |

### Processo, liderança e entrega

| Categoria | Termos |
|-----------|--------|
| Metodologia | **Scrum**, metodologias ágeis, sprints, Jira |
| Engenharia | code review, Pull Requests, **CI/CD**, padrões de código, sustentação de legado |
| Liderança | liderança hands-on, **4 desenvolvedores**, GitHub Projects |
| Resultado | 4 promoções, entregas alinhadas ao negócio |

### Projetos e formação

| Item | Destaque ATS |
|------|----------------|
| Deprecated-Finder | TypeScript, VS Code/Cursor, extensão |
| MedIT (TCC) | TypeScript, React, saúde |
| Repo-Workspace | JavaScript, yarn, CLI |
| ADS 2024-2026 | Athon / Anhembi Morumbi |
| ETEC 2021-2024 | Técnico em Desenvolvimento de Sistemas |
| Certificações | Oracle OCI, MongoDB Path, Git (Ada Tech), Web Frontend (Udemy), n8n + IA |

---

## Match com tipos de vaga

### Desenvolvedor Full Stack / Front-end (ex.: AGX, vagas React)

| Requisito comum | No PDF? |
|-----------------|---------|
| React | Sim |
| TypeScript | Sim |
| JavaScript | Sim |
| APIs REST | Sim |
| Git / PR / code review | Sim |
| Tailwind CSS | Sim |
| Performance / UX | Sim (bullet AGX) |
| Next.js | Não (omitido de propósito no HTML atual) |
| Inglês avançado | Não (intermediário declarado) |

### Líder técnico / hands-on (ex.: Alutal)

| Requisito comum | No PDF? |
|-----------------|---------|
| Liderança de equipe | Sim (4 devs) |
| React + JavaScript | Sim |
| C# / .NET | Sim (competências; sem projeto TechMoto) |
| SQL | Sim |
| GitHub | Sim |
| Scrum / ágil | Sim |
| Sustentação de legado | Sim |

---

## Pontos fortes (ATS + recrutador)

1. **Densidade de keywords** sem parecer lista solta — skills categorizadas + repetição na experiência.  
2. **Uma empresa com narrativa de evolução** — estágio → Pleno I, 4 promoções.  
3. **Liderança mensurável** — equipe de 4 pessoas.  
4. **Projetos com stack explícita** e MedIT marcado como TCC.  
5. **Certificações nomeadas** com instituição e ano.  
6. **PDF tecnicamente válido** para parsers modernos.  
7. **Headline alinhada** — Full Stack, Líder, React, TypeScript, C#.

---

## Pontos de atenção (opcionais)

Nenhum impede candidatura; são refinamentos se quiser maximizar score.

| Item | Situação no PDF | Sugestão |
|------|-----------------|----------|
| `PROJETOS SELECIONADOSgithub.com/...` | Título e URL colados na extração | GitHub em linha separada abaixo do título |
| Formação + certificações | Colunas podem quebrar datas (`2024-` / `2026`) | Aceitável; DOCX 1 coluna só se algum portal falhar |
| Apenas 1 empregador | Normal para sua senioridade | Manter bullet de evolução interna |
| Next.js | Ausente | Incluir só se for verdade no dia a dia |
| Inglês intermediário | Honesto | Pode pesar em vagas com inglês avançado obrigatório |
| C# sem projeto dedicado | TechMoto removido | C# ainda aparece em skills e resumo; ok para Full Stack |

---

## Checklist ATS — versão atual

| Critério | Status |
|----------|--------|
| PDF com texto selecionável | ✅ |
| 1 página | ✅ |
| Tamanho ~100 KB (texto, não imagem) | ✅ |
| Nome, telefone, e-mail, cidade | ✅ |
| LinkedIn, GitHub, portfólio | ✅ |
| Seções com títulos claros (PT-BR) | ✅ |
| Experiência com empresa, cargo, datas | ✅ |
| Bullets com ação e métricas | ✅ |
| Seção de competências rica | ✅ |
| Scrum / Jira / CI/CD / Postman / Tailwind | ✅ |
| Projetos relevantes | ✅ |
| Formação + certificações | ✅ |
| Idiomas | ✅ |
| Match depende da vaga colada no revisor | ⚠️ |
| GitHub colado ao título de projetos | ⚠️ |

---

## Pontuação estimada por cenário

| Cenário | Faixa |
|---------|-------|
| PDF antigo sem texto (referência histórica) | 15–45 |
| **PDF atual**, revisor sem descrição de vaga | **65–80** |
| **PDF atual** + vaga colada + ajuste pontual de keywords | **75–90** |
| DOCX linear (fallback para portais difíceis) | 80–92 |

Para comparar revisores de forma justa: **mesmo PDF + mesma vaga + mesma ferramenta**.

---

## Prioridades de melhoria

### Manutenção (sempre)

1. Editar `Currículo.html` → **Ctrl+P** → salvar `Currículo.pdf`.  
2. Validar **Ctrl+F** antes de cada candidatura.  
3. Enviar **PDF**, nunca HTML, nos portais.

### Match por vaga (5–10 min)

4. Colar descrição da vaga no revisor ATS.  
5. Incluir no HTML apenas keywords **verdadeiras** que faltarem (ex.: Kanban, Vitest, .NET Core).  
6. Reexportar PDF e retestar.

### Layout (opcional, se algum revisor falhar)

7. Linha dedicada: `GitHub: github.com/RafaelHDSV (71+ projetos públicos)`.  
8. Versão **1 coluna** para Formação + Certificações (DOCX alternativo).

### Conteúdo (só se for real)

9. **Next.js** — se já estiver em uso na AGX.  
10. **Testes automatizados** (Jest/Vitest) — se fizer parte da rotina.  
11. Projeto **C#** de volta — se quiser reforçar vagas .NET (ex. TechMoto em uma linha).

---

## Avaliação por público

| Público | Avaliação |
|---------|-----------|
| ATS (triagem automática) | **Muito bom** com PDF atual |
| Recrutador / tech lead | **Muito bom** — claro, 1 página, liderança visível |
| Vaga front-end com Tailwind + React + Git | **Alto match** |
| Vaga com Scrum + Jira + liderança júnior | **Alto match** |
| Vaga internacional (inglês fluente obrigatório) | **Médio** — gap de idioma |
| Vaga sênior / Tech Lead formal | **Médio-alto** — liderança forte; título “Líder” (não Tech Lead) é adequado |

---

## Roteiro de teste ATS (recomendado)

```
1. Abrir Currículo.pdf → Ctrl+F "Tailwind" → deve encontrar
2. No revisor: upload do PDF (não HTML)
3. Colar descrição completa da vaga
4. Anotar keywords faltando
5. Ajustar HTML somente com fatos reais
6. Reexportar PDF → repetir passo 2
```

---

## Arquivos na pasta `CVs/`

| Arquivo | Função |
|---------|--------|
| `Currículo.html` | Edição e exportação |
| `Currículo.pdf` | **Envio em candidaturas** (versão validada nesta análise) |
| `Currículo_2025.*` | Histórico / log |
| `analise-ats.md` | Este documento |

---

## Referências

- [github.com/RafaelHDSV](https://github.com/RafaelHDSV)  
- [linkedin.com/in/rafael-vieira1720](https://linkedin.com/in/rafael-vieira1720)  
- [Alutal — Líder de Desenvolvimento de Software](https://www.linkedin.com/jobs/view/4404092497)

---

*Análise baseada em extração de `Currículo.pdf` em maio de 2026: 1 página, ~3.065 caracteres, ~104 KB. Revisores ATS automáticos são indicativos, não garantia de aprovação.*
