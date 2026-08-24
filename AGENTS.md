# AGENTS.md

## Fonte de verdade

Leia `PROJECT.md` antes de implementar mudanças relevantes.

Os requisitos, restrições e decisões descritos nele devem ser preservados.

Quando houver conflito entre uma suposição e o `PROJECT.md`, siga o `PROJECT.md`.

## Princípios

- Mantenha o projeto simples.
- Não adicione dependências sem necessidade.
- Não crie abstrações prematuras.
- Não invente conteúdo ou requisitos.
- Não aumente o escopo do MVP automaticamente.
- Não altere funcionalidades existentes sem verificar impacto.
- Reutilize padrões existentes.
- Priorize HTML semântico.
- Preserve acessibilidade.
- Preserve responsividade.
- Preserve consistência visual.
- Evite estilos inline sem justificativa.
- Evite código morto.
- Evite duplicação desnecessária.

## Antes de implementar

1. Leia `PROJECT.md`.
2. Leia os arquivos relacionados à tarefa.
3. Entenda o comportamento atual.
4. Verifique os padrões existentes.
5. Identifique a menor alteração necessária.

## Durante a implementação

- Trabalhe somente no escopo solicitado.
- Não faça redesign sem solicitação.
- Não refatore áreas não relacionadas.
- Não instale bibliotecas sem necessidade.
- Não substitua placeholders por informações inventadas.
- Preserve dados centralizados existentes.
- Evite modificar arquivos que não tenham relação direta com a tarefa.
- Se uma decisão importante estiver indefinida, informe antes de assumir uma solução que altere o produto.
- Quando houver mais de uma solução possível, prefira a mais simples que atenda aos requisitos atuais.

## Depois de implementar

Execute, quando disponíveis:

npm run build
npm run lint
git diff --check

Depois informe:

1. arquivos criados;
2. arquivos modificados;
3. arquivos removidos;
4. decisões relevantes;
5. placeholders ou pendências;
6. resultado das validações.

## Git

Não faça commit automaticamente.

Não faça push automaticamente.

Não altere branches sem solicitação.

O usuário decide quando uma etapa será registrada.

## Restrições padrão

Não adicionar sem solicitação explícita:

- backend;
- banco de dados;
- autenticação;
- CMS;
- painel administrativo;
- bibliotecas de UI;
- bibliotecas de animação;
- gerenciamento global de estado;
- novas páginas;
- integrações externas não previstas;
- funcionalidades fora do MVP.

## Frontend

Para projetos simples, priorize as ferramentas já existentes no projeto.

Não adicione bibliotecas para resolver problemas que possam ser resolvidos adequadamente com:

- React;
- JavaScript;
- HTML;
- CSS.

Crie componentes quando houver responsabilidade clara, reutilização real ou benefício evidente de organização.

Não fragmente a interface em componentes triviais sem necessidade.

## Responsividade

Trabalhe de forma mobile-first quando definido no `PROJECT.md`.

Evite:

- larguras fixas desnecessárias;
- margens manuais para corrigir alinhamentos;
- breakpoints criados apenas para esconder problemas estruturais.

Prefira:

- containers consistentes;
- grid;
- flexbox;
- `clamp()`;
- unidades relativas;
- layouts fluidos.

## Acessibilidade

Considere desde a implementação:

- HTML semântico;
- hierarquia correta de headings;
- foco visível;
- navegação por teclado;
- contraste;
- textos alternativos;
- reduced motion quando aplicável.

Não adicione ARIA quando elementos HTML nativos já fornecerem a semântica necessária.

## Imagens

Quando trabalhar com imagens:

- preserve proporções;
- utilize `object-fit` quando apropriado;
- use lazy loading fora da primeira dobra quando fizer sentido;
- evite layout shift;
- não invente `alt` definitivo quando a imagem real ainda não existir;
- mantenha substituição de assets simples.

## SEO

Para sites públicos, considere SEO básico:

- idioma;
- title;
- meta description;
- headings;
- Open Graph;
- conteúdo indexável;
- favicon quando disponível.

Não invente:

- domínio;
- canonical;
- URLs públicas;
- imagem Open Graph;
- dados estruturados não sustentados pelo projeto.

## Placeholders

Quando dados reais ainda não estiverem disponíveis:

- utilize placeholders claramente identificáveis;
- centralize dados que serão substituídos em vários locais;
- nunca apresente placeholders como conteúdo real;
- não invente depoimentos, contatos, preços, certificações ou informações do cliente.

## Qualidade

Priorize:

- legibilidade;
- manutenção;
- responsividade;
- acessibilidade;
- performance;
- SEO básico;
- simplicidade;
- consistência.

A solução mais sofisticada não é necessariamente a melhor solução.