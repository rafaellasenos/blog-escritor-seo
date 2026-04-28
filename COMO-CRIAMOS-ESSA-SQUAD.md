# Como criamos o squad Blog Escritor SEO
> Passo a passo completo da sessão de criação — 19/04/2026

---

## 1. Onboarding — Configurar a empresa

**Comando:** `/expxagents onboarding`

O sistema detectou que `_expxagents/_memory/company.md` estava vazio e iniciou o onboarding.

- Informamos o site: `https://www.acougueintegrado.com.br/`
- O sistema pesquisou automaticamente com `WebFetch` + `WebSearch`
- Encontrou: nome, setor (SaaS gestão para açougues), descrição, público, produtos, redes sociais
- Confirmamos as informações e salvamos em `_expxagents/_memory/company.md`

---

## 2. Criar o squad — Solution Architect

**Comando:** `/expxagents` → opção "Criar novo squad"

O **Solution Architect** conduziu a fase de Discovery com perguntas focadas:

| Pergunta | Resposta |
|---------|---------|
| Objetivo do squad | Blog e SEO |
| Hierarquia | marketing > conteudo > blog |
| Formato | Artigos completos (research + SEO) |
| Público | Donos e gestores de açougue |
| Referências | Pesquisa de mercado automática |

O Architect fez pesquisa de mercado para identificar temas relevantes (Açougue 4.0, precificação, rastreabilidade, etc.) e propôs o design inicial do squad.

---

## 3. Ajustes iterativos durante o design

O squad foi expandido progressivamente ao longo da conversa:

### Iteração 1 — Pipeline base (4 agentes)
Ana Beatriz → Marcos Oliveira → Juliana Santos → Fernanda Costa

### Iteração 2 — Adicionar distribuição para redes sociais
Usuária pediu: "quero um agente que desmembre o conteúdo em posts para redes sociais"
→ Adicionado: **Bruno Almeida** (Distribuidor)
→ Definidas as redes: **Instagram feed + stories**

### Iteração 3 — Adicionar designer visual
→ Adicionada: **Camila Torres** (Designer Visual — artes HTML/CSS)

### Iteração 4 — Adicionar publicador
→ Adicionado: **Diego Ferreira** (Publicador — revisão final + pacote de publicação)

### Iteração 5 — Adicionar UX designer para o template do blog
Usuária perguntou: "tem algum agente especialista em UX design para blog?"
→ Adicionada: **Isabela Nunes** (UX Designer do Blog)
→ Posicionada no step 03, após a pauta SEO

**Pipeline final:** 8 agentes, 8 steps

---

## 4. Refinamento dos agentes — Copy humanizada

Usuária pediu: "quero que fujam da estrutura de texto genérica de inteligência artificiais, que tenham uma linguagem humanizada"

Atualizações realizadas em **Juliana Santos** e **Bruno Almeida**:

- Adicionada busca de referências de copywriters brasileiros antes de escrever
- Referências: Paulo Maccedo, Leandro Branquinho, Conrado Adolpho, Erico Rocha, André Siqueira
- Anti-patterns específicos: sem "No mundo atual...", sem listas genéricas de IA, sem palavras de enchimento
- Instrução de técnicas: frases curtas, perguntas retóricas, microhistórias, ritmo variado

---

## 5. Brandbook — Design System

Usuária forneceu o arquivo:
`G:\Meu Drive\Clientes\Açougue Integrado\01 Brand Book\BRANDBOOK - Açougue Integrado v2.pdf`

O PDF foi lido e os dados extraídos foram salvos em dois arquivos do design system:

**`squads/design-system/_memory/design-tokens.md`**
- Cores oficiais: `#1179cc` (azul), `#e05402` (vermelho), preto, branco
- Tipografia: Impact (headlines) + Open Sauce (corpo e complementares)
- Espaçamentos, border radius, stacks CSS

**`squads/design-system/_memory/brand-guidelines.md`**
- Regras de logo (versões, o que não fazer)
- Estilo visual dos criativos (fundo azul dominante, highlight vermelho, foto real)
- Exemplos de títulos reais dos criativos oficiais
- Anti-patterns visuais

Os agentes **Camila Torres** e **Isabela Nunes** foram atualizados para ler esses arquivos obrigatoriamente + ter o caminho do PDF como referência.

---

## 6. Estrutura de arquivos criada

```
squads/marketing/conteudo/blog/blog-escritor-seo/
├── squad.yaml                    ← configuração completa do squad
├── squad-party.csv               ← personas dos agentes para o virtual office
├── state.json                    ← estado atual do pipeline (dashboard)
├── agents/
│   ├── pesquisadora.md           ← Ana Beatriz
│   ├── estrategista-seo.md       ← Marcos Oliveira
│   ├── ux-blog.md                ← Isabela Nunes
│   ├── redatora.md               ← Juliana Santos
│   ├── revisora.md               ← Fernanda Costa
│   ├── distribuidor.md           ← Bruno Almeida
│   ├── designer.md               ← Camila Torres
│   └── publicador.md             ← Diego Ferreira
├── templates/
│   ├── blog-article.html         ← template do blog (Isabela)
│   ├── slide-01.html             ← capa do carrossel (Camila)
│   ├── slide-07.html             ← slide CTA final (Camila)
│   └── story-01.html             ← story enquete (Camila)
├── output/
│   └── v1/
│       ├── step-01-pesquisa.md
│       ├── step-02-pauta-seo.md
│       ├── step-03-template.md
│       ├── step-04-artigo.md
│       ├── step-05-revisao.md
│       ├── step-06-posts-instagram.md
│       ├── step-07-artes.md
│       └── step-08-publicacao.md
└── _memory/
    └── memories.md               ← aprendizados do squad

squads/design-system/_memory/
├── design-tokens.md              ← cores, fontes, espaçamentos (do brandbook)
└── brand-guidelines.md           ← regras de marca, estilo, anti-patterns
```

---

## 7. Primeiro run — Tema: Açougue 4.0

**Comando:** `/expxagents run blog-escritor-seo`
**Tema escolhido:** Açougue 4.0 e tecnologia

O pipeline rodou completo em 8 steps, produzindo:
- Artigo de blog ~1.550 palavras (score 8.7/10)
- Template HTML/CSS do blog com brandbook aplicado
- 7 slides de carrossel + legenda + hashtags
- 5 stories com enquete e CTA
- Artes HTML/CSS para Instagram
- Checklist de publicação com ordem e horários

---

## Como rodar novamente

```
/expxagents run blog-escritor-seo
```

Na próxima rodada, o sistema criará automaticamente `output/v2/` e você pode escolher um novo tema da lista ou sugerir o seu.
