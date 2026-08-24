# Vibe Coding Starter

Workflow reutilizável para desenvolvimento de sites profissionais com **ChatGPT + Figma + Codex**, desde o briefing com o cliente até a auditoria técnica e publicação.

Este repositório não é um boilerplate de interface e não contém um site pronto.

Ele reúne o processo, os prompts e as regras utilizados para conduzir projetos frontend com IA de forma estruturada, mantendo decisões de produto, design e escopo sob controle humano.

---

## Objetivo

O objetivo deste starter é reduzir o tempo necessário para iniciar e desenvolver novos sites sem transformar vibe coding em geração descontrolada de código.

O processo separa as responsabilidades entre:

### ChatGPT

Responsável principalmente por:

- condução e interpretação do briefing;
- definição do MVP;
- definição da jornada;
- decisões de produto;
- direção visual;
- preparação do `PROJECT.md`;
- revisão visual;
- análise dos resultados;
- decisão sobre quais correções devem ser realizadas.

### Figma

Opcional.

Pode ser utilizado para:

- explorar a direção visual;
- validar composição;
- definir referências de layout;
- visualizar o projeto antes da implementação.

Para sites simples, o desenvolvimento pode seguir diretamente para o código quando a direção visual estiver suficientemente definida.

### Codex

Responsável principalmente por:

- analisar o repositório;
- planejar a implementação técnica;
- implementar o frontend;
- investigar problemas;
- executar validações;
- realizar auditoria técnica;
- aplicar somente as correções aprovadas.

---

# Fluxo

```text
Cliente
   ↓
Briefing
   ↓
ChatGPT
   ↓
Interpretação + MVP + Jornada
   ↓
Direção visual
   ↓
Figma (opcional)
   ↓
PROJECT.md
   ↓
Setup do projeto
   ↓
AGENTS.md
   ↓
Codex
   ↓
Análise inicial
   ↓
Bloco 1 — Fundação + Header + Hero
   ↓
Revisão visual
   ↓
Bloco 2 — Conteúdo principal
   ↓
Revisão visual
   ↓
Bloco 3 — Final CTA + Footer
   ↓
Revisão visual global
   ↓
Auditoria técnica
   ↓
Revisão humana da auditoria
   ↓
Correções aprovadas
   ↓
Validação final
   ↓
Git
   ↓
Deploy
```

---

# Estrutura do starter

```text
vibe-coding-starter/
├── docs/
│   ├── briefing.md
│   ├── figma-prompt.md
│   └── codex-prompts.md
│
├── AGENTS.md
├── CHATGPT-PROMPT.md
├── PROJECT.template.md
└── README.md
```

---

# Arquivos

## `CHATGPT-PROMPT.md`

Prompt utilizado para iniciar um novo projeto no ChatGPT.

Ele estabelece:

- responsabilidades;
- princípios do processo;
- controle de escopo;
- ordem das etapas;
- papel do ChatGPT;
- papel do Codex.

Use no início de cada novo projeto.

---

## `docs/briefing.md`

Briefing com as perguntas principais para o cliente.

O objetivo é coletar informações sobre:

- negócio;
- objetivo;
- público;
- conversão;
- conteúdo;
- funcionalidades;
- identidade visual;
- referências;
- materiais disponíveis;
- expectativas.

O briefing deve refletir as respostas reais do cliente.

Não complete informações ausentes por suposição.

---

## `docs/figma-prompt.md`

Prompt para criação de uma direção visual no Figma.

Use quando uma referência visual antes da implementação trouxer benefício ao projeto.

O Figma não é uma etapa obrigatória.

---

## `PROJECT.template.md`

Template utilizado para gerar o `PROJECT.md` específico de cada projeto.

O arquivo registra:

- visão geral;
- objetivo;
- público;
- CTA;
- MVP;
- jornada;
- seções;
- conteúdo disponível;
- conteúdo pendente;
- direção visual;
- design system;
- responsividade;
- acessibilidade;
- performance;
- SEO;
- stack;
- escopo;
- critérios de aceite.

O `PROJECT.md` resultante será a principal fonte de verdade sobre o produto durante a implementação.

---

## `AGENTS.md`

Define as regras permanentes para o agente trabalhar no repositório.

Inclui regras relacionadas a:

- escopo;
- implementação;
- dependências;
- placeholders;
- responsividade;
- acessibilidade;
- SEO;
- qualidade;
- Git.

Copie este arquivo para a raiz de cada novo projeto.

---

## `docs/codex-prompts.md`

Contém os prompts utilizados durante a implementação.

A sequência padrão é:

1. Análise inicial
2. Bloco 1 — Fundação + Header + Hero
3. Bloco 2 — Conteúdo principal
4. Bloco 3 — Final CTA + Footer
5. Auditoria final
6. Correções aprovadas após auditoria

Cada etapa deve ser revisada antes de avançar.

---

# Como iniciar um novo projeto

## 1. Inicie uma nova conversa no ChatGPT

Copie o conteúdo de:

