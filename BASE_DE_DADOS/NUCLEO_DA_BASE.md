# Núcleo da Base de Dados de Criação

**Versão:** 2.1  
**Última atualização:** 2026-10-17  
**Função:** preservar produto final, processo criativo, genealogia das decisões, fontes, imagens, prompts, cânone e versões.

## Princípio central

O banco precisa permitir reconstruir **o que uma obra era em qualquer ponto do tempo**.

Nenhuma atualização importante deve apagar:
- versão anterior;
- origem;
- data;
- justificativa;
- nível de cânone;
- dependências narrativas ou conceituais.

## 1. ENTIDADE OBRA

Campos obrigatórios quando conhecidos:
- obra_id
- titulo_principal
- titulos_alternativos[]
- subtitulo
- autor
- idioma_titulo
- tipo
- universo
- colecao
- volume
- status_autoral
- nivel_canone
- data_criacao_conhecida
- data_primeiro_registro
- data_ultima_atualizacao
- premissa_integral
- tese_central
- problema_que_a_obra_investiga
- perguntas_centrais[]
- objetivos[]
- publico
- meta_palavras
- palavras_atuais
- descricao_longa
- notas_autorais[]
- core_visions_aplicavel
- tags[]
- obras_relacionadas[]
- material_origem[]

## 2. ENTIDADE UNIDADE_CRIATIVA

Representa qualquer fragmento ainda não consolidado:
- unidade_id
- obra_id
- tipo
- conteudo_integral
- resumo_funcional
- origem
- data_criacao
- data_registro
- nivel_canone
- autor_da_ideia
- relacoes[]
- posicao_atual
- status
- substitui_unidade_id
- substituida_por
- observacoes

Tipos possíveis:
premissa, personagem, relação, local, objeto, instituição, evento, cena, revelação, conflito, regra de mundo, mecanismo, teoria, conceito, símbolo, motivação, medo, desejo, segredo, setup, payoff, transformação, questão aberta, contradição, decisão autoral, hipótese, imagem, prompt, dado, fonte, citação curta, capítulo, beat, major beat.

Material sem posição vai para **MATERIAL NÃO POSICIONADO**.

## 3. ENTIDADE CAPÍTULO

- capitulo_id
- obra_id
- numero
- titulo
- parte
- funcao
- pergunta_central
- estado_inicial
- estado_final
- major_beats[]
- beats[]
- conceitos[]
- fontes[]
- imagens[]
- prompts[]
- status
- data_update

## 4. MAJOR BEAT

- major_beat_id
- titulo
- fundamento_pregresso
- estado_anterior
- transformacao
- estado_resultante
- beats_filhos[]
- setups_recebidos[]
- payoffs_entregues[]
- questoes_abertas[]
- funcao
- data_update

## 5. BEAT

Usar identificador estável, ex.: CAP3-02.04.

Campos:
- beat_id
- titulo
- fundamento_pregresso
- descricao_integral
- funcao
- classificacao_continuidade
- estado_anterior
- evento
- resultado
- novo_estado
- setup
- payoff
- personagens
- local
- objetos
- conceitos
- consequencias[]
- questoes_abertas[]
- fontes[]
- data_update

Classificação funcional:
- ABERTURA
- CONTINUAÇÃO
- TRANSFORMAÇÃO
- CONCLUSÃO

Um Beat pode exercer mais de uma função.

## 6. QUESTÃO NARRATIVA / INTELECTUAL

- questao_id
- obra_id
- pergunta
- tipo
- aberta_em
- desenvolvida_em[]
- transformada_em[]
- concluida_em
- payoff_pendente
- status
- data_update

## 7. CONVENÇÃO DE REALIDADE

- convencao_id
- entidade
- nome
- definicao
- tipo: Ideia-Crença ou Ideia-Símbolo
- origem: ferida, medo, esperança, valor, experiência formadora
- nucleos_associados[]
- nucleo_predominante
- gravidade
- evidencias[]
- momento_formacao
- relacoes[]
- contradicoes[]
- historico_transformacoes[]
- data_update

