# Arquitetura de banco de dados e rastreabilidade do conteúdo
**Atualização:** 2026-10-16
**Tipo:** especificação proposta em Markdown/JSON, sem servidor ou banco de dados operacional neste momento.

## Objetos
**PROJECT** — MG-ROOT; visão, autor, escopo, versões.
**TRACK** — MG-TRK-FOUNDATIONS, MG-TRK-SPECIALTIES, MG-TRK-CASES, MG-TRK-EXAMS.
**DISCIPLINE** — MG-DIS-XXXX: disciplina mãe e área acadêmica.
**SUBDISCIPLINE** — MG-SUB-XXXX: domínio dentro de disciplina; pode compartilhar relações.
**SPECIALTY** — MG-SPE-XXXX: campo clínico; integra múltiplas disciplinas.
**PLAYLIST** — MG-PL-XXXX: ordenação editorial de unidades, com status de publicação.
**LESSON** — MG-LES-XXXX: aula canônica, parte de uma ou mais playlists.
**CONCEPT** — MG-CON-XXXX: princípio/fenômeno com definição, limites e referências.
**MECHANISM** — MG-MEC-XXXX: cadeia causal com setas tipadas e níveis de evidência.
**CASE** — MG-CAS-XXXX: caso clínico ficcional, composto ou adequadamente licenciado.
**EXAM** — MG-EXA-XXXX: organismo, exame, país, etapa, blueprint, edição.
**QUESTION** — MG-QUE-XXXX: item didático, origem/licença e racionales.
**ASSET** — MG-AST-XXXX: imagem/diagrama/vídeo/prompt com proveniência.
**SOURCE** — MG-SRC-XXXX: guideline/artigo/livro, citação, URL/DOI, data e versão.
**REVIEW** — MG-REV-XXXX: revisão científica e editorial.
**DECISION** — MG-DEC-XXXX: declaração autoral explícita com data e fonte.

## Relações principais
PLAYLIST inclui LESSON; LESSON explica CONCEPT; CONCEPT fundamenta MECHANISM; CASE evidencia ou desafia mecanismos; QUESTION avalia conceitos e habilidades; EXAM agrupa questões; ASSET ilustra aulas ou conceitos; SOURCE apoia claims específicos; REVIEW aprova versões; DECISION determina status de escolhas editoriais.

## Campos de status
- `confirmed_author`: Samuel afirmou diretamente.
- `direction_accepted`: Samuel aceitou a direção geral, não cada detalhe.
- `assistant_proposal`: opção da IA pendente de aprovação.
- `example_only`: usado apenas para explicar.
- `open_question`: sem decisão.

## Modelo YAML de aula
```yaml
id: MG-LES-0001
titulo: "Exemplo: hipercalemia e eletricidade celular"
estado: example_only
created_at: "2026-10-16"
updated_at: "2026-10-16"
idioma: pt-BR
playlists: []
disciplinas: ["fisiologia", "nefrologia", "farmacologia"]
objetivos: []
conceitos: []
mecanismos: []
casos_relacionados: []
exames_relacionados: []
assets: []
referencias: []
revisao_cientifica:
  status: pendente
  revisor: null
  data: null
historico:
  - data: "2026-10-16"
    acao: "Modelo cadastrado; aula não publicada"
```

## Protocolo de evolução
1. Registrar ideia na íntegra e sua atribuição; não apagar fonte original.
2. Extrair entidades e relações; preservar ambiguidade e separar decisões de propostas.
3. Criar ficha com ID estável, conectando disciplina, subdisciplina, especialidade, caso, prova e materiais visuais.
4. Acrescentar pesquisas e fontes verificáveis sem reescrever retroativamente o que Samuel disse.
5. Solicitar validação do autor para decisões de identidade e estrutura.
6. Revisão científica por profissional habilitado e validação das fontes antes da publicação.
7. Guardar versões e changelog; corrigir com histórico, não silenciosamente.
8. Permitir formatos futuros de publicação e automação sem perda da rastreabilidade.

## Log inicial
- **2026-10-16** — núcleo Medical Geniality organizado a partir desta conversa, como documentação de concepção. Quatro eixos e a integração por mecanismos são registrados com seus níveis de certeza.
