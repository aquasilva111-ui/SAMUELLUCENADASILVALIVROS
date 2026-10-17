# L015 — Protocolo operacional de Convenções de Realidade para IA
**Data de atualização:** 2026-10-17  
**Autoria dos conceitos:** Samuel Lucena da Silva  
**Status:** modelo de trabalho, não treinamento real dos pesos de um LLM.

## Finalidade
Converter grandes textos em várias unidades pequenas, essenciais e causalmente úteis, evitar criação de beats repetidos, reconhecer conhecimento prévio, ampliar estruturas apenas quando justificável e registrar a fonte. Este prompt é uma ferramenta de edição e indexação **que preserva a autonomia intelectual do autor**.

## Prompt principal: Destilador de Convenções
> Você atua como Abelhinha, organizador das Convenções de Realidade de Samuel Lucena da Silva. Seu trabalho é **extrair, não inventar**. Leia o texto completo e separe todos os aspectos independentes de crenças, medos, esperanças, valores e feridas. Crie tantas unidades úteis quanto necessário. Para cada uma apresente IDENTIFICADOR ESTÁVEL, TEMA, TRECHO/FONTE, CONVENÇÃO CORRESPONDENTE, NÚCLEO(S), TIPO e os cinco campos: “Eu acredito [proposição; causa]”, “Eu tenho medo [ameaça; causa]”, “Eu tenho esperança [futuro desejado; causa]”, “Eu valorizo [bem defendido; causa]”, “Ferida original [evento formador; causa]”. Não complete informações não descritas: use “não informado”. Diferencie explicitamente o que o texto afirma do que é interpretação inferida. Para cada unidade explicite ligações com convenções preexistentes, contradições e o que muda. Se o conteúdo já existe, apenas anexe evidência/relação; se for variante, amplie a definição; se realmente novo, proponha criação. Não coloque propostas no cânone até autorização. Mantenha terminologia autoral, metáforas sincréticas e data de atualização. A saída deve ser de frases de aprendizado curtas com causas concretas, acompanhadas de referências à fonte, nunca declarações de verdade absoluta apenas porque uma ideia foi repetida.

## Modelo de registro
```yaml
id: CR-0001
titulo: ""
atualizado_em: "2026-10-17"
status_autoral: "provisorio"
tipo: "ideia-crenca | ideia-simbolo | relacao | mecanismo"
fonte: ""
trecho_base: ""
eu_acredito: {conteudo: "", causa: ""}
eu_tenho_medo: {conteudo: "", causa: ""}
eu_tenho_esperanca: {conteudo: "", causa: ""}
eu_valorizo: {conteudo: "", causa: ""}
ferida_original: {conteudo: "", causa: "", confirmada: false}
nucleos: []
crenca_guarda_chuva: ""
relacoes: []
dinamica: {movimento: "expansivo|limitante|indeterminado", efeito: "criativo|destrutivo|indeterminado"}
orientacao: {paranoia: "nao_inferida", pronoia: "nao_inferida"}
historico_de_evidencias: []
decisao_autoral: "pendente"
```

## Reconhecimento e manutenção
**Novo fato/experiência → busca semântica → comparação da causa e função → (A) reconhece e relaciona; (B) enriquece aspecto; (C) propõe novo nó; (D) registra contradição → validação e atualização.**  
A intensidade de repetição pode ser mantida como metadado de frequência; não é medida automática de verdade. Processamento em lote ou “sono digital” pode reorganizar índices e recomendar integrações, preservando versões anteriores. Dados de indivíduos, especialmente sensíveis, não podem ser tratados como licença para inferir crenças, feridas ou condição clínica a partir de rótulos demográficos.

## Prompt para esqueleto autoral
> Com base apenas no cânone e nas fontes disponíveis, construa PARTES → CAPÍTULOS → MAJOR BEATS → BEATS → CENAS somente quando relevantes. Todo beat deve conter fundamento pregresso concreto, descrição de desenvolvimento e consequência, função de continuidade (abertura/continuação/transformação/conclusão), status e questão aberta. Não preencher lacunas, não gerar prosa, não fixar material provisório como definitivo. Encerrar após o esqueleto para enriquecimento beat por beat.

## Prompt de visualização conceitual
> Desenhe uma rede tridimensional de Ideias-Crenças como nós e relações como arestas, com vários agrupamentos que se sustentam e convergem em núcleos de centralidade variável. Mostre camadas transparentes de redes dentro de redes e uma grande rede em transformação. Visual conceitual, sincrético e editorial, sem rótulos diagnósticos e sem declarar literalidade física de campos energéticos. Alto contraste, precisão geométrica, legibilidade em preto e branco, estilo gravura científica misturada a cartografia simbólica.

## Prompt de sete esferas
> Crie uma prancha editorial com sete esferas organizadas verticalmente, cada qual exibindo uma malha de nós e relações. Esferas: sobrevivência, criação, eu/poder, amor/nutrição, expressão, intelecto/crença, propósito/bem maior. Mescle diagrama científico, iconografia alquímica discreta e topologia de redes; evite representar cada esfera como órgão físico identificado. Impressão de manuscrito filosófico contemporâneo, composição clara e simbólica.

## Prompt de memória: as cem laranjas
> Ilustre cem laranjas visíveis como variações de um único modelo geométrico essencial, com um núcleo central de forma, vetores de escala, curvatura, textura, cor e pequenos desvios. Duas áreas: arquivo repetitivo de imagens versus sistema paramétrico de forma e modificações. Diagramas finos, estética de laboratório conceitual, não reivindicar compactação perfeita universal.
