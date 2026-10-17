# Núcleo da Base de Dados de Criação

**Versão:** 1.0  
**Última atualização:** 2026-10-16

A base deve preservar **produto final + processo de criação + genealogia das decisões**.

## 1. OBRA

Campos:
- obra_id
- titulo_principal
- titulos_alternativos[]
- subtitulo
- autor
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
- perguntas_centrais[]
- objetivos[]
- publico
- meta_palavras
- palavras_atuais
- descricao_longa
- notas_autorais[]

## 2. UNIDADE CRIATIVA

Qualquer material antes de encontrar posição definitiva:
- unidade_id
- obra_id
- tipo: premissa, personagem, relação, local, objeto, instituição, evento, cena, revelação, conflito, regra de mundo, mecanismo, teoria, conceito, símbolo, motivação, medo, desejo, segredo, setup, payoff, transformação, questão aberta, contradição, decisão autoral, hipótese, imagem, prompt
- conteúdo integral
- origem
- data
- nível de cânone
- relações
- posição atual
- status

Material sem lugar vai para **MATERIAL NÃO POSICIONADO**, nunca é descartado.

## 3. Processo de Abelha

Visão → Extração → Perguntas → Decomposição → Organização → Registro → Lacunas → Atualização → Saturação → Esqueleto maduro.

A entrada pode ser desordenada. Áudio, frase interrompida, correção e associação não são erros. A função da Abelhinha é organizar.

## 4. #esqueleto

Estrutura possível:
PROJETO → PARTES → CAPÍTULOS → MAJOR BEATS → BEATS → CENAS.

Não criar cenas artificiais para preencher simetria.

### Beat

Campos possíveis:
- beat_id estável, ex. CAP3-02.04
- título
- fundamento pregresso
- descrição
- função
- setup
- payoff
- personagens
- local
- consequências
- questões abertas
- data_update

Todo Beat precisa de razão para existir.

### Fundamento pregresso

Responder:
- Que coisa já estabelecida faz este Beat existir?
- Que questão anterior continua?
- Que promessa, problema ou consequência chega aqui?
- A unidade abre, continua, transforma ou conclui?

Se não houver antecedente localizado:
**Fundamento pregresso não localizado no material disponível.**

## 5. Convenções de Realidade

Cada convenção registra:
- identificador
- nome
- definição
- tipo: Ideia-Crença ou Ideia-Símbolo
- origem: ferida, medo, esperança, valor ou experiência formadora
- núcleos
- núcleo predominante
- gravidade
- evidências
- momento de formação
- relações
- contradições
- histórico de transformações

### Sete núcleos

1. Existencial — sobrevivência e segurança — O que ameaça sua existência?
2. Criativo — desejo e transformação — O que deseja criar?
3. Identitário — identidade e poder — Quem acredita ser?
4. Nutritivo — afeto e vínculos — Quem ama ou protege?
5. Expressivo — comunicação — O que consegue expressar?
6. Intelectual — conhecimento e interpretação — O que acredita ser verdadeiro?
7. Propósito — sentido e pertencimento — Por que acredita existir?

São categorias conceituais; não frequências físicas comprovadas.

## 6. Personagens

Cada personagem possui organização individual e histórico cronológico que nunca é apagado.

Registrar:
- experiências formadoras
- relações
- conhecimentos por período
- convenções dominantes
- secundárias
- contraditórias
- adormecidas
- emergentes
- lacunas

Nunca usar informação adquirida no futuro em cena anterior.

## 7. Eventos e cenas

Separar:
- **Realidade factual:** o que aconteceu.
- **Realidade interpretada:** o que cada personagem acredita.
- **Realidade transformada:** o que mudou em suas convenções.

## 8. Correções

Quando Samuel corrige:
ANTIGO → NOVO → DATA → ORIGEM → STATUS.

Não continuar usando a versão anterior, mas preservar que ela existiu.

Se duas versões conflitarem sem correção explícita:
**CONTRADIÇÃO A RESOLVER**
- Versão A
- Versão B
- origem/data
- decisão pendente

## 9. IMAGEM

Campos:
- imagem_id
- obra
- arquivo
- título
- função
- descrição visual integral
- intenção/sensação
- personagem/cena/conceito
- prompt original
- prompt atualizado
- negative prompt
- ferramenta/modelo
- proporção
- data
- versão
- aprovação
- observações

## 10. PROMPT

Guardar evolução:
- prompt_id
- obra
- objetivo
- original
- revisões
- termos obrigatórios
- termos proibidos
- referências visuais
- resultado
- feedback do autor
- data_update

## 11. FONTE / REFERÊNCIA

- referência
- tipo
- obra
- função
- confiabilidade
- trecho útil
- fato derivado
- interpretação
- hipótese derivada

Fato, interpretação e hipótese nunca devem colapsar no mesmo campo.

## 12. UPDATE

Cada mudança relevante:
- data
- obra
- elemento
- estado anterior
- novo estado
- motivo
- origem
- nível de aprovação
- arquivos afetados

## 13. Questões narrativas

- ID
- pergunta
- abertura
- desenvolvimentos
- transformações
- payoff
- status
- obras/capítulos associados

## 14. Modo Colmeia

Para muito material:
esqueleto provisório → entrevista progressiva → extração → atualização → nova entrevista → saturação.

Saturação = causalidade central compreensível, trajetórias principais definidas, setups/payoffs importantes com destino e questões restantes deliberadamente abertas. Não significa livro finalizado.

## 15. Banco deve conseguir responder

- O que sabemos?
- Quem definiu?
- Quando entrou?
- É cânone ou hipótese?
- O que veio antes?
- O que transformou?
- Onde reaparece?
- Qual imagem/prompt pertence?
- Qual versão era válida numa data?
