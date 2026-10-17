# Schema da Base de Dados — L025

**Nome provisório:** Base de Distribuição da Soberania Política  
**Status:** núcleo técnico inicial  
**Última atualização:** 2026-10-17

Objetivo: permitir que cada afirmação quantitativa ou classificatória seja reconstruída a partir da evidência original.

## PAIS
pais_id; nome; iso2; iso3; região; sistema_constitucional; período; status_avaliacao; avaliadores[]; indice_democratico_simples; indice_democratico_ponderado; intervalo_incerteza; classificacao_provisoria; observacoes; data_update.

## SETOR
setor_id; codigo; nome; definicao; pergunta_central; peso_simples; peso_ponderado; racional_peso; status; data_update.

Setores iniciais: S01 eleitoral; S02 executivo; S03 legislativo; S04 judiciário; S05 econômico; S06 administrativo/regulatório; S07 informacional; S08 partidário; S09 territorial; S10 sociedade civil; S11 religioso; S12 coercitivo.

## INDICADOR
indicador_id; setor_id; nome; definicao_operacional; pergunta; direção; escala_min; escala_max; regra_0; regra_1; regra_2; regra_3; regra_4; fontes_preferenciais[]; mecanismo_associado[]; risco_dupla_contagem[]; status_metodologico; versão; data_update.

## OBSERVACAO
observacao_id; pais_id; indicador_id; periodo; valor_bruto; valor_normalizado; confiança; justificativa; codificador; data_codificacao; divergencia_entre_avaliadores; resolução_divergencia; status.

## EVIDENCIA
evidencia_id; observacao_id; tipo; descricao; fato_documentado; trecho_curto; dado_numerico; unidade; data_do_fato; fonte_id; interpretação; limitações; data_registro.

## FONTE
fonte_id; titulo; instituição; autor; url; arquivo; tipo; data_publicacao; data_consulta; cobertura_temporal; cobertura_geografica; metodologia_da_fonte; confiabilidade; conflito_de_interesse; observacoes.

## PERFIL_SETORIAL
perfil_setorial_id; pais_id; setor_id; periodo; score_democratico; intervalo_incerteza; plutocracia_score; oligarquia_score; aristocracia_score; teocracia_score; autocracia_score; partidocracia_score; burocratocracia_score; tecnocracia_score; militocracia_score; outro_score; método_de_agregação; notas; data_update.

## MECANISMO_DE_PODER
mecanismo_id; nome; definição; fonte_do_poder; forma_de_organização; mecanismo_de_reprodução; indicadores_relacionados[]; regras_de_exclusão[]; riscos_de_confusão[]; data_update.

## DECISAO_METODOLOGICA
decisao_id; assunto; pergunta; opções_consideradas[]; decisão_atual; status; autor_da_decisão; justificativa; data; substitui; substituida_por; arquivos_afetados[].

## VERSAO_METODOLOGIA
versão_id; numero; data; setores[]; indicadores[]; pesos[]; faixas[]; mudanças[]; motivo; compatibilidade_com_versões_anteriores; status.

## AUDITORIA
auditoria_id; pais_id; período; versão_metodologia; avaliador; problemas_encontrados[]; correções[]; score_antes; score_depois; data.

## Regra de imutabilidade histórica

Nunca sobrescrever silenciosamente score, regra de indicador, peso ou classificação. Quando a metodologia mudar, criar nova versão. Um país avaliado sob v0.1 deve continuar recuperável sob v0.1 após a criação de v0.2.

## Saídas previstas

- ficha nacional;
- comparador de países setor a setor;
- linha do tempo;
- atlas mundial com camadas;
- trilha de auditoria.

**Última atualização:** 2026-10-17
