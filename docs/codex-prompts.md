# Prompts do Codex

Use estes prompts na ordem indicada.

Cada etapa deve ser revisada antes de avançar para a próxima.

---

# 01 — Análise inicial

Leia `AGENTS.md` e `PROJECT.md` completamente.

Depois analise a estrutura atual do projeto.

Não altere nenhum arquivo.

Quero um plano de implementação contendo:

1. o que precisa ser implementado para atingir o MVP;
2. ordem recomendada;
3. arquivos e pastas que sugere criar;
4. arquivos existentes que provavelmente serão modificados;
5. decisões importantes ainda indefinidas;
6. dados e assets pendentes;
7. riscos de complexidade desnecessária;
8. possíveis dependências que acredita serem necessárias, justificando cada uma.

Priorize uma estrutura enxuta.

Não crie componentes apenas para fragmentar código.

Não proponha bibliotecas quando React, JavaScript e CSS forem suficientes.

Não escreva código ainda.

---

# 02 — Bloco 1: Fundação + Header + Hero

Implemente o **Bloco 1 do MVP: fundação visual + Header + Hero**.

Use `PROJECT.md` e `AGENTS.md` como fonte de verdade.

## Fundação

Configure:

- reset CSS necessário;
- variáveis/tokens;
- cores;
- tipografia;
- escala tipográfica;
- espaçamentos;
- container;
- estilos globais;
- links;
- botões;
- estados de foco;
- responsividade base.

Não adicione bibliotecas sem necessidade.

## Header

Implemente conforme `PROJECT.md`.

Priorize:

- marca;
- navegação;
- CTA principal quando aplicável;
- comportamento mobile simples;
- acessibilidade por teclado.

## Hero

Implemente conforme `PROJECT.md`.

Priorize:

- proposta principal;
- hierarquia;
- CTA;
- elemento visual principal;
- experiência mobile.

Quando assets reais estiverem ausentes, utilize placeholders claramente identificados.

Não invente conteúdo.

## Restrições

Não implemente ainda as demais seções.

Não faça redesign além da direção visual definida.

Não adicione animações elaboradas.

Não faça commit.

## Validação

Execute:

npm run build
npm run lint
git diff --check

Depois informe:

1. arquivos criados e modificados;
2. decisões tomadas;
3. placeholders utilizados;
4. pendências;
5. resultado das validações.

---

# 03 — Bloco 2: Conteúdo principal

Implemente o **Bloco 2 do MVP: conteúdo principal da landing page**.

Use `PROJECT.md`, `AGENTS.md` e os padrões já implementados.

Não altere Header ou Hero sem necessidade.

Implemente todas as seções intermediárias definidas no `PROJECT.md`.

## Objetivo

Cada seção deve possuir função clara dentro da jornada.

Não trate o site como uma sequência de componentes independentes.

Preserve, quando aplicável, uma narrativa como:

**entendimento → demonstração/prova → redução de objeções → oferta → confiança**

## Direção visual

Mantenha consistência sem repetir exatamente a mesma composição.

Evite que todas as seções sejam:

- texto + imagem;
- três cards;
- grids idênticos.

Explore, quando coerente:

- composição editorial;
- diferentes proporções;
- listas;
- divisões sutis;
- alternância de fundos;
- imagens dominantes;
- áreas textuais mais contidas;
- espaço negativo.

Não adicione decoração sem função.

## Dados

Conteúdos repetitivos podem utilizar arquivos de dados simples.

Não crie arquitetura complexa.

Quando dados reais estiverem ausentes:

- utilize placeholders;
- centralize quando fizer sentido;
- não invente informações.

## Imagens

Prepare a implementação para:

- alt individual;
- aspect-ratio ou dimensões quando conhecidas;
- object-fit;
- lazy loading quando apropriado;
- substituição simples dos assets.

## Mobile

Não apenas empilhe o desktop.

Garanta:

- hierarquia;
- leitura;
- imagens relevantes;
- CTAs confortáveis;
- ausência de overflow;
- espaçamento adequado.

## Restrições

Não implemente:

- novas funcionalidades;
- bibliotecas desnecessárias;
- animações elaboradas;
- Final CTA;
- Footer;

salvo se `PROJECT.md` definir uma estrutura diferente.

Não faça commit.

## Validação

Execute:

npm run build
npm run lint
git diff --check

Depois informe:

1. seções implementadas;
2. arquivos criados e modificados;
3. decisões de composição;
4. placeholders;
5. pendências;
6. resultado das validações.

---

# 04 — Bloco 3: Final CTA + Footer

Implemente o **Bloco 3 do MVP: fechamento da landing page**.

Use `PROJECT.md`, `AGENTS.md` e o sistema visual existente.

Não altere as seções anteriores sem necessidade.

## Final CTA

Implemente o encerramento da jornada.

O objetivo é transformar o interesse construído ao longo da página na ação principal definida no `PROJECT.md`.

Priorize:

- headline;
- texto curto;
- CTA principal;
- hierarquia forte;
- composição coerente com o restante da página.

Evite copy comercial genérica.

Não invente:

- preços;
- promoções;
- disponibilidade;
- prazos;
- condições.

