# Análise ATS — Currículo (PDF)

**Arquivo analisado:** `CVs/Currículo.pdf` (versão atual, texto selecionável)  
**Fonte para edição:** `CVs/Currículo.html`  
**Data da análise:** maio de 2026  
**Contexto:** notas anteriores de **42** e **83** — a nota baixa foi explicada por PDF antigo **sem camada de texto** (não pesquisável)

---

## Resumo executivo

| Pergunta | Resposta |
|----------|----------|
| O currículo está bom para ATS? | **Sim**, na versão atual do PDF. Conteúdo e formato são adequados para dev Full Stack no BR. |
| O PDF está legível para sistemas? | **Sim** — extração automática confirmada (~3.000 caracteres, 1 página). |
| Por que antes deu 42? | PDF anterior exportado como **imagem** (~806 KB, 0 texto). ATS lia página em branco. |
| Por que 83 em outro teste? | Outra ferramenta, outro arquivo (HTML) ou vaga colada — não contradiz o PDF novo. |
| Faixa esperada agora | **72–88** com PDF atual + descrição da vaga no revisor; **55–70** sem vaga de referência. |
| Nota única “oficial”? | **Não.** Use revisores como checklist, não como veredito final. |

**Conclusão:** o problema era a **exportação**, não o conteúdo. Com o `Currículo.pdf` atual, o ATS consegue ler nome, contato, skills, AGX, projetos e formação. Foque em **match por vaga** e nos pequenos ajustes de layout listados abaixo.

---

## Diagnóstico do `Currículo.pdf` atual

Teste de extração de texto (mesmo tipo de leitura que muitos ATS fazem):

| Verificação | PDF antigo (errado) | PDF atual (correto) |
|-------------|---------------------|---------------------|
| Páginas | 1 | **1** |
| Texto extraído | **0 caracteres** | **~3.031 caracteres** |
| Tamanho do arquivo | ~806 KB | **~100 KB** |
| Pesquisa no leitor (Ctrl+F) | Não funcionava | **Funciona** |
| Pronto para candidatura | Não | **Sim** |

**Como manter assim:** exportar sempre a partir do `Currículo.html` com **Ctrl+P → Salvar como PDF** (Chrome/Edge), escala 100%, 1 página. Evitar exportações que rasterizam a página inteira em imagem.

### Teste rápido antes de cada envio

1. Abrir o PDF → **Ctrl+F** → buscar `React` ou `AGX`.  
2. Selecionar um parágrafo → **Ctrl+C** → colar no Bloco de Notas.  
3. Se o texto colado for legível, o ATS tende a ler da mesma forma.

---

## O que o ATS extrai do seu PDF (ordem real)

Trecho linearizado a partir do arquivo atual — útil para entender como o sistema “vê” o currículo:

```text
Rafael Henrique De Sousa Vieira
Desenvolvedor Full Stack · Líder · React · TypeScript · C#
Sorocaba, SP | (11) 94710-0007
rafaelvieira1720@gmail.com | linkedin.com/in/rafael-vieira1720 | ...

RESUMO PROFISSIONAL
Desenvolvedor Full Stack com perfil hands-on e experiência em liderança de equipe...
JavaScript — React, TypeScript, Node.js, MongoDB, SQL — C# (.NET)...

COMPETÊNCIAS TÉCNICAS
Front-end: React.js, TypeScript, JavaScript, HTML5, CSS3, Sass, Less, Ant Design...
Back-end e dados: Node.js, APIs REST, C# (.NET), MongoDB, SQL
Liderança e engenharia: liderança hands-on, code review, Pull Requests...
...

EXPERIÊNCIA PROFISSIONAL
AGX SoftwareJul 2024 – Presente
Desenvolvedor Full Stack Júnior III + Líder de Equipe
[bullets da AGX]

PROJETOS SELECIONADOSgithub.com/RafaelHDSV (71+ projetos públicos)
Deprecated-Finder — ...
MedIT (TCC) — ...
...

FORMAÇÃO ACADÊMICA | CERTIFICAÇÕES (colunas)
IDIOMAS
```

Tudo essencial está presente para busca por palavra-chave.

---

## Pontos fortes para ATS (confirmados no PDF)

### Estrutura

