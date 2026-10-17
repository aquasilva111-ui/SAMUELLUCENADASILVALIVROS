# Base de Dados — Núcleo Magia

**Versão:** 1.0  
**Data:** 2026-10-16  
**Última atualização:** 2026-10-17  
**Núcleo:** NUC-MAGIA

## Objetivo

Criar uma camada de dados especializada para livros de magia, astrologia histórica, ocultismo e republicações correlatas sem contaminá-la com regras de Core Visions ou Beauty Trending.

## ENTIDADE NUCLEO_MAGIA

Campos:

- nucleo_id
- nome
- data_criacao
- data_update
- descricao_integral
- escopo_confirmado[]
- escopo_provisorio[]
- obras_autorais[]
- republicacoes[]
- colecoes[]
- subnucleos[]
- metodologias_aplicaveis[]
- metodologias_nao_aplicadas_automaticamente[]
- regras_de_proveniencia[]
- regras_de_direitos[]
- identidade_visual[]
- historico[]

## ENTIDADE OBRA_MAGIA

- magia_obra_id
- obra_id_original
- titulo
- titulo_original
- autor
- autoria_tipo: autoral | histórica | tradução | edição
- categoria
- subnucleo
- natureza_editorial
- idioma_original
- idiomas_planejados[]
- data_original
- edicao_base
- dominio_publico_status
- verificacao_juridica
- texto_fonte
- imagens_fonte[]
- traducoes_modernas_localizadas[]
- concorrentes_editoriais[]
- oportunidade_editorial
- estrategia
- prompts[]
- imagens[]
- fontes[]
- fatos_documentados[]
- interpretacoes[]
- hipoteses[]
- questoes_abertas[]
- data_update

## ENTIDADE EDICAO_HISTORICA

- edicao_id
- obra_id
- ano
- titulo_exato
- autor_creditado
- pseudonimo
- editora
- cidade
- paginas
- formato
- proveniencia_exemplar
- digitalizacao
- url
- data_consulta
- observacoes
- confiabilidade

## ENTIDADE TRADUCAO

- traducao_id
- obra_id
- idioma
- variante
- titulo_de_trabalho
- fonte_de_traducao
- responsavel
- status
- glossario
- politica_de_arcaísmos
- politica_de_termos_astrologicos
- notas_editoriais
- revisão_humana
- data_update

## ENTIDADE DIREITOS

- direitos_id
- obra_id
- territorio
- texto_original_status
- traducao_status
- imagens_originais_status
- material_editorial_moderno_status
- observacoes
- fonte_verificacao
- data_verificacao

## ENTIDADE IMAGEM_MAGIA

Além dos campos gerais de imagem:

- origem_historica
- ano_da_imagem
- tipo: gravura | diagrama | página | capa | símbolo | recriação | capa_nova
- status_direitos
- fidelidade_historica
- restauração_permitida
- intervenções_realizadas[]
- legenda_editorial
- edição_relacionada

## ENTIDADE PROMPT_MAGIA

Além dos campos gerais:

- função: restauração | reconstrução | capa | diagrama | gravura | publicidade
- época_visual
- técnica_visual
- nível_de_fidelidade
- elementos_históricos_obrigatórios[]
- elementos_modernos_permitidos[]
- anacronismos_proibidos[]
- referência_primária[]
- resultado_associado

## ENTIDADE OPORTUNIDADE_EDITORIAL

- oportunidade_id
- obra_id
- idioma
- mercado
- concorrência_localizada
- lacuna_percebida
- evidência
- força_da_evidência
- prioridade
- estratégia
- riscos
- data_pesquisa
- status

## ENTIDADE COLECAO_MAGIA

- colecao_id
- titulo
- conceito
- escopo
- autores_históricos[]
- obras[]
- identidade_visual
- ordem_de_publicacao
- idiomas
- política_editorial
- status
- data_update

## Obras registradas em 2026-10-16

### MAG-AUT-001
**Magia da Paranoia: O Diabo Todo-Poderoso**  
Obra autoral. ID original L004.

### MAG-REP-001
**A Manual of Astrology, or The Book of the Stars**  
Robert Cross Smith / Raphael. Projeto de republicação e tradução histórica.

## Princípio de segurança do cânone

Uma descoberta bibliográfica não altera automaticamente a interpretação de uma obra autoral de Samuel.

Uma sugestão estética não altera automaticamente o texto.

Uma tradução moderna encontrada online não é fonte textual reutilizável sem análise de direitos.

Uma associação temática não muda automaticamente o núcleo de uma obra.

## Histórico

- **2026-10-16:** criação da estrutura NUC-MAGIA e separação explícita de Core Visions e Beauty Trending.


## Obra registrada em 2026-10-17

### MAG-AUT-002
**Título:** A Magia e Bruxaria Popular Sincrético-Moderna: O Quinto Elemento  
**Autor:** Samuel Lucena da Silva  
**Autoria:** autoral  
**Categoria:** metafísica / magia / filosofia espiritual / sincretismo / cultura espiritual contemporânea  
**Subnúcleo:** magia popular sincrético-moderna  
**Natureza editorial:** tratado narrativo de filosofia e metafísica mágica  
**Idioma-base:** português  
**Estado:** desenvolvimento avançado  
**Conceito editorial associado:** Magia às Massas  
**Local:** `LIVROS/MAGIA_E_BRUXARIA_POPULAR_SINCRETICO_MODERNA_O_QUINTO_ELEMENTO/`  
**Banco de dados dedicado:** `BASE_DE_DADOS/MAG_AUT_002_MAGIA_E_BRUXARIA_POPULAR_SINCRETICO_MODERNA_O_QUINTO_ELEMENTO.md`

### Escopo confirmado de MAG-AUT-002

- Deus/Fonte como centro de gravidade anterior aos nomes.
- axioma “Deus est deus, deus Est Deus”.
- Quinto Elemento/Éter como princípio de mediação, relação, tradução, circulação e integração.
- Rede Mercuriana e espiritualidade sincrética da internet.
- Reino Sincrético e sincretismo por função.
- Ciência Metafísica.
- Convenções de Realidade e Gravidade de Realidade.
- manifestação como passagem entre imagem, expectativa, vontade, comportamento e consequência.
- Fonte, Pléroma, Éons/Virtudes.
- Árvore da Vida como arquitetura das Esferas Universais.
- Árvore Inversa/Qliphoth como potência em desconexão.
- deuses como formas culturais de relação com o divino.
- anjos, daimons e especialização de potências.
- Energeticum Petroleum.
- passagem da Virtude à matéria e Magia às Massas.

### Regras de proveniência e cânone

- Diferenciar história documentada, tradição, interpretação, síntese autoral e hipótese metafísica.
- Não atribuir retroativamente sínteses modernas a tradições antigas.
- Não substituir termos autorais por terminologia mais convencional sem decisão de Samuel.
- Registrar datas, versões, prompts, imagens e mudanças de doutrina.
- Preservar o manuscrito-mãe e sua migração para os dois livros atuais.
- Não utilizar L025 ou L026 para esta obra; esses IDs já pertencem a outros projetos.

**Última atualização desta inclusão:** 2026-10-17
