# Plano de Dados e Verificação

**Obra:** L001  
**Criado em:** 2026-10-17  
**Última atualização:** 2026-10-17  
**Status:** plano de pesquisa; nenhum número deve ser tratado como validado por este documento.

## 1. Objetivo

Construir base empírica suficiente para:
- definir zonas;
- testar o modelo;
- estimar população por zona;
- evitar estatísticas inventadas/herdadas;
- separar correlação, associação, causalidade e metáfora;
- sustentar capítulos sem transformar o livro em relatório técnico ilegível.

## 2. Famílias de dados necessárias

### População e pobreza monetária
Usar como referência, não como definição completa da Linha Vermelha.

### Segurança alimentar
Necessária para capturar insuficiência que renda monetária pode ocultar.

### Habitação
Custo, adequação, risco de perda, informalidade, superlotação.

### Trabalho
Formalidade, desemprego, subemprego, volatilidade, proteção.

### Saúde
Acesso, gasto do bolso, adiamento por custo, vulnerabilidade a choque.

### Serviços básicos
Água, saneamento, energia, transporte e conectividade quando pertinente.

### Dívida e reserva
Particularmente importante para diferenciar “aparência de segurança” de capacidade de absorção.

### Choques e resiliência financeira
Perguntas de pesquisas domiciliares sobre capacidade de enfrentar despesas inesperadas podem ser muito valiosas.

### Tempo
Carga de trabalho, deslocamento e cuidado podem mostrar custo não monetário de manutenção.

## 3. Fontes institucionais candidatas a pesquisar

Estas são **fontes candidatas**, não dados já importados:
- Banco Mundial;
- Nações Unidas / UNDP;
- FAO;
- ILO/OIT;
- OMS/WHO;
- UNICEF;
- OCDE onde aplicável;
- Eurostat para países europeus;
- institutos estatísticos nacionais;
- pesquisas domiciliares nacionais;
- bancos centrais e pesquisas de finanças familiares;
- bases de custo de moradia e condições habitacionais reconhecidas.

Registrar para cada uso:
fonte, tabela, ano, cobertura, definição, unidade, metodologia, revisão, link e data de consulta.

## 4. Matriz mínima por indicador

Cada indicador deve ter:
- ID;
- nome;
- conceito medido;
- unidade;
- população-alvo;
- ano;
- geografia;
- fonte primária;
- periodicidade;
- comparabilidade internacional;
- lacunas;
- se é individual ou domiciliar;
- transformação aplicada;
- função no modelo;
- peso provisório;
- justificativa;
- sensibilidade.

## 5. Problema de sobreposição

Não somar:
“X milhões com insegurança alimentar” + “Y milhões em moradia inadequada”
como se fossem pessoas distintas.

Precisamos de uma das abordagens:
- microdados combinados;
- estimativa de interseções;
- cenários de limite inferior/superior;
- classificação por país usando múltiplos indicadores agregados;
- restrição da métrica aos países com dados combináveis.

## 6. Poder de compra e custo local

Um corte em dólares pode ser útil, mas não é suficiente.

Testar:
- PPP;
- custo de cesta básica;
- custo de moradia;
- renda disponível após essenciais;
- índices locais;
- limiares nacionais;
- combinação de absoluto + relativo.

## 7. Estabilidade longitudinal

Idealmente o índice deve capturar:
- probabilidade de queda;
- número de meses de reserva;
- histórico recente de choques;
- volatilidade de renda;
- reincidência em insegurança.

Se dados longitudinais globais forem insuficientes, declarar a limitação.

## 8. Capítulo de contabilidade

Estrutura metodológica possível:
1. explicar por que renda isolada não basta;
2. apresentar dimensões;
3. construir regras;
4. calcular país por país;
5. mostrar intervalo global;
6. apresentar mapa/tabela;
7. testar cenários;
8. mostrar limitações;
9. permitir atualização futura.

## 9. Regra de linguagem

Evitar:
- “prova que” quando há associação;
- “causa” quando estudo é correlacional;
- “o cérebro faz” como generalização sem população/condição;
- “bilhões” sem referência;
- extrapolar estudo local para espécie humana.

Preferir:
- “neste conjunto de dados...”;
- “o estudo encontrou...”;
- “a estimativa sugere...”;
- “o modelo classifica...”;
- “não há dados suficientes para...”.

## 10. Auditoria científica prioritária da versão antiga

Pesquisar antes de reutilizar:
- relação entre escassez financeira e desempenho cognitivo;
- carga alostática e pobreza;
- privação de sono e saúde;
- estresse crônico e funções executivas;
- efeitos da insegurança alimentar;
- mobilidade para dentro/fora da pobreza;
- efeitos intergeracionais de pobreza;
- epigenética humana: limites do que pode ser afirmado;
- dívida e saúde mental;
- habitação e estresse;
- volatilidade de renda;
- consumo compensatório: evidência e limites.

## 11. Evidência negativa também entra

Se uma hipótese querida pelo livro não encontrar suporte:
- registrar;
- não esconder;
- decidir se vira metáfora, hipótese ou é removida.

## 12. Reprodutibilidade

Guardar:
- planilhas;
- consultas;
- fórmulas;
- scripts;
- versão da metodologia;
- data dos dados.

O livro pode ter um apêndice metodológico ou repositório público associado.

## 13. Nenhum número validado ainda

Em 2026-10-17 este documento contém apenas arquitetura de pesquisa. O livro ainda não possui uma contabilidade populacional aprovada.