Use placeholders claramente identificáveis quando dados reais estiverem ausentes.

## Footer

Implemente somente informações existentes no projeto.

Pode incluir, conforme `PROJECT.md`:

- marca;
- contatos;
- redes sociais;
- localização;
- copyright.

Evite:

- sitemap desnecessário;
- newsletter não solicitada;
- formulários;
- links fictícios;
- políticas inexistentes.

## Ritmo global

Antes de concluir, revise as transições entre as seções.

Procure inconsistências evidentes em:

- containers;
- paddings;
- alinhamentos;
- fundos;
- espaçamento;
- largura de conteúdo.

Não faça redesign.

Não tente melhorar seções já aprovadas sem motivo concreto.

## Responsividade

Garanta comportamento coerente em:

- mobile;
- tablet;
- desktop.

## Restrições

- sem novas dependências;
- sem novas funcionalidades;
- sem animações elaboradas;
- sem commit.

## Validação

Execute:

npm run build
npm run lint
git diff --check

Depois informe:

1. arquivos criados e modificados;
2. decisões relevantes;
3. dados que continuam como placeholders;
4. resultado das validações.

Não faça commit.

---

# 05 — Auditoria final

Faça uma **auditoria técnica completa do MVP atual**.

## Regra principal

Trabalhe somente em modo de análise.

Não modifique arquivos.

Não corrija problemas.

Não instale dependências.

Não faça commit.

Quero primeiro um diagnóstico.

## Estrutura e código

Analise:

- organização;
- componentes;
- dados;
- duplicação;
- abstrações prematuras;
- código morto;
- imports não utilizados;
- assets antigos;
- arquivos remanescentes do template;
- consistência geral.

## Navegação

Verifique:

- Header;
- âncoras;
- ids;
- navegação mobile;
- CTAs;
- links internos;
- links externos.

## Conversão

Verifique todos os pontos relacionados ao CTA principal.

Confirme:

- destinos;
- consistência;
- dados centralizados;
- placeholders;
- comportamento dos links externos.

## Responsividade

Analise possíveis problemas aproximadamente em:

- 320px;
- 375px;
- 768px;
- 1024px;
- 1440px;
- telas maiores.

Procure:

- overflow;
- quebra inadequada de texto;
- imagens excessivamente grandes;
- containers inconsistentes;
- gaps problemáticos;
- elementos apertados;
- desalinhamentos;
- problemas de navegação.

## Acessibilidade

Verifique:

- HTML semântico;
- headings;
- textos alternativos;
- foco;
- contraste;
- navegação por teclado;
- ARIA somente quando necessária;
- propósito dos links;
- reduced motion.

Não recomende ARIA quando elementos HTML nativos já resolverem a necessidade.

## Imagens e performance

Verifique:

- lazy loading;
- LCP;
- dimensões ou aspect-ratio;
- layout shift;
- object-fit;
- assets;
- carregamentos desnecessários;
- estrutura preparada para imagens reais.

## SEO

Verifique:

- lang;
- title;
- meta description;
- viewport;
- Open Graph;
- favicon;
- heading principal;
- conteúdo indexável;
- canonical quando aplicável.

Identifique itens que dependem de domínio, assets ou dados reais.

## Placeholders

Liste TODOS os placeholders existentes.

Separe em:

### A. Obrigatório substituir antes de produção

[...]

### B. Pode permanecer durante desenvolvimento

[...]

## Limpeza

Identifique:

- assets sem uso;
- arquivos do template;
- comentários desnecessários;
- código morto;
- dados não consumidos.

Não remova nada nesta etapa.

## Validação

Execute:

npm run build
npm run lint
git diff --check

Não faça alterações para os comandos passarem.

Apenas reporte os resultados.

## Relatório

Classifique cada problema como:

### CRÍTICO

Impede funcionamento ou publicação.

### ALTO

Deve ser corrigido antes de produção.

### MÉDIO

Melhora qualidade, acessibilidade, SEO ou manutenção.

### BAIXO

Refinamento opcional.

Para cada problema informe:

- problema;
- arquivo ou local aproximado;
- impacto;
- correção recomendada.

Finalize respondendo:

1. **Pode publicar?**
2. **Correções obrigatórias antes de produção**
3. **Melhorias opcionais**
4. **Dados reais ainda necessários**

Não altere nenhum arquivo.

---

# 06 — Correções após auditoria

Use este prompt somente depois de revisar o relatório da auditoria e decidir quais itens realmente devem ser corrigidos.

Implemente apenas as correções aprovadas abaixo:

[COLE AQUI A LISTA DE CORREÇÕES APROVADAS]

## Regras

- não corrija itens não aprovados;
- não aumente o escopo;
- não faça redesign;
- não instale dependências sem necessidade;
- não substitua placeholders por informações inventadas;
- não refatore áreas não relacionadas;
- não faça commit.

## Validação

Ao terminar execute:

npm run build
npm run lint
git diff --check

Depois informe:

1. arquivos modificados;
2. arquivos removidos;
3. correções realizadas;
4. pendências restantes;
5. resultado das validações.

Não faça commit.