```text
CHATGPT-PROMPT.md
```

Use essa conversa como ambiente principal de planejamento e revisão do projeto.

---

## 2. Faça o briefing

Utilize:

```text
docs/briefing.md
```

O briefing pode ser:

- respondido diretamente pelo cliente;
- realizado durante uma reunião;
- preenchido durante uma conversa.

Preserve as respostas originais.

---

## 3. Interprete o briefing

Com o ChatGPT, transforme as respostas em:

- objetivo principal;
- público;
- problema;
- CTA;
- MVP;
- jornada;
- estrutura;
- conteúdo necessário;
- funcionalidades;
- restrições;
- pendências.

Separe claramente:

**o que o cliente pediu**

de

**o que foi decidido como solução para atender ao pedido.**

---

## 4. Defina a direção visual

Determine:

- conceito;
- sensações;
- paleta;
- tipografia;
- composição;
- tratamento de imagens;
- ritmo;
- referências;
- elementos que devem ser evitados.

Quando necessário, utilize:

```text
docs/figma-prompt.md
```

para gerar uma referência visual.

---

## 5. Crie o projeto frontend

Para o fluxo padrão:

```bash
npm create vite@latest
```

Selecione:

```text
React
JavaScript
```

Depois:

```bash
cd nome-do-projeto
npm install
npm run dev
```

A stack pode ser alterada quando o projeto exigir, mas isso deve ser uma decisão consciente e não uma escolha automática do agente.

---

## 6. Inicialize o Git

Caso ainda não esteja inicializado:

```bash
git init
```

Confira:

```bash
git status
```

Faça um primeiro checkpoint quando a base estiver correta.

Exemplo:

```bash
git add .
git commit -m "chore: initialize project"
```

---

## 7. Crie o `PROJECT.md`

Copie:

```text
PROJECT.template.md
```

para o novo repositório.

Renomeie para:

```text
PROJECT.md
```

Preencha utilizando as decisões tomadas durante:

- briefing;
- interpretação;
- definição do MVP;
- direção visual.

Não deixe decisões importantes apenas no histórico do ChatGPT.

Se o Codex precisar saber algo para implementar corretamente, essa informação deve estar no projeto.

---

## 8. Adicione o `AGENTS.md`

Copie:

```text
AGENTS.md
```

para a raiz do novo projeto.

A estrutura deve ficar aproximadamente:

```text
novo-projeto/
├── src/
├── public/
├── AGENTS.md
├── PROJECT.md
├── package.json
└── ...
```

---

# Desenvolvimento com Codex

Na raiz do projeto, inicie:

```bash
codex
```

Os prompts estão em:

```text
docs/codex-prompts.md
```

---

## Etapa 1 — Análise inicial

Comece sempre pelo prompt:

```text
01 — Análise inicial
```

O Codex deve primeiro entender o projeto.

Não permita que ele comece alterando arquivos imediatamente.

Revise:

- estrutura proposta;
- dependências;
- arquivos;
- decisões indefinidas;
- complexidade sugerida.

Somente depois aprove a implementação.

---

## Etapa 2 — Bloco 1

Execute:

```text
02 — Bloco 1: Fundação + Header + Hero
```

Depois da implementação:

```bash
npm run dev
```

Abra o site no navegador e revise visualmente.

Verifique principalmente:

- identidade visual;
- Hero;
- hierarquia;
- Header;
- CTA;
- espaçamento;
- mobile.

Corrija problemas concretos antes de avançar.

---

## Etapa 3 — Bloco 2

Execute:

```text
03 — Bloco 2: Conteúdo principal
```

Depois faça outra revisão visual.

Verifique:

- ritmo entre seções;
- repetição excessiva de layouts;
- hierarquia;
- imagens;
- leitura;
- alinhamentos;
- responsividade;
- coerência com a jornada.

---

## Etapa 4 — Bloco 3

Execute:

```text
04 — Bloco 3: Final CTA + Footer
```

Depois faça uma revisão visual da página completa.

Neste momento, avalie o site como uma experiência única, não apenas seção por seção.

---

# Revisão visual

Relatórios do agente não substituem revisão no navegador.

Sempre verifique manualmente:

- desktop;
- tablet quando relevante;
- mobile.

Procure:

- desalinhamentos;
- espaçamentos estranhos;
- conteúdo apertado;
- áreas vazias sem intenção;
- quebras de texto;
- hierarquia;
- contraste;
- CTAs;
- navegação;
- comportamento das imagens.

Problemas visuais conhecidos devem ser corrigidos antes da auditoria.

A auditoria não deve funcionar como uma lista de tarefas que já sabemos que existem.

---

# Auditoria técnica

Quando o MVP estiver visualmente aprovado, utilize:

```text
05 — Auditoria final
```

O Codex deve apenas analisar.

Não permita correções automáticas nesta etapa.

A auditoria deve considerar:

- estrutura;
- código;
- navegação;
- conversão;
- responsividade;
- acessibilidade;
- imagens;
- performance;
- SEO;
- placeholders;
- assets;
- código morto.

