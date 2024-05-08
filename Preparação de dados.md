# Preparação de Dados

A preparação dos dados visa garantir que a informação contida nos conjuntos de dados seja adequadamente formatada e exposta para analise por ferramentas de analise de dados. Isso inclui lidar com incompletude, lixo e inconsistencias nos dados do mundo real. Além disso, a preparação dos dados tambem capacida os preparadores a selecionarem os modelos de analise de dados mais apropriados.

## Tarefas na preparação de dados

 - Discretização/Enumeração;
 - Limpeza;
 - Integração;
 - Transformação;
 - Redução.

### Discretização/Enumeração

Utiliza-se a discretização (ou enumeração) para reduzir o número de valores de um atributo continuo, dividindo-o em intervalos;
 - Os métodos mais utilizados (Naive Bayes, CHAID, etc.), requerem valores discretos;
 - Redução do tamanho dos dados;
 - Método utilizado para produzir sumariação dos dados;
 - (Sinónimo de *binning*).

### Limpeza

Ausencia de valores em determinados atributos devido a:
 - inconsistencia;
 - dados nao registados;
 - analise incorreta;
 - dados registados de forma errada;
 - etc.

A ausencia de dados pode revelar algo sobre que campos nao foram preenchidos!

Como abordar a limpeza de dados:
 * Ignorar os registos com dados em falta: Esta abordagem pode ser útil se a quantidade de dados em falta for baixa em comparação com o total de dados. No entanto, se houver uma quantidade significativa de dados em falta, essa abordagem pode resultar na perda de informações importantes.
 * Ignorar atributos com dados em falta: Se os atributos com dados em falta não são essenciais para a análise ou se não contêm informações críticas, essa abordagem pode ser aceitável. No entanto, se os atributos ausentes forem importantes, ignorá-los pode comprometer a análise.
 * Preencher manualmente os dados em falta: Esta abordagem é mais trabalhosa, mas pode ser necessária se os dados ausentes forem críticos e não puderem ser inferidos com precisão de outras maneiras.
 * Preencher os dados em falta com um mesmo valor ("talvez"): Essa abordagem pode introduzir viés nos dados e distorcer análises subsequentes. Pode criar tendências artificiais nos dados ou até mesmo gerar novas classes.
 * Preencher com o valor médio do atributo: Esta é uma abordagem comum e pode ser apropriada se o desvio padrão dos dados não for grande. No entanto, pode distorcer a distribuição dos dados se houver valores extremos.
 * Preencher com o valor mais frequente do atributo: Esta abordagem é simples e rápida, mas pode não ser apropriada se houver uma grande variedade de valores no atributo ou se os dados forem altamente variáveis.

É importate ter em mente que quanto mais valores "inventados" forem introduzidos durante o processo de limpeza de dados, maior será o desvio entre os dados processados e a realidade que eles reprsentam. Portanto, é crucial escolher as abordagens de limpeza de dados com cuidado, considerando a qualidade e a integridade dos dados.

### Integração

Na integração de dados, é essencial considerar que os dados podem ter varias origens e o objetivo é unifica-los em um conjunto coeso. Isso envolve detectar e resolver conflitos entre os dados, especialmente quando surgem inconsistencias. Para resolver esses conflitos, é importante confiar na fonte de dados mais confiavel. ALem disso, a integração de dados requer um profundo conhecimento do negocio para garantir que a coleção resultante de dados seja precisa e útil.

### Transformação

 - Alisamento (smoothing);
   - Remover lixo/ruido dos dados (binning, clustering, regressao);
 - Agregação;
   - Pressupoe que o resultado sumaria os dados iniciais;
 - Generalização;
   - Hierarquização de conceitos;
 - Construção de atributos;
   - Construção de novos atributos a partir de outros;
 - Uniformização;
   - Pretende evitar com uma gama alargada de valores sobressaiam em relação a outros com menor quantidade de valores;
 - Deteção de valores atipicos. 

### Redução

A redução de dados é uma estratégia essencial quando lidamos com grandes volumes de dados armazenados em um Data Warehouse, muitas vezes medidos em terabytes. Isso se deve ao fato de que a execução de tarefas de exploração e análise em conjuntos de dados tão grandes pode se tornar impraticável devido ao tempo e recursos necessários.

O objetivo da redução de dados é obter uma representação menor do volume original de dados, mantendo ao máximo os mesmos resultados analíticos. Isso pode ser feito de várias maneiras, como amostragem aleatória, agregação de dados ou seleção de características relevantes. O resultado final é um conjunto de dados menor que ainda preserva a maioria das informações necessárias para análise e tomada de decisões, mas que é mais gerenciável e fácil de processar.

**Estrategias**
Na construção de cubos de dados, as operações de agregação são aplicadas para criar uma representação multidimensional dos dados. A redução de dimensões envolve remover atributos irrelevantes, redundantes ou pouco interessantes para a análise, podendo ser realizada através de métodos como a Principle Component Analysis (PCA). A compressão de dados é realizada aplicando técnicas para reduzir a representação dos dados originais. A redução de quantidade de dados pode ser alcançada por meio de técnicas paramétricas ou não paramétricas. Por fim, a discretização e generalização de conceitos visam reduzir a quantidade de valores por atributo, simplificando a análise.