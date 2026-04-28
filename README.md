# Blog Escritor SEO — Squad ExpxAgents

Pipeline de 10 agentes que pesquisa, redige e publica artigos de blog otimizados para SEO, com template HTML alinhado à identidade visual da empresa.

## O que essa squad faz

A cada execução, ela:
1. Valida o contexto da empresa configurada
2. Extrai o design system da marca (cores, fontes)
3. Pesquisa keywords e tendências do setor
4. Define pauta e estratégia SEO
5. Seleciona imagens do Unsplash/Pexels
6. Cria ou atualiza os templates HTML do blog
7. Redige o artigo completo (1.500–2.500 palavras)
8. Revisa o conteúdo editorial e SEO
9. Monta o pacote HTML final e atualiza a homepage

## Pré-requisitos

- [ExpxAgents](https://expxagents.com) instalado
- Empresa configurada em `_expxagents/_memory/company.md`
- Logo em `_expxagents/_assets/logo-branco.png`

## Como instalar

Copie esta pasta para dentro do diretório `squads/` do seu projeto:

```
squads/
  marketing/
    conteudo/
      blog/
        blog-escritor-seo/   ← aqui
```

## Como rodar

```bash
/expxagents run blog-escritor-seo
```

## Agentes

| Agente | Função |
|--------|--------|
| Carlos Mendes | Validador — verifica configuração da empresa |
| Beatriz Fontes | Design System Builder — extrai tokens da marca (condicional) |
| Ana Beatriz | Pesquisadora — keywords e tendências |
| Marcos Oliveira | Estrategista SEO — pauta e estrutura do artigo |
| Renata Vidal | Curador de Imagens — seleciona fotos do Unsplash/Pexels |
| Isabela Nunes | UX Blog — cria templates HTML/CSS (condicional) |
| Juliana Santos | Redatora — escreve o artigo completo |
| Fernanda Costa | Revisora — revisão editorial e SEO |
| Diego Ferreira | Publicador — monta HTML final e atualiza homepage |
| Fernando Dias | Deployer — publica no servidor (trigger manual) |

## Versão

v2.0.0
