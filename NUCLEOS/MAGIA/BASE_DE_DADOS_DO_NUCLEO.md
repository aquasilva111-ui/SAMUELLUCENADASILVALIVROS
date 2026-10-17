# Base de Dados — Núcleo Magia

**Versão:** 1.1  
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


## ENTIDADE MAGIA_DAS_SOMBRAS

**Adicionada em:** 2026-10-17

Campos:
- magia_sombra_id
- obra_id
- planeta_arquetipo
- nome
- data_primeira_definicao
- virtude_original
- virtude_status
- deformacao_sombria
- objetivo
- objeto_de_captura
- mecanismo_principal
- formula_canonica
- mensagem_simbolica
- aplicacao_individual[]
- aplicacao_coletiva[]
- economia_psiquica[]
- principio_etico
- forma_virtuosa
- forma_virtuosa_status
- combinacoes_planetarias[]
- fatos_documentados[]
- interpretacoes_magico_simbolicas[]
- hipoteses[]
- questoes_abertas[]
- imagens[]
- prompts[]
- historico[]
- data_update

### Regra
Uma lacuna em virtude, mecanismo ou forma luminosa permanece lacuna. Não usar correspondências astrológicas gerais para completar automaticamente o sistema autoral.

## ENTIDADE FLUXO_DE_POTENCIA

Campos:
- fluxo_id
- obra_id
- fonte_da_potencia
- produtor
- tipo_de_potencia
- controlador
- mecanismo_de_controle
- mecanismo_de_extracao
- receptor
- ponto_de_concentracao
- forma_de_dependencia
- capacidade_de_saida
- impacto_na_autonomia
- camada_epistemica
- fontes[]
- status
- data_update

## ENTIDADE COMBINACAO_DE_SOMBRAS

Campos:
- combinacao_id
- forcas[]
- ordem_causal
- mecanismo_de_cada_forca
- interface_entre_mecanismos
- formula
- status_canone
- exemplos[]
- contraexemplos[]
- questoes_abertas[]
- data_update

### Combinação confirmada
**Saturno + Plutão:** dependência → impossibilidade de saída → extração → concentração → domínio.

### Combinações ainda não definidas
- Plutão + Netuno;
- Saturno + Netuno;
- Saturno + Plutão + Netuno.

## ENTIDADE CAMADA_EPISTEMICA_MAGIA

Valores:
- conceito_autoral;
- fato_documentado;
- análise_histórica_econômica_social;
- interpretação_magico_simbolica;
- hipótese;
- especulação;
- metáfora_símbolo.

Regra: não promover uma camada a outra sem fonte ou decisão autoral.

## Obras autorais adicionadas em 2026-10-17

### MAG-AUT-002
**Título:** Magia das Sombras Plutônica  
**ID original:** L026  
**Data conceitual:** 2026-09-02  
**Objetivo:** dominar/capturar riqueza e potência do outro.  
**Fórmula:** POTÊNCIA DO OUTRO → CONTROLE → EXTRAÇÃO → CONCENTRAÇÃO.  
**Estado:** base de criação detalhada ativa.

### MAG-AUT-003
**Título:** Magia das Sombras Netuniana  
**ID original:** L027  
**Data conceitual:** 2026-09-03  
**Objetivo:** dominar o livre-arbítrio.  
**Mecanismo:** alienação e isolamento.  
**Estado:** embrionário; fórmula detalhada e forma virtuosa abertas.

## Histórico adicional

- **2026-10-17:** criação das entidades especializadas de Magia das Sombras e integração de L026 e L027 ao NUC-MAGIA.