### Sete núcleos
1. Existencial — sobrevivência e segurança.
2. Criativo — desejo e transformação.
3. Identitário — identidade e poder.
4. Nutritivo — afeto e vínculos.
5. Expressivo — comunicação.
6. Intelectual — conhecimento e interpretação.
7. Propósito — sentido e pertencimento.

São categorias conceituais; não frequências físicas comprovadas.

## 8. PERSONAGEM / AGENTE

- personagem_id
- nomes[]
- obra_id
- papel
- periodo
- biografia_confirmada
- experiências_formadoras[]
- relações[]
- conhecimentos_por_periodo[]
- desejos[]
- medos[]
- segredos[]
- convenções_dominantes[]
- convenções_secundárias[]
- convenções_contraditórias[]
- convenções_adormecidas[]
- convenções_emergentes[]
- questões_abertas[]
- historico[]

Nunca usar conhecimento futuro numa cena anterior.

## 9. EVENTO / CENA — TRÊS CAMADAS

### Realidade factual
O que efetivamente aconteceu no cânone.

### Realidade interpretada
O que cada personagem, grupo ou instituição acredita que aconteceu.

### Realidade transformada
Que convenções, decisões, relações ou estados mudaram por causa do evento.

Campos:
- evento_id
- obra_id
- data_interna
- local
- participantes[]
- realidade_factual
- interpretacoes[]
- transformacoes[]
- fundamentos[]
- consequencias[]
- fontes[]
- status

## 10. CONCEITO / TEORIA

- conceito_id
- nome
- definicao_autoral
- problema_que_resolve
- mecanismo
- limites
- conceitos_relacionados[]
- primeira_ocorrencia
- exemplos[]
- contraexemplos[]
- evidencias[]
- hipoteses[]
- grau_de_evidencia
- status
- data_update

## 11. IMAGEM

- imagem_id
- obra_id
- caminho_arquivo
- nome_arquivo
- titulo
- funcao
- descricao_visual_integral
- intencao
- sensacao
- conceito_central
- cena
- personagem
- prompt_original
- prompt_atualizado
- negative_prompt
- ferramenta_modelo
- proporcao
- data_criacao
- data_importacao
- versao
- status_aprovacao
- referencia_de[]
- elementos_obrigatorios[]
- elementos_proibidos[]
- observacoes

## 12. PROMPT

- prompt_id
- obra_id
- imagem_id
- objetivo
- data_criacao
- texto_original
- revisoes[]
- termos_obrigatorios[]
- termos_proibidos[]
- referencias_visuais[]
- resultado_associado
- feedback_autoral[]
- versao_atual
- data_update

Prompts nunca devem ser sobrescritos sem histórico.

## 13. FONTE / REFERÊNCIA

- fonte_id
- obra_id
- titulo
- autor
- tipo
- url_ou_arquivo
- data_publicacao
- data_consulta
- função
- confiabilidade
- trecho_util
- fato_derivado
- interpretação_derivada
- hipótese_derivada
- observacoes

Separar:
**fato documentado → interpretação → inferência → hipótese → especulação.**

## 14. UPDATE

- update_id
- data
- obra_id
- elemento
- estado_anterior
- novo_estado
- motivo
- origem
- nivel_aprovacao
- arquivos_afetados[]
- observacoes

## 15. CONTRADIÇÃO

- contradicao_id
- obra_id
- versao_a
- origem_a
- versao_b
- origem_b
- impacto
- pergunta_de_resolucao
- status
- decisao_final
- data_decisao

Nunca escolher sozinho qual versão vale.

## 16. PROVENIÊNCIA

Toda informação deve ser rastreável sempre que possível para:
- fala direta de Samuel;
- arquivo importado;
- conversa;
- pesquisa externa;
- sugestão da IA;
- inferência editorial.

