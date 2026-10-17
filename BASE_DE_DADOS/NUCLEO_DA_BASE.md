# Núcleo da Base de Dados de Criação

**Versão:** 2.0  
**Última atualização:** 2026-10-16  
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
