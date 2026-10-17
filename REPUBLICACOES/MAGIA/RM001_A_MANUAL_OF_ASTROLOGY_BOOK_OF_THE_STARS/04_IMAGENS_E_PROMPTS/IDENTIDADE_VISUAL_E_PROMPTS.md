# Imagens e Prompts — RM001

**Data:** 2026-10-16  
**Status:** direção visual inicial.

## 1. Referências históricas a capturar

### IMG-RM001-001 — Folha de rosto de 1828
**Fonte de referência:** Google Books, edição VL1CAAAAYAAJ.  
**Função:** genealogia visual e bibliográfica.  
**Status do arquivo:** referência externa registrada; imagem binária ainda não importada para o repositório.

### IMG-RM001-002 — Capa / encadernação de reprints históricos
**Função:** pesquisa de evolução editorial.  
**Status:** coletar apenas com proveniência e direitos claros.

### IMG-RM001-003 — Diagramas astrológicos
**Função:** restaurar legibilidade sem alterar informação.

### IMG-RM001-004 — Três gravuras mencionadas no título histórico
**Função:** localizar na cópia-base, identificar páginas, autoria quando possível e preservar.

### IMG-RM001-005 — Capa nova PT-BR
**Função:** principal peça comercial da primeira tradução.

## 2. Direção visual da edição brasileira

A capa deve transmitir simultaneamente:

- livro histórico;
- autoridade documental;
- astrologia;
- beleza editorial;
- sensação de biblioteca rara;
- clareza contemporânea.

Evitar parecer:
- livro genérico de horóscopo;
- romance de bruxa;
- fantasia YA;
- produto New Age de banco de imagem;
- extensão de Beauty Trending;
- extensão de Core Visions.

## 3. Prompt — capa PT-BR clássica

> Design a premium Brazilian Portuguese cover for “Manual de Astrologia, ou O Livro das Estrelas”, a restored edition of Robert Cross Smith’s 1828 astrological manual published under the name Raphael. Create a historically grounded early-19th-century British celestial engraving aesthetic. Central zodiac wheel with astronomically coherent geometry, refined planetary glyphs, small engraved stars, archival paper texture, elegant ornamental border inspired by Georgian book design, sophisticated serif title hierarchy, reserved space for “Robert Cross Smith — Raphael”. Scholarly, mysterious and collectible rather than fantasy. High editorial credibility. No stock-photo mystic, no tarot deck, no random pentagram, no neon, no modern horoscope app aesthetic.

## 4. Prompt — capa luxo midnight

> Collector’s hardcover edition of “Manual de Astrologia, ou O Livro das Estrelas”. Deep midnight book-cloth appearance, restrained gold-foil celestial sphere, twelve zodiac signs arranged in exact radial geometry, fine engraved star field, small planetary glyphs, nineteenth-century ornamental framework, authoritative rare-library mood, minimal but monumental composition, premium publishing photography simulation, no fantasy illustration, no glowing crystals.

## 5. Prompt — folha de rosto reinterpretada

> Reconstruct a clean typeset title page inspired by an 1828 British astrology manual. Preserve the long-form hierarchical structure typical of period title pages, centered serif typography, generous spacing, small ornamental celestial vignette, black ink on warm ivory paper. Do not imitate damaged scan artifacts. Do not invent historical publisher information. Leave exact bibliographic lines as editable text placeholders.

## 6. Prompt — restauração de diagrama

> Restore an early nineteenth-century astrological diagram from a scanned public-domain source. Preserve every line, number, label, house division, zodiac glyph and geometric relationship. Remove stains, page yellowing and scanning noise only when they do not carry information. Do not modernize the diagram, do not redraw ambiguous glyphs from guesswork, flag illegible sections for manual review. Black engraved lines on neutral archival background, print-ready resolution.

## 7. Prompt — anúncio editorial

> Editorial launch poster for a restored 1828 astrology classic in Brazilian Portuguese. Feature the new book standing beside a faint archival reproduction of the original title page, celestial engraving motifs, elegant scholarly composition, premium dark-library atmosphere, clear headline “Uma obra de 1828 finalmente preparada para uma nova geração de leitores em português”. Avoid sensational occult horror language.

## 8. Negative prompt

- illegible AI typography;
- incorrect zodiac glyphs;
- excess gold;
- neon purple;
- crystal ball cliché;
- tarot cards;
- Wiccan symbols without historical basis;
- random alchemy glyphs;
- witch silhouette;
- gothic castle;
- modern observatory;
- modern telescope in period engraving;
- Beauty Trending cosmetics editorial language;
- Core Visions neural/psychological diagrams.

## 9. Política de restauração

Existem três estados distintos:

### Restauração
Limpa dano visual sem alterar a composição.

### Reconstrução
Redesenha elemento existente com base em referência suficiente.

### Reinterpretação
Cria uma nova peça inspirada no material histórico.

Nunca chamar uma reinterpretação de “imagem original restaurada”.

## 10. Arquivos futuros

Quando as imagens forem importadas, nomear:

- `1828_title_page_source_[origem].jpg`
- `1828_engraving_01_source_[origem].jpg`
- `1828_diagram_[pagina]_source_[origem].jpg`
- `1828_title_page_restored_v01.png`
- `ptbr_cover_concept_v01.png`
- `ptbr_cover_final_v01.tif`

Manter checksum, origem, data de importação e licença/estado de direitos no banco.