A proveniência impede que uma proposta antiga da IA seja promovida silenciosamente a decisão autoral.

## 17. CORE VISIONS

Quando aplicável:
- core_visions_aplicavel
- tom
- etapa_ativacao
- diagnostico
- modelo_core
- reconfiguracao
- integracao
- conceitos_nomeados[]
- paleta
- tipografia
- diagramas[]
- restricoes
- data_da_decisao

## 18. PROCESSO DE ABELHA

Visão → Extração → Perguntas → Decomposição → Organização → Registro → Lacunas → Atualização → Saturação → Esqueleto maduro.

A entrada pode ser desordenada. A organização não deve empobrecer a ideia.

## 19. MODO COLMEIA

Para obras extensas:
esqueleto provisório → entrevista progressiva → extração → atualização → nova entrevista → saturação.

Saturação não significa manuscrito finalizado.

## 20. Perguntas que o banco deve responder

- O que sabemos?
- O que ainda não sabemos?
- Quem definiu?
- Quando entrou?
- Em qual fonte?
- É cânone, hipótese ou sugestão?
- O que veio antes?
- Qual elemento causou este?
- Que questão continua aqui?
- Que versão era válida em determinada data?
- Onde uma ideia reaparece?
- Qual imagem/prompt pertence a qual conceito?
- Quais setups ainda não receberam payoff?
- Quais payoffs ainda não possuem setup?
- Quais contradições continuam abertas?


## 21. NÚCLEO EDITORIAL

**Adicionado em:** 2026-10-16

Campos:
- nucleo_editorial_id
- nome
- descricao
- escopo
- obras[]
- republicacoes[]
- subnucleos[]
- metodologias_aplicadas[]
- metodologias_nao_aplicadas_automaticamente[]
- identidade_visual
- regras
- data_criacao
- data_update

### Regra de segregação

Núcleo editorial, metodologia e universo não são sinônimos.

Exemplo confirmado em 2026-10-16:
- `NUC-MAGIA` é núcleo editorial;
- Core Visions é metodologia editorial independente;
- Beauty Trending é núcleo/linha independente;
- uma obra de Magia não herda Core Visions ou Beauty Trending sem decisão explícita.

## 22. REPUBLICAÇÃO / EDIÇÃO HISTÓRICA

**Adicionado em:** 2026-10-16

Campos:
- republicacao_id
- nucleo_editorial_id
- obra_historica
- autor_historico
- pseudonimo
- ano_base
- edicao_base
- idioma_original
- dominio_publico_status
- verificacao_por_territorio
- traducao_propria
- traducoes_localizadas[]
- concorrentes[]
- imagens_historicas[]
- prompts[]
- estrategia_multilingue[]
- produtos_planejados[]
- fatos_bibliograficos[]
- observacoes_de_mercado[]
- inferencias_editoriais[]
- hipoteses_comerciais[]
- questoes_abertas[]
- data_update

### Regra autoral

Republicar, traduzir, restaurar ou dirigir editorialmente uma obra histórica não transforma Samuel em autor do texto histórico. Registrar separadamente:
- autor histórico;
- tradutor;
- editor;
- diretor editorial;
- autor de introdução/notas, quando houver.

## 23. DIREITOS E PROVENIÊNCIA EDITORIAL

Campos:
- direitos_id
- entidade
- territorio
- texto_original_status
- traducao_status
- imagens_status
- paratextos_status
- fonte_da_verificacao
- data_verificacao
- incertezas[]
- restricoes[]

Regra:
**texto em domínio público ≠ tradução moderna em domínio público ≠ digitalização/imagem moderna automaticamente livre.**

## 24. OPORTUNIDADE EDITORIAL POR IDIOMA

