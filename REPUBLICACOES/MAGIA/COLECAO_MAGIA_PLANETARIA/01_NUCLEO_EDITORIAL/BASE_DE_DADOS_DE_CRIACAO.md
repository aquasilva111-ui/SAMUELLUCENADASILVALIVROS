# Base de Dados de Criação — Núcleo de Republicações de Magia Planetária

**ID:** DB-NUC-MAGIA-REP-PLAN
**Data de criação:** 2026-10-17
**Última atualização:** 2026-10-17
**Versão:** 1.0
**Escopo:** exclusivamente MAG-REP-002 a MAG-REP-007.

## 1. Objetivo

Preservar a genealogia bibliográfica, textual, jurídica, visual e criativa de cada um dos seis livros. O banco deve permitir reconstruir o estado de qualquer projeto em qualquer data.

## 2. ENTIDADE PROJETO_REPUBLICACAO

Campos:
- projeto_id
- titulo_historico
- titulo_localizado
- autor_historico
- atribuicao_historica
- pseudonimos[]
- data_original
- periodo
- idioma_original
- tradicao
- funcao_no_nucleo
- descricao_integral
- valor_editorial
- estado
- nivel_decisao
- data_entrada
- data_update
- responsavel_direcao
- tradutores[]
- revisores[]
- produtos_planejados[]
- idiomas_planejados[]
- questoes_abertas[]
- arquivos_relacionados[]

## 3. ENTIDADE EDICAO_FONTE

- edicao_id
- projeto_id
- titulo_exato
- autor_creditado
- editor_historico
- tradutor_historico
- cidade
- editora
- ano
- idioma
- paginas
- formato
- identificadores_bibliograficos[]
- instituicao_detentora
- url
- data_consulta
- status_direitos_texto
- status_direitos_digitalizacao
- qualidade_scan
- paginas_faltantes[]
- defeitos[]
- fonte_da_verificacao
- data_verificacao
- observacoes

## 4. ENTIDADE TESTEMUNHO_TEXTUAL

- testemunho_id
- projeto_id
- sigla_editorial
- tipo: manuscrito | impresso | transcrição | edição crítica
- data
- idioma
- proveniencia
- relacao_com_outros_testemunhos[]
- confiabilidade
- lacunas[]
- variantes_relevantes[]
- status_uso

## 5. ENTIDADE TRANSCRICAO

- transcricao_id
- edicao_id
- projeto_id
- pagina_inicial
- pagina_final
- texto_diplomatico
- texto_normalizado
- caracteres_incertos[]
- notas[]
- responsavel
- metodo
- revisoes[]
- data_criacao
- data_update

Regra: nunca substituir leitura incerta por certeza sem registrar a intervenção.

## 6. ENTIDADE TRADUCAO

- traducao_id
- projeto_id
- edicao_fonte_id
- idioma_origem
- idioma_destino
- variante
- titulo_localizado
- texto_fonte_id
- tradutor
- versao
- literalidade
- politica_arcaismos
- politica_nomes
- politica_termos_tecnicos
- politica_transliteracao
- glossario_id
- ambiguidades[]
- notas[]
- revisoes[]
- revisao_humana
- status
- data_criacao
- data_update

## 7. ENTIDADE SEGMENTO_TEXTUAL

- segmento_id
- projeto_id
- localizacao_original
- capitulo
- secao
- paragrafo
- texto_fonte
- traducao_atual
- variantes[]
- notas_traducao[]
- notas_historicas[]
- entidades_mencionadas[]
- planetas[]
- materiais[]
- simbolos[]
- operacoes[]
- fontes_relacionadas[]
- status
- data_update

## 8. ENTIDADE CORRESPONDENCIA_PLANETARIA

- correspondencia_id
- projeto_id
- planeta
- categoria
- item
- formulacao_exata_da_fonte
- localizacao
- contexto
- edicao
- interpretacao_editorial
- divergencias_em_outros_textos[]
- confianca
- data_update

Categorias possíveis: metal, pedra, planta, animal, cor, número, imagem, anjo, espírito, inteligência, dia, hora, perfume, música, parte do corpo, função, operação, lugar, qualidade, símbolo, nome divino, pentáculo e outro.

## 9. ENTIDADE ENTIDADE_ESPIRITUAL

- entidade_id
- projeto_id
- nome
- variantes_nome[]
- classe
- planeta_associado
- fonte
- localizacao
- descricao_historica
- funcoes_atribuidas[]
- relacoes[]
- iconografia[]
- status
- observacoes

Regra: não fundir entidades de tradições distintas apenas porque compartilham planeta.

## 10. ENTIDADE RITUAL_OU_OPERACAO

- operacao_id
- projeto_id
- nome
- fonte
- localizacao
- planeta
- dia
- hora
- materiais[]
- palavras[]
- gestos[]
- diagramas[]
- finalidade_descrita
- condicoes[]
- notas_editoriais[]
- advertencias_historicas[]
- status

O banco é documental. Registrar prática histórica não equivale a afirmar eficácia sobrenatural.

## 11. ENTIDADE DIREITOS

- direitos_id
- projeto_id
- territorio
- componente
- objeto
- status
- base_da_avaliacao
- fonte
- data_verificacao
- prazo_ou_regra
- restricoes[]
- incertezas[]
- acao_necessaria
- revisado_por
- data_update

Componentes: texto original, tradução histórica, tradução moderna, edição crítica, imagem, fotografia, scan, restauração, capa, tipografia, prefácio, notas, índice.

## 12. ENTIDADE IMAGEM_HISTORICA

