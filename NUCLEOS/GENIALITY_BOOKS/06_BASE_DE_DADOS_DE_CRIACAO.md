# Base de dados criativa — Geniality Books
**Versão inicial:** 1.0
**Atualização:** 2026-10-17
**Status:** arquitetura operacional para registro incremental; complementa `BASE_DE_DADOS/NUCLEO_DA_BASE.md`, sem substituir a base geral.

## Chaves e entidades
**MARCA** — `brand_id=GB`; nome autoral; descrição literal; autor; coleções; público; data_primeiro_registro; data_update; decisões pendentes; direitos.
**LINHA** — `line_id=GB-01..GB-08`; nome_original; nome_normalizado_se_aprovado; profissão; escopo; status; proveniência; data_update.
**LIVRO** — `book_id`; line_id; título_original; título_final; idioma; idade_alvo; objetivos; capítulos; páginas; ISBN_se_existir; estado_editorial; revisão; data_update.
**SEÇÃO/BEAT** — `unit_id`; book_id; major_beat; descrição; fundamento_pregresso; objetivo; questão_que_abre_ou_resolve; resultado; duração/páginas; aprovação; data_update.
**CONCEITO_PROFISSIONAL** — `concept_id`; profissão; definição; nível_de_dificuldade; pré-requisitos; exatidão; risco; fonte; modo_visual; aplicação; data_update.
**ATIVIDADE** — `activity_id`; profissão; objetivo; materiais; idade; instruções; supervisão; segurança; aprendizado; aprovação.
**ILUSTRAÇÃO** — `asset_id`; livro; unidade; arquivo; prompt; estilo; dimensões; direitos; fonte_visual; aprovação; versão; data_update.
**PROMPT** — `prompt_id`; origem (autor/IA); corpo_integral; versão; arte_assoc; restrições; uso; data_update.
**FONTE** — `source_id`; obra; origem (fala/arquivo/fonte externa); data_da_fala; data_de_registro; evidência; grau de confiança; correções.
**DECISÃO** — `decision_id`; autor_da_decisão; elemento; estado_anterior; novo_estado; data; motivo; nível_canone; fonte.
**UPDATE** — `update_id`; arquivos; antes/depois; autor_de_mudança; data_update; status.

## Entradas iniciais verificadas da conversa
| line_id | nome original | origem | estado |
|---|---|---|---|
| GB-01 | Medical Geniality | fala autoral | confirmado como nome |
| GB-02 | Astronaut Geniality | fala autoral | confirmado como nome |
| GB-03 | Actors Geniality | fala autoral | confirmado como nome |
| GB-04 | Writers Geniality | fala autoral | confirmado como nome |
| GB-05 | Scientific Geniality | fala autoral | confirmado como nome |
| GB-06 | gastronomic geniality | fala autoral | confirmado como nome |
| GB-07 | fhashionistic geniality | fala autoral | confirmado como nome |
| GB-08 | PopArtistric Geniality | fala autoral posterior | confirmado como nome |

## Política de preservação
1. Cada fala autoral deve conservar termo, fonte e diferença de grafia/capitalização.
2. Nunca sobrescrever nome autoral com alternativa de nomenclatura da IA.
3. Cada sugestão do assistente fica rotulada e não entra no cânone automaticamente.
4. Uma proposta de livro não significa livro publicado ou capa criada.
5. Imagens precisam de ativo verificável, direitos e versões; prompts nunca equivalem a arte entregue.
6. Revisões científicas/clinicamente sensíveis devem ser feitas por especialistas humanos com fontes apropriadas.
7. Mudanças incrementais: só editar unidades afetadas, registrar data e preservar as anteriores.

## Relações
`GB` → oito linhas `GB-01..GB-08` → futuros livros → seções → conceitos/atividades → imagens/prompts/fontes.
`GB-01` ↔ `NUCLEOS/MEDICAL_GENIALITY`: relação temática e nominal; **não fusão**.

## Exemplo de entrada de unidade (proposta)
```json
{"unit_id":"GBM-07.02","book_id":"GB-01-BOOK-01-PROPOSTO","tipo":"atividade_interativa","descricao":"Perguntar o que importa saber sobre paciente fictício com febre","origem":"sugestao_IA","nivel_canone":"nao_aprovado","data_update":"2026-10-17"}
```