Campos:
- oportunidade_id
- obra_id
- idioma
- variante
- edicoes_localizadas[]
- traducao_equivalente_localizada
- lacuna_percebida
- tamanho_de_mercado_estimado
- concorrencia
- diferencial
- prioridade
- força_da_evidencia
- data_da_pesquisa
- fontes[]
- status

Nunca registrar “não existe” quando a evidência é apenas “não foi localizado na busca”.

## 25. SUBBASE ESPECIALIZADA — REPUBLICAÇÕES DE MAGIA PLANETÁRIA

**Adicionada em:** 2026-10-17

Existe uma base de dados especializada em:
REPUBLICACOES/MAGIA/COLECAO_MAGIA_PLANETARIA/01_NUCLEO_EDITORIAL/BASE_DE_DADOS_DE_CRIACAO.md

Escopo fechado:
- MAG-REP-002 — Agrippa;
- MAG-REP-003 — Heptameron;
- MAG-REP-004 — Arbatel;
- MAG-REP-005 — Key of Solomon;
- MAG-REP-006 — De Vita;
- MAG-REP-007 — Picatrix.

A subbase expande as entidades gerais deste arquivo com testemunho textual, transcrição, segmento textual, correspondência planetária, entidade espiritual, ritual/operação, restauração visual, capa, paratexto, índice planetário e glossário.

Ela deve permanecer vinculada à base geral sem contaminar outros livros ou republicações com regras específicas da magia planetária.

**Última atualização desta integração:** 2026-10-17

## 25. ENTIDADES PARA ENSAIO FACTUAL

**Adicionado em:** 2026-10-17  
**Origem:** necessidades metodológicas de L001 — Sobrevivendo Abaixo da Linha Vermelha.

### 25.1 ZONA_MODELO
- zona_id
- obra_id
- nome
- definicao_autoral
- status: confirmado/provisório
- dimensoes[]
- critérios_entrada[]
- critérios_saida[]
- unidade_analise
- temporalidade
- exemplos[]
- contraexemplos[]
- dados_necessarios[]
- limitações[]
- data_update

### 25.2 DADO_METRICA
- dado_id
- obra_id
- conceito
- valor
- unidade
- população
- geografia
- período
- fonte_id
- definição_da_fonte
- transformação_aplicada
- incerteza
- limitações
- status_verificacao
- data_update

### 25.3 ALEGACAO
Serve para impedir que frase repetida vire fato por inércia.
- alegacao_id
- obra_id
- texto
- origem
- tipo: fato/interpretação/hipótese/metáfora/cenário
- evidencias[]
- evidencias_contrarias[]
- escopo
- confiança
- status: não verificada/verificada/parcial/rejeitada
- destinos_no_texto[]
- data_update

### 25.4 EXPERIENCIA_AUTORAL
- experiencia_id
- obra_id
- pessoa
- descrição_literal
- data_do_relato
- período_relatado
- contexto
- interpretação_do_autor
- inferências_editoriais_separadas[]
- pode_ser_publicado
- posição_estrutural
- status

Regra: nunca completar experiência autobiográfica com inferência da IA.

### 25.5 METODOLOGIA_DE_CLASSIFICACAO
- metodologia_id
- obra_id
- versão
- objetivo
- unidade_analise
- dimensoes[]
- indicadores[]
- pesos[]
- limiares[]
- regras_de_dados_ausentes
- regras_de_sobreposicao
- validações[]
- análise_de_sensibilidade
- limitações[]
- resultados[]
- data_update

### 25.6 CENARIO_DE_FUTURO
- cenario_id
- obra_id
- nome
- premissas[]
- mecanismos[]
- horizonte_temporal
- evidencias_de_base[]
- componentes_especulativos[]
- riscos[]
- alternativas[]
- status
- data_update

Regra: cenário futuro nunca deve ser escrito como descrição factual do presente.

## 26. MATRIZ EPISTEMOLÓGICA

