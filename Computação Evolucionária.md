# Computação Evolucionária

## Bibliografia básica

* Goldberg, D. E., Genetic Algorithms in Search, Optimization, and Machine Learning. Addison-Wesley, 1989
* Ricardo Linden, Algoritmos Genéticos

## Computação Evolutiva

Classe de algoritmos de busca estocásticos baseados em população inspirados na Teoria Neo-Darwiniana.

### O que é evolução?

Melhoria sucessiva através de numerosas interações. Ocorre em um horizonte de tempo maior que o horizonte do aprendizado.
* Variabilidade genética
* Influência do meio
* Seleção natural

### O que é adaptabilidade?

Modificação reativa a um fator externo. Ocorre a curto prazo. Fundamental pra sedimentação das características boas.

### Onde CE se aplica?

Em problemas complexos que não possuem soluções escaláveis.


## Um pouco de biologia

### Teoria da Evolução
Observações de Darwin em 1850
* Animais da mesma espécie eram ligeiramente diferentes de seus parentes em ecossistemas diferentes
* Cada grupo era mais adaptado às necessidades e oportunidades oferecidas pelo seu ecossistema específico
* Filhos eram um pouco diferentes dos pais, logo existia algo causando variabilidade genética
* Indivíduos competiam por recursos. Os mais adaptados tinham mais chances de conseguir esses recursos. Os menos adaptados não conseguem e tem uma prole menor.

No século XX, Mendel compreende melhor o processo de transmissão de informação genética. A unidade básica de informação foi denominada **gene**. Com essa definição, surge o Neo-Darwinismo.

### Fundamentos Biológicos
Todo indivíduo é formado por uma ou mais células. Dentro de cada célula, existem *n* cromossomos (23 para humanos). Cada cromossomo consiste em sequências de DNA, que codificam a informação. Existem porções do cromossomo que não são genes.
**Dogma Central**: O DNA se replica e pode ser transcrito para o RNA, que é traduzido para proteínas. 

#### Composição dos cromossomos
Genes (sequências de DNA): tem uma posição (**locus**) e uma forma (**alelo**)

### Tradução
**introns** são as partes latentes sem informação, e os **exons** são as regiões codificantes. *splicing* é o processo de identificar essas regiões.

### Termos
**Genoma**: Conjunto completo de material genético
**Genótipo**: Um conjunto específico de genes do genoma
**Fenótipo**: Expressão das carasterísticas físicas e mentais codificadas pelos genes e modificadas pelo ambiente
**Fitness** ou **adaptabilidade**: Qualidade do indivíduo, medida pelo seu sucesso (sobrevivência)

### Reprodução
* Assexuada: um único indivíduo
* Sexuada: mais indivíduos, base para algoritmos genéticos. 

##### Cross-Over
Processo responsável pela reprodução sexuada, que faz a troca de material genético. Um cromossomo se cruza com o outro fisicamente.

### Mutação
Acontece por pequenos erros da enzima DNA polimerase, que geram mutações no código genético. Podem ser boas, ruins ou neutras. Também pode ser causada por fatores externos.

### Mecanismos
Mutação - Variação 
Fluxo gênico - Troca de informação
Deriva gênica - Variância natural, já que populações são finitas
Seleção - Critério de otimização