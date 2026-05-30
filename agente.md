# Guia do agente - Fundacao Rede Brasil

Este arquivo orienta futuros agentes que forem trabalhar neste repositorio. Ele resume o contexto do projeto, as decisoes ja tomadas e os cuidados que devem ser preservados.

## Contexto do projeto

O projeto e um site estatico da Fundacao Rede Brasil, reposicionado como fundacao de apoio universitario. A comunicacao deve aproximar a instituicao de fundacoes de apoio que operam projetos de ensino, pesquisa, extensao, desenvolvimento institucional, ciencia, tecnologia e inovacao.

Referencia principal usada no trabalho: FAPUR. Tambem foram analisadas FAU, FUSP, FAIFCE, Fundacoes UFPel e referencias normativas sobre fundacoes de apoio.

O site publicado fica em:

- `https://venturajackson.github.io/Fundacaoredebrasil/`

## Estrutura atual

- `index.html`: pagina unica do site, com secoes institucionais, solucoes, portais, transparencia, noticias e contato.
- `styles.css`: estilos responsivos, paleta visual e layout.
- `script.js`: abertura/fechamento do menu mobile.
- `referencias.txt`: pesquisa e referencias que fundamentaram o reposicionamento.
- `.nojekyll`: arquivo para GitHub Pages publicar os arquivos estaticos sem processamento Jekyll.
- `fotos/logo-fundacao-rede-brasil.jpeg`: logo usada no cabecalho e rodape.
- `.github/workflows/`: pasta de workflows; conferir antes de alterar deploy.

## Posicionamento editorial

Tratar a Fundacao Rede Brasil como uma estrutura de apoio a projetos academicos. A linguagem deve ser institucional, clara e operacional, evitando tom generico de ONG ou pagina promocional.

Prioridades de conteudo:

- explicar o papel de uma fundacao de apoio universitario;
- destacar gestao de projetos, convenios, contratos, compras, bolsas, cursos, eventos e prestacao de contas;
- atender publicos distintos: coordenadores, fornecedores, sociedade, colaboradores e canais internos;
- reforcar transparencia, governanca, integridade e dados publicos;
- deixar claro quando algo e modelo, recomendacao ou conteudo pendente de confirmacao oficial.

Dados publicos ja usados:

- Razao social: Fundacao Rede Brasil.
- CNPJ: 13.407.204/0001-93.
- Natureza juridica: Fundacao Privada.
- Sede publica localizada: Itaguai/RJ.
- CNAE principal localizado: pesquisa e desenvolvimento experimental em ciencias sociais e humanas.

Nao afirmar instituicoes apoiadas, credenciamentos, homologacoes, dirigentes, e-mails, telefones, relatorios ou documentos oficiais sem fonte confirmada pelo usuario.

## Secoes esperadas no site

O site atual foi organizado com estas areas:

- Inicio: hero com promessa central de gestao de projetos academicos.
- Portais/acesso rapido: coordenador, fornecedor, sociedade e atendimento.
- A Fundacao: definicao, papel institucional e dados publicos.
- Solucoes: gestao de projetos, captacao, compras, bolsas/pessoas, cursos/eventos e prestacao de contas.
- Espaco do coordenador: fluxo de submissao, formalizacao, execucao e encerramento.
- Compras e fornecedores: editais, cotacoes, cadastro e regulamento.
- Transparencia: contratos, relatorios, demonstrativos, estatuto, codigo de etica, regularidade fiscal e ouvidoria.
- Noticias: comunicados institucionais, projetos e compras.
- Contato: formulario e atendimento por assunto.

Se novas paginas forem criadas, manter essa arquitetura de informacao e evitar duplicar conteudo sem necessidade.

## Direcao visual

A identidade observada na logo combina azul-marinho, verde e dourado. O site deve continuar com aparencia institucional, limpa e confiavel.

Diretrizes:

- manter foco no servico e na governanca, nao em uma landing page publicitaria;
- usar layouts densos, organizados e responsivos;
- preservar boa leitura em mobile;
- evitar excesso de efeitos decorativos;
- manter botoes e cards com raio pequeno, coerente com o estilo atual;
- garantir que textos longos quebrem sem estourar containers;
- usar a logo real do projeto como sinal visual principal.

O CSS atual usa variaveis em `:root` para cores e deve ser preferido antes de criar novas cores soltas.

## Stack e restricoes tecnicas

Este e um site estatico simples:

- HTML puro.
- CSS puro.
- JavaScript pequeno, sem framework.
- Publicacao por GitHub Pages.

Nao adicionar build step, bundler, framework ou dependencias sem necessidade real. Qualquer melhoria deve funcionar abrindo/publicando os arquivos estaticos diretamente.

## Cuidados de codificacao

O `index.html` atual mostra caracteres acentuados com mojibake em alguns pontos, apesar de declarar UTF-8. Antes de fazer grandes alteracoes textuais, verificar a codificacao do arquivo e preservar uma saida consistente.

Para novos arquivos de documentacao, preferir ASCII quando possivel. Para conteudo publico em portugues, acentos podem ser usados se o arquivo estiver salvo corretamente em UTF-8.

## Fluxo recomendado para alteracoes

1. Ler `referencias.txt` antes de alterar texto institucional.
2. Conferir `git status --short` para nao sobrescrever mudancas locais do usuario.
3. Fazer edicoes pequenas e focadas.
4. Validar visualmente em desktop e mobile quando alterar layout.
5. Conferir links, ancoras e menu mobile.
6. Se houver deploy, confirmar status do GitHub Pages e da pagina publicada.

Comandos uteis:

```powershell
git status --short
node --check script.js
```

Como nao ha build step, a validacao principal e abrir `index.html` ou a URL publicada e testar navegacao, responsividade e legibilidade.

## Pendencias e pontos sensiveis

Antes de publicacao oficial, o usuario deve confirmar:

- credenciamentos e homologacoes da fundacao;
- instituicoes apoiadas;
- diretoria, conselhos e governanca;
- estatuto, codigo de etica, demonstrativos, relatorios e regularidade fiscal;
- contatos oficiais por departamento;
- existencia real dos portais de coordenador, fornecedor, colaborador e transparencia;
- textos juridicos e institucionais finais.

Enquanto essas informacoes nao forem confirmadas, manter chamadas como modelo, recomendacao ou estrutura sugerida.

## Regra principal

Preservar o reposicionamento: Fundacao Rede Brasil como fundacao de apoio universitario orientada a projetos, transparencia, compras, prestacao de contas e atendimento a coordenadores, fornecedores e sociedade.