- **1 página** — ideal para triagem rápida.  
- Seções com títulos claros em português (aparecem em maiúsculas na extração: `RESUMO PROFISSIONAL`, `EXPERIÊNCIA PROFISSIONAL`, etc.).  
- **Experiência em bullets** — quatro itens com verbos de ação (Evoluí, Lidero, Desenvolvo, Atuo).  
- **Datas** legíveis: `Jul 2024 – Presente`.  
- **Localização:** Sorocaba, SP.  
- **Links** em texto: e-mail, LinkedIn, GitHub, portfólio.

### Palavras-chave (mercado dev / liderança júnior)

| Área | Termos detectados no PDF |
|------|--------------------------|
| Stack web | JavaScript, TypeScript, React, Node.js, HTML5, CSS3, Sass, Less |
| Dados / API | APIs REST, MongoDB, SQL |
| Outras | C#, .NET, Ant Design |
| Processo | Git, GitHub, Pull Requests, code review, GitHub Projects |
| Liderança | liderança, hands-on, 4 desenvolvedores, padrões de código |
| Legado / entrega | sustentação de legado, sistemas em produção, boas práticas |
| Projetos | Deprecated-Finder, MedIT (TCC), Repo-Workspace, TechMoto |
| Certificações | Oracle OCI, MongoDB, Web Frontend, n8n, agentes de IA |

### Conteúdo que ranqueia bem

- Progressão na **AGX** (estágio → Júnior III) + **3 promoções**.  
- **Liderança de 4 desenvolvedores** — diferencial para vagas com componente de líder.  
- Projetos com **stack explícita** (`| TypeScript`, `| C#, .NET`).  
- Formação **ADS** + técnico ETEC.

---

## Pontos de atenção (PDF atual — melhorias opcionais)

Nada disso invalida o currículo; são refinamentos se quiser maximizar parsers mais rígidos.

### 1. Textos “colados” na extração (baixo impacto)

O parser às vezes junta blocos vizinhos:

| No PDF visual | Na extração ATS |
|---------------|-----------------|
| AGX Software · Jul 2024 | `AGX SoftwareJul 2024` |
| Projetos Selecionados · github.com/... | `PROJETOS SELECIONADOSgithub.com/...` |

**Por quê:** layout com flex (data à direita, GitHub alinhado ao título).  
**Mitigação:** no HTML, quebrar linha ou inserir espaço fixo entre empresa e data; GitHub em linha própria abaixo do título de projetos.

### 2. Colunas Formação + Certificações (baixo/médio)

Em duas colunas, o ATS pode intercalar linhas. No seu PDF, as seções ainda aparecem completas, mas datas como `2024–` / `2026` podem quebrar em linhas separadas.

**Mitigação:** se algum revisor reclamar de “educação incompleta”, usar versão **1 coluna** só para aquele portal (DOCX opcional).

### 3. Quebra de linha em “C# (.NET)” (muito baixo)

No resumo, `C#` e `(.NET)` podem cair em linhas diferentes na extração. As duas partes ainda estão no texto — risco mínimo.

### 4. Bullets sem marcador “•” no texto bruto

Os itens da AGX são lidos como parágrafos separados, não como lista formal. A maioria dos ATS aceita; o conteúdo das frases permanece indexável.

### 5. Inglês “intermediário” vs vaga exigindo avançado

Não é falha de PDF — é **match de requisito**. Para vagas internacionais, ajustar só se for honesto.

### 6. Match depende da vaga

Revisores sem descrição da vaga costumam dar nota menor. Sempre testar com o **texto da vaga colado**.

---

## Checklist ATS — `Currículo.pdf` atual

| Critério | Status |
|----------|--------|
| PDF com texto selecionável | ✅ Confirmado |
| 1 página | ✅ |
| Tamanho de arquivo saudável (~100 KB) | ✅ |
| Nome, e-mail, telefone | ✅ |
| Cidade/estado | ✅ |
| LinkedIn / GitHub / portfólio em texto | ✅ |
| Seções reconhecíveis | ✅ |
| Experiência com datas e empresa | ✅ |
| Skills dedicadas + repetição na experiência | ✅ |
| Projetos + formação + certificações | ✅ |
| Sem imagem-only / scan | ✅ |
| Colunas no rodapé | ⚠️ Aceitável; opcional simplificar |
| Textos colados (AGX/data, Projetos/GitHub) | ⚠️ Opcional corrigir no HTML |
| Match com palavras da vaga | ⚠️ Adaptar por anúncio |

---

## Pontuação estimada (PDF atual)

| Cenário | Faixa provável |
|---------|----------------|
| PDF antigo (sem texto) — referência | 15–45 ← explica **~42** |
| **PDF atual**, revisor genérico, sem vaga | **58–75** |
| **PDF atual** + vaga colada + keywords alinhadas | **72–88** |
| DOCX 1 coluna (mesmo conteúdo) | 78–92 (se algum portal falhar) |

Refaça os dois revisores usando **somente o PDF novo** e a **mesma vaga** — a comparação passa a ser confiável.

---

## Prioridades de melhoria (pós-correção do PDF)

### Manutenção (sempre)

1. Exportar PDF só via **HTML → Ctrl+P → Salvar como PDF**.  
2. Validar **Ctrl+F** antes de enviar.  
3. Enviar **`Currículo.pdf`** nos portais (não HTML).

### Alto impacto (conteúdo / match)

4. Nos revisores ATS: upload do **PDF atual** + **descrição completa da vaga**.  
5. Incluir na experiência ou resumo **5–10 keywords** da vaga que forem verdadeiras.  
6. Para vagas **liderança** (ex. Alutal): reforçar `liderança`, `React`, `C#`, `SQL`, `GitHub`, `sustentação`.  
7. Para vagas **front-end**: reforçar `React`, `TypeScript`, `JavaScript`, `APIs REST`, `code review`, `Pull Requests`.

### Médio (layout no HTML → novo PDF)

8. Separar `AGX Software` e `Jul 2024 – Presente` (evitar `AGX SoftwareJul`).  
9. GitHub em linha abaixo de “Projetos Selecionados”.  
10. Se nota de “educação” falhar em algum site: versão 1 coluna em Formação/Certificações.

### Baixo

11. `|` e `-` ASCII em vez de `·` e `–` se algum revisor mostrar caracteres estranhos.  
12. Nome de arquivo sem acento: `Rafael_Vieira_Curriculo_FullStack.pdf`.

---

## O currículo está bom?

| Leitor | Avaliação com PDF atual |
|--------|-------------------------|
| **ATS (triagem automática)** | **Bom** — texto extraível, keywords sólidas |
| **Recrutador / tech lead** | **Bom** — 1 página, claro, liderança e stack visíveis |
| **Vaga internacional (inglês avançado)** | **Médio** — conteúdo ok; gap pode ser idioma |
| **Vaga sênior / Tech Lead formal** | **Médio** — liderança forte para júnior; título “Líder” é adequado |

---

## Como testar ATS de forma confiável (roteiro)

1. Abrir `CVs/Currículo.pdf` → confirmar busca por `React`.  
2. Escolher **uma vaga** alvo.  
3. No revisor: upload **deste PDF** + colar descrição da vaga.  
4. Anotar keywords faltando (só as que você realmente tem).  
5. Ajustar `Currículo.html` → exportar **novo** PDF → repetir teste.  
6. Comparar os dois revisores **no mesmo PDF** (não misturar com HTML).

---

## Adaptação rápida por vaga (5 min)

1. Copiar requisitos obrigatórios.  
2. Marcar ✓ (já no PDF) / ✗ (faltando).  
3. Inserir ✗ verdadeiros no HTML.  
4. Exportar PDF → validar Ctrl+F.  
5. Reenviar ao revisor com vaga colada.

**Já coberto no PDF atual:** React, TypeScript, JavaScript, Node.js, MongoDB, SQL, Git, GitHub, REST, liderança, code review, legado, Ant Design, C#/.NET.

---

## Arquivos na pasta `CVs/`

| Arquivo | Uso |
|---------|-----|
| `Currículo.html` | Edição e exportação |
| `Currículo.pdf` | **Envio em candidaturas** (versão atual OK) |
| `Currículo_2025.*` | Histórico / log |
| `analise-ats.md` | Este documento |

---

## Referências

- [github.com/RafaelHDSV](https://github.com/RafaelHDSV)  
- [linkedin.com/in/rafael-vieira1720](https://linkedin.com/in/rafael-vieira1720)  
- [Alutal — Líder de Desenvolvimento de Software](https://www.linkedin.com/jobs/view/4404092497)

---

*Análise baseada no `Currículo.pdf` com texto selecionável (~3.031 caracteres extraídos, 1 página, ~100 KB). O PDF anterior sem camada de texto não deve ser usado para novos testes ou candidaturas.*