- imagem_id
- projeto_id
- edicao_id
- pagina
- tipo
- titulo
- legenda_original
- descricao_integral
- funcao
- planeta
- entidades[]
- simbolos[]
- dimensoes
- resolucao
- fonte
- status_direitos
- defeitos[]
- intervencao_permitida
- arquivo_original
- sha256
- data_importacao

## 13. ENTIDADE RESTAURACAO_VISUAL

- restauracao_id
- imagem_id
- projeto_id
- versao
- objetivo
- prompt_id
- intervencoes[]
- elementos_preservados[]
- elementos_reconstruidos[]
- incertezas[]
- ferramenta
- operador
- arquivo_resultado
- status_aprovacao
- data_criacao
- data_update

## 14. ENTIDADE PROMPT

- prompt_id
- projeto_id
- imagem_id
- funcao
- objetivo
- texto_original
- negative_prompt
- referencias[]
- elementos_obrigatorios[]
- elementos_proibidos[]
- fidelidade_exigida
- revisoes[]
- resultado_associado
- feedback_autoral[]
- status
- data_criacao
- data_update

Regra: Prompt V1 nunca deve ser sobrescrito.

## 15. ENTIDADE CAPA

- capa_id
- projeto_id
- idioma
- formato
- produto
- conceito
- hierarquia_textual
- titulo
- subtitulo
- credito_autor
- credito_editorial
- imagem_base
- prompt_id
- fontes_tipograficas
- paleta
- simbolos[]
- elementos_proibidos[]
- versao
- status
- data_update

## 16. ENTIDADE PARATEXTO

- paratexto_id
- projeto_id
- tipo
- autor
- titulo
- funcao
- texto
- fontes[]
- relacao_com_texto_historico
- status_autoria
- status_direitos
- data_update

Tipos: apresentação, introdução, ensaio, cronologia, nota editorial, nota de tradução, glossário, posfácio e índice.

## 17. ENTIDADE AFIRMACAO

- afirmacao_id
- projeto_id
- texto
- classe
- fonte
- localizacao
- autor_da_interpretacao
- confianca
- contradicoes[]
- status
- data_update

Classes: FATO BIBLIOGRÁFICO, FATO TEXTUAL, CONTEXTO HISTÓRICO, INTERPRETAÇÃO EDITORIAL, INTERPRETAÇÃO AUTORAL, HIPÓTESE, QUESTÃO ABERTA e SUGESTÃO DA IA.

## 18. ENTIDADE INDICE_PLANETARIO

- indice_id
- projeto_id
- planeta
- ocorrencias[]
- correspondencias[]
- entidades[]
- operacoes[]
- imagens[]
- notas[]
- comparacoes_com_outros_volumes[]
- data_update

## 19. ENTIDADE GLOSSARIO

- termo_id
- projeto_id
- termo_fonte
- variantes[]
- idioma
- traducao_adotada
- traducao_alternativa
- definicao_contextual
- ocorrencias[]
- decisao
- motivo
- data_decisao
- data_update

## 20. ENTIDADE DECISAO

- decisao_id
- projeto_id
- data
- pergunta
- opcoes[]
- decisao
- autor_da_decisao
- justificativa
- arquivos_afetados[]
- substitui_decisao
- status

## 21. ENTIDADE UPDATE

- update_id
- data
- projeto_id
- elemento
- estado_anterior
- novo_estado
- motivo
- origem
- aprovacao
- arquivos_afetados[]
- observacoes

## 22. REGISTROS INICIAIS

### MAG-REP-002 — Agrippa
Função: síntese de correspondências e magia celestial.
Fonte prioritária atual: edição inglesa de 1651 da Wellcome Collection.
Status inicial: candidato forte para transcrição, indexação e tradução.
Próxima ação: mapear estrutura do volume e todas as ocorrências planetárias.

### MAG-REP-003 — Heptameron
Função: tempo ritual, dias, horas, direções e anjos.
Fonte prioritária atual: material histórico de 1655 associado à tradução de Robert Turner.
Próxima ação: delimitar precisamente o texto dentro do volume que o preserva.

### MAG-REP-004 — Arbatel
Função: sete Espíritos Olímpicos e esferas planetárias.
Fonte prioritária atual: tradução inglesa de Robert Turner, 1655.
Próxima ação: mapear nomes, funções, planeta e estrutura dos aforismos.

### MAG-REP-005 — Key of Solomon
Função: pentáculos e operação planetária dentro da tradição salomônica.
Fonte prioritária atual: Mathers, 1889.
Próxima ação: inventariar pranchas e estabelecer política de reconstrução gráfica.

### MAG-REP-006 — De Vita
Função: magia natural, simpatia celeste, corpo, ambiente, música e matéria.
Fonte prioritária atual: códice de 1489 da Library of Congress/WDL.
Próxima ação: escolher fonte textual adequada para tradução e mapear o terceiro livro.

### MAG-REP-007 — Picatrix
Função: magia astral e talismânica medieval.
Trava: edição Pingree 1986 está em copyright.
Próxima ação: localizar fonte histórica ou edição juridicamente reutilizável antes de qualquer transcrição comercial.

## 23. Perguntas que a base deve responder

- Qual é a fonte de cada frase publicada?
- Qual edição sustentou uma tradução?
- Qual versão da tradução estava ativa em determinada data?
- Qual correspondência planetária aparece em qual página?
- Que correspondências divergem entre os seis livros?
- Qual imagem foi restaurada e com qual prompt?
- Que símbolo é histórico e que símbolo é criação moderna?
- O que está livre no território de publicação?
- O que ainda depende de licença?
- Que decisão veio de Samuel?
- Que proposta ainda é apenas possibilidade?
- Qual material foi alterado, quando e por quê?