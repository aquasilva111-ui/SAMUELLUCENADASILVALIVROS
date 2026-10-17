# Identidade visual e prompts de criação
**Atualização:** 2026-10-16
**Status:** proposta visual do assistente; Samuel ainda não aprovou uma estética oficial do Medical Geniality.
**Nota:** não há imagem-fonte autoral fornecida neste diálogo, portanto não fingir que capa ou mockup definitivo foi criado ou escolhido.

## Direção visual candidata — “anatomia causal”
O diferencial é visualizar o conhecimento como arquitetura navegável: redes neurais e fisiológicas, sequências causais, organismos em múltiplas escalas, lâminas biomédicas e desenhos anatômicos de precisão. O layout deve facilitar leitura, revisão e acessibilidade antes de qualquer ornamento. Infográficos devem distinguir mecanismo comprovado, hipótese e correlação; marcadores de eixo e legendas sempre necessários quando exigidos cientificamente.

## Sistema gráfico proposto
- **Hierarquia:** pergunta → mecanismo → manifestação → evidência → decisão → revisão.
- **Composição:** ilustração estrutural do órgão ao centro; linhas finas conectam detalhe microscópico e efeito sistêmico; zonas laterais para legendas.
- **Tipografia:** sem serifas de alta legibilidade em aulas, detalhes discretos monoespaçados para parâmetros; cuidado com símbolos gregos e unidades.
- **Paleta candidata, não oficial:** azul profundo, ciano moderado, marfim e cor de acento âmbar; contraste validado para daltonismo.
- **Formatos:** vídeo 16:9, miniatura 16:9, esquema vertical 9:16, caderno A4 e SVG escalável.
- **Ética:** não utilizar fotos de pacientes identificáveis, imagens clínicas inventadas apresentadas como reais, sinais de instituições ou logos de exames sem permissão.

## Prompt mestre — aula visual
> Criar ilustração educacional original para “Medical Geniality”, com rigor anatômico, aparência editorial premium, didática e acessível. Fenômeno: [FENÔMENO]. Demonstrar estrutura normal, perturbação, mecanismo causal e manifestações em painéis conectados. Hierarquia impecável, espaço livre para rótulos revisados por humano, cortes anatômicos coerentes, ausência de órgãos duplicados ou vasos inventados, informação visual sem sensacionalismo. Fundo escuro discreto com acentos ciano e âmbar (cores provisórias). Composição 16:9, alta resolução; separar artisticamente arte de evidência científica; não inserir texto pequeno gerado automaticamente.

## Prompt — anatomia por camadas
> Ilustração biomédica original de [ÓRGÃO/SISTEMA], em três escalas: anatomia macroscópica, detalhe histológico e processo celular. Estruturas proporcionais, localização correta e setas discretas para posterior legenda manual; iluminação científica controlada, clareza superior ao realismo decorativo. Não criar estruturas não verificadas. Layout 16:9.

## Prompt — diagrama causal
> Diagrama de educação médica sobre [PROCESSO] com trilha ordenada de eventos [A] → [B] → [C] → [D], ramificações, feedback positivo/negativo quando confirmados e legenda de diferentes tipos de relação (causa, associação, hipótese). Vetorial, minimalista e legível. Reservar rótulos para diagramação revisada.

## Prompt — caso clínico interativo
> Interface conceitual original “Clinical Cases” para Medical Geniality. Painel de apresentação de caso fictício, dados revelados progressivamente, blocos separados para informações conhecidas, hipóteses do aluno, diagnósticos diferenciais e novo achado. Não exibir nome, rosto nem identificador de paciente real. Contraste forte, tipografia editorial, funcional em desktop e celular.

## Prompt — questão de prova
> Composição gráfica 16:9 para “Medical Geniality — Exams”. Questão didática original em primeiro plano, áreas de pistas, mecanismo necessário, justificativas de alternativas e um contrafactual. Não copiar interfaces oficiais nem usar marcas de certificadoras. Distinções visuais entre resposta respaldada, interpretação e dúvida.

## Prompt — capa de playlist
> Criar thumbnail original de playlist Medical Geniality, disciplina [DISCIPLINA], tópico [TÓPICO]. Um elemento anatômico ou conceitual central cientificamente plausível, aspecto elegante de atlas médico contemporâneo, detalhe técnico controlado, fundo limpo, contraste alto, espaço para título inserido em pós-produção, sem rosto de paciente real, formato 16:9.

## Prompt — livro/caderno futuro
> Capa editorial para eventual caderno Medical Geniality sobre [ASSUNTO], mantendo fidelidade a [DIREÇÃO VISUAL APROVADA], ilustração original com anatomia respeitada, título legível em português e linguagem visual consistente com playlists e cases. Mockup não é anúncio de livro existente.

## Controle de qualidade de imagens
Cada peça precisa ter `asset_id`, `prompt_version`, `autor_da_arte`, `licenca`, `conteudo_clinico_revisado`, `referencias`, `atualizado_em` e local no repo. A imagem produzida por IA nunca será a única autoridade sobre a anatomia ou a fisiopatologia.