---

# Revisão da auditoria

Não trate todas as recomendações do agente como obrigatórias.

Classifique os resultados entre:

### Problema real

Algo que:

- quebra funcionalidade;
- prejudica acessibilidade;
- impede produção;
- cria comportamento incorreto;
- gera manutenção problemática.

### Pendência de conteúdo

Algo que depende do cliente:

- imagens;
- logo;
- contatos;
- depoimentos;
- textos;
- domínio;
- favicon;
- dados comerciais.

### Melhoria opcional

Algo que pode melhorar o projeto, mas não é necessário para o MVP.

### Overengineering

Sugestão tecnicamente possível, mas sem benefício proporcional à complexidade adicionada.

---

# Correções finais

Depois de revisar a auditoria, utilize:

```text
06 — Correções após auditoria
```

Envie somente a lista de correções aprovadas.

O Codex não deve decidir sozinho que toda recomendação da auditoria precisa ser implementada.

---

# Validação

Antes de considerar o frontend tecnicamente concluído:

```bash
npm run build
npm run lint
git diff --check
```

Também confira:

```bash
git status
```

E teste a aplicação no navegador.

---

# Conteúdo real

Antes da publicação, substitua todos os placeholders necessários.

Verifique principalmente:

- logo;
- imagens;
- alt texts;
- WhatsApp;
- Instagram;
- email;
- endereço;
- depoimentos;
- nomes;
- textos;
- favicon;
- Open Graph;
- domínio;
- links externos.

Nunca publique depoimentos, contatos, preços ou informações fictícias como se fossem reais.

---

# Git

Prefira commits que representem etapas compreensíveis do desenvolvimento.

Exemplos:

```bash
git commit -m "chore: initialize project"
git commit -m "feat: add landing foundation and hero"
git commit -m "feat: add main landing content"
git commit -m "feat: complete landing page mvp"
git commit -m "fix: improve accessibility and seo"
```

Não force granularidade quando alterações de etapas diferentes já estiverem misturadas.

Um commit coerente é melhor do que uma separação artificial ou incorreta.

---

# Deploy

Somente publique quando:

- conteúdo obrigatório estiver presente;
- placeholders de produção tiverem sido removidos;
- links estiverem funcionando;
- responsividade estiver validada;
- build estiver passando;
- auditoria tiver sido revisada;
- correções obrigatórias tiverem sido aplicadas;
- SEO básico estiver configurado.

A plataforma de deploy depende do projeto.

---

# Princípios do workflow

## IA não define o produto sozinha

Vibe coding não significa entregar todas as decisões para o agente.

A IA pode acelerar:

- planejamento;
- implementação;
- revisão;
- investigação;
- documentação.

Mas decisões sobre:

- escopo;
- experiência;
- produto;
- direção visual;
- prioridade;
- qualidade final

continuam exigindo revisão humana.

## Não inventar dados

Quando informações do cliente estiverem ausentes, utilize placeholders.

Nunca preencha lacunas silenciosamente.

## MVP primeiro

Uma funcionalidade não deve ser implementada apenas porque seria interessante.

Se não for necessária para o objetivo atual, registre para uma versão futura.

## Simplicidade

Não adicione:

- biblioteca;
- abstração;
- componente;
- arquitetura;
- integração

sem benefício concreto.

## Revisar antes de avançar

O fluxo é incremental por um motivo.

Cada bloco deve estar suficientemente correto antes do próximo.

Isso reduz retrabalho e impede que problemas estruturais se espalhem pelo projeto.

---

# Checklist final

Antes do deploy:

- [ ] Briefing concluído
- [ ] MVP definido
- [ ] Jornada definida
- [ ] Direção visual aprovada
- [ ] `PROJECT.md` atualizado
- [ ] `AGENTS.md` presente
- [ ] Header funcionando
- [ ] Hero funcionando
- [ ] Conteúdo principal implementado
- [ ] Final CTA funcionando
- [ ] Footer funcionando
- [ ] Desktop revisado
- [ ] Mobile revisado
- [ ] CTAs testados
- [ ] Links testados
- [ ] Imagens finais inseridas
- [ ] Alt texts revisados
- [ ] Conteúdo real inserido
- [ ] Placeholders de produção removidos
- [ ] Acessibilidade básica revisada
- [ ] SEO básico configurado
- [ ] Auditoria concluída
- [ ] Correções obrigatórias aplicadas
- [ ] `npm run build` aprovado
- [ ] `npm run lint` aprovado
- [ ] `git diff --check` aprovado
- [ ] `git status` revisado
- [ ] Commit final realizado
- [ ] Deploy validado

---

# Observação

Este workflow foi pensado inicialmente para sites frontend simples, como:

- landing pages;
- portfólios;
- sites institucionais;
- páginas profissionais;
- sites de apresentação de serviços.

Projetos com backend, autenticação, pagamentos, dashboards, aplicações complexas ou requisitos específicos devem adaptar o processo em vez de aplicar este starter mecanicamente.