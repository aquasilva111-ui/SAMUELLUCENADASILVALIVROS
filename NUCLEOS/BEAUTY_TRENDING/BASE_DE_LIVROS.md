# Base de criação de livros — Beauty Trending

**Autor/criador:** Samuel Lucena da Silva  
**Última atualização:** 2026-10-16  
**Estado:** documentação editorial em desenvolvimento; decisões declaradas pelo criador separadas de recomendações da IA.

## Objetivo operacional

Construir catálogo multiproduto de ebooks Kindle, paperbacks e artigos derivados preservando a integridade de cada livro. Esta é uma **base de dados editorial estruturada em Markdown**, legível por pessoas, GitHub e agentes de IA; não é um banco SQL ativo nem publicação já realizada.

## Registro de projeto por livro

Criar pasta `LIVROS/BEAUTY_TRENDING/SLUG_DO_LIVRO/`, separando:

- `README.md`: identidade, autor, estágio e decisões.
- `NUCLEO.md`: tese, questão central, argumento, objeções, promessa de leitura.
- `MANUSCRITO.md`: texto preparado, com capítulos e status individual.
- `BEATS.md`: banco expansível de cenas/argumentos/etapas pelo Processo de Abelha.
- `PESQUISA.md`: fontes verificadas, detalhes bibliográficos, excertos limitados, dúvidas.
- `ESTILO.md`: arquétipo, voz, imagem sensorial, exemplos e proibições.
- `VISUAIS.md`: briefings de capa, miolo, variantes e atribuição/licenciamento.
- `KDP.md`: tamanho de corte, margens, sangria, prova, ISBN/opções, linguagem, direitos, descrição, categorias e metadados a confirmar.
- `HISTORICO.md`: decisões datadas e origem.

**Campos sugeridos para ficha de livro:** `id`, `titulo`, `subtitulo`, `serie`, `linha`, `idioma`, `autor`, `publico`, `arquetipo_primario`, `arquetipo_secundario`, `tese`, `pergunta_central`, `formato`, `status`, `versao`, `data_atualizacao`, `capitulos`, `fontes`, `artes`, `metadados_kdp`, `pendencias`.

## Níveis de decisão

**CONFIRMADO**: enunciado explícito do autor. **PROVISÓRIO**: formulação ainda ajustável. **POSSIBILIDADE**: direção exploratória. **QUESTÃO ABERTA**: sem definição. **SUGESTÃO DA IA**: proposta que não vira cânone automaticamente. Registrar decisões e alterações sem apagar versões anteriores.

## Fluxo editorial

1. Captura integral do material de Samuel; preservar datas e texto bruto.
2. Identificação da tese, público e promessa de leitura; mapear questões abertas.
3. Esqueleto/major beats/beat-by-beat conforme o método escolhido.
4. Pesquisa e checagem de fatos, inclusive contrapontos.
5. Redação autoral por capítulos em voz Beauty Trending.
6. Edição de argumento, estilo, consistência e inclusão.
7. Preparação de capa, imagens, direitos e especificações por formato.
8. Exportação e validação separada de ebook reflowable e miolo paperback.
9. Revisão de prova, metadados e checagem da plataforma antes de publicar.
10. Registrar edição publicada, data, arquivos-fonte e erratas.

## Projetos identificados nas conversas

- **Men Are Just Dudes — Demystifying Men in Modern Society:** título de trabalho, coleção Just for Men; tese sobre arquétipo da criança ferida, oportunidades de amadurecimento, acesso financeiro e suporte comunitário. Arquétipo editorial ainda não definido. **Status: conceito confirmado; estrutura não definida.**
- **Coleção por arquétipo:** ideia sugerida como estratégia de catálogo, **não confirmada** como oito livros encomendados.
- **Beauty Trending original:** marca/macrocoleção confirmada; títulos de ebooks específicos ainda a catalogar.

## Qualidade do arquivo e continuidade

Nunca sobrescrever uma versão sem histórico. Vincular todo visual ao livro/capítulo. Manter as referências de tendência como interpretação editorial salvo pesquisa externa. Evitar contagens arbitrárias de palavras como promessa; fazer arquitetura adequada ao conteúdo. A estrutura é expansível por livro sem duplicar manual de marca inteiro.