Para obras de não ficção, toda afirmação importante deve poder ser classificada como:
1. experiência pessoal;
2. conceito autoral;
3. dado;
4. literatura externa;
5. interpretação;
6. hipótese;
7. cenário futuro.

A base deve preservar a passagem de uma categoria para outra. Uma hipótese só se torna fato documental após verificação; uma metáfora não se torna mecanismo científico por repetição.


## 27. SUBBASE ESPECIALIZADA — DISTRIBUIÇÃO DA SOBERANIA POLÍTICA

**Adicionada em:** 2026-10-17  
**Obra vinculada:** L025 — Teoria das Subdemocracias / Democracia Fracionada [títulos de trabalho]

Caminho:
`LIVROS/L025_TEORIA_DAS_SUBDEMOCRACIAS/01_NUCLEO_E_CANONE/SCHEMA_BASE_DE_DADOS.md`

Objetivo: medir, de maneira setorial e auditável, quanto do poder político é efetivamente controlável democraticamente e quais mecanismos de concentração ocupam o espaço restante.

Entidades especializadas:
- PAIS;
- SETOR;
- INDICADOR;
- OBSERVACAO;
- EVIDENCIA;
- FONTE;
- PERFIL_SETORIAL;
- MECANISMO_DE_PODER;
- DECISAO_METODOLOGICA;
- VERSAO_METODOLOGIA;
- AUDITORIA.

Regra epistemológica:
`fonte → evidência → indicador → setor → perfil nacional → incerteza → interpretação`.

A subbase não permite produzir percentuais nacionais diretamente por impressão. Toda classificação deve preservar versão metodológica, período, fontes, justificativa e margem de incerteza.

**Última atualização desta integração:** 2026-10-17


## 26. SUBBASE ESPECIALIZADA — L009 PSICOLOGIA DOS CHAKRAS: ESFERAS DE PODER

**Adicionada em:** 2026-10-17  
**Arquivo mestre:** BASE_DE_DADOS/L009_PSICOLOGIA_DOS_CHAKRAS.md

A subbase L009 especializa as entidades gerais desta base para registrar:

- Esfera de Poder;
- pergunta existencial;
- Virtudes;
- chakra;
- glândula;
- território corporal;
- psicologia;
- estados funcionais;
- compensações entre Esferas;
- Convenções de Realidade;
- Gravidade de Realidade;
- atividades de integração;
- história do chakra;
- deidades e cultos;
- práticas mágicas;
- Esferas Universais / Sephiroth;
- dimensão coletiva em passado, presente e futuro;
- pesquisas históricas, fisiológicas, psicológicas e religiosas;
- imagens e prompts visuais;
- versões de capítulo e migrações estruturais.

### Regra de proveniência do L009

A subbase deve distinguir explicitamente:
1. cânone autoral;
2. interpretação metafísica autoral;
3. tradição histórica;
4. fisiologia / ciência;
5. analogia funcional;
6. hipótese;
7. possibilidade editorial;
8. questão aberta.

O núcleo canônico específico vive em:
LIVROS/L009_PSICOLOGIA_DOS_CHAKRAS/01_NUCLEO_E_CANONE/NUCLEO_COMPLETO.md

O esqueleto vigente vive em:
LIVROS/L009_PSICOLOGIA_DOS_CHAKRAS/02_ESQUELETO/ESQUELETO_MESTRE_2026-10-17.md

O banco visual vive em:
LIVROS/L009_PSICOLOGIA_DOS_CHAKRAS/04_IMAGENS_E_PROMPTS/

**Última atualização desta integração:** 2026-10-17


## 26. Subbase específica — Magia Moderna (2026-10-17)

Local: `LIVROS/MAGIA_MODERNA_COMO_DOMINAR_SEUS_DAIMONS/01_NUCLEO_E_CANONE/BASE_DE_DADOS_DE_CRIACAO.md`.

Entidades: obra, unidade criativa, conceito, questão, imagem, prompt, proveniência, update. Os conceitos Daimon, Energeticum Petroleum, refinaria de alta tecnologia e domínio têm definições mínimas autorais e expansões propostas pela IA registradas separadamente. Origem das falas e prompts integrais documentados; vínculo interobras com L025 é referência, não fusão. **Data update:** 2026-10-17.


## 28. SUBBASE ESPECIALIZADA — MASCULINIDADE DETERMINISTA

**Adicionada em:** 2026-10-17  
**Obra vinculada:** L026 — A Masculinidade Determinista  
**Data autoral de origem da ideia:** 2026-08-31

Caminho principal:
LIVROS/L026_MASCULINIDADE_DETERMINISTA/01_NUCLEO_E_CANONE/BASE_DE_DADOS_DE_CRIACAO.md

Objetivo: preservar a genealogia completa do livro, distinguindo afirmações autorais, teses a investigar, conceitos do livro, hipóteses explicativas, propostas editoriais da IA, evidência externa futura e decisões de redação.

Entidades especializadas:
- TESE_AUTORAL;
- NORMA_DE_MASCULINIDADE;
- PROVA_DE_MASCULINIDADE;
- EXPERIENCIA_AFETIVA;
- EXPERIENCIA_EROTICA;
- MECANISMO_DE_VIGILANCIA_IDENTITARIA;
- CONFLITO_EGO_ALTEREGO_SUPEREGO;
- RELACAO_MULHER_COMO_VALIDACAO;
- RELACAO_ENTRE_HOMENS;
- ALEGACAO_PESQUISAVEL;
- CONTRAEXEMPLO;
- EVIDENCIA;
- HIPOTESE_DE_DESENVOLVIMENTO;
- IMAGEM_CONCEITUAL;
- PROMPT_VISUAL;
- DECISAO_AUTORAL;
- QUESTAO_ABERTA.

Regra epistemológica:
afirmação autoral → classificação → pergunta pesquisável → evidência favorável/contrária → delimitação → formulação editorial.

Regra especial: a proposição de que a maioria dos homens teria capacidade romântica de amar outro homem deve permanecer registrada como tese/proposição autoral a investigar até que a pesquisa delimite o que se entende por amor, capacidade romântica, orientação romântica, orientação sexual, intimidade, vínculo, desejo e população de referência.

Regra de linguagem: não transformar automaticamente afeto, admiração, intimidade, ternura, vínculo, desejo sexual, orientação sexual e orientação romântica em sinônimos.

Regra de psicologia conceitual: “ego”, “alter ego” e “superego” aparecem no material autoral como eixos úteis para organizar o conflito do homem com a masculinidade determinista. A obra ainda precisa decidir se serão vocabulário autoral, diálogo com tradições psicanalíticas ou metáfora estrutural.

Regra visual: imagens devem priorizar sensação e ideia, com símbolos legíveis de vigilância, prova, divisão interna, proximidade afetiva, julgamento social e identidade condicionada.

**Última atualização desta integração:** 2026-10-17


## 28. SUBBASE DE CRIAÇÃO — PRINCÍPIOS MÁGICOS DO MARKETING

**Adicionada em:** 2026-10-17  
**Obra:** MAG-AUT-003 — Princípios Mágicos do Marketing — Magia e Bruxaria Moderna  
**Caminho:** `LIVROS/PRINCIPIOS_MAGICOS_DO_MARKETING_MAGIA_E_BRUXARIA_MODERNA/01_NUCLEO_E_CANONE/BASE_DE_DADOS_DE_CRIACAO.md`

A subbase organiza de forma rastreável título autoral, tese proposta pela IA, matriz de analogias, 16 princípios candidatos, questões intelectuais, ética, imagens, prompts, evidência, fontes, versões e histórico. Regras: preservar fonte literal, não promover sugestões automaticamente a cânone e separar símbolos/metáforas de afirmações verificáveis. **Última atualização:** 2026-10-17.
