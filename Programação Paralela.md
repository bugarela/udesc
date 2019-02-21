# Programação Paralela

### Bibliografia Básica
* **SematicsScholar** - FOSTER, Ian. Designing and Building Parallel Programs: Concepts and Tools for Parallel Software Engineering. 1995.
* Livrinhos dos anais da escola regional de alto desempenho

### Em resumo: Desempenho

---

#### Sistemas Distribuídos
Mais geral e universal que a computação paralela (grande área)

#### Sistemas Paralelos
Forma restrita de computação distribuída, dedicada a solução de um único problema

#### Sistemas Concorrentes
Ações que podem ser executadas simultaneamente. Dois ou mais programas sequenciais que podem ser executados como processos paralelos.

### Todos requerem múltiplos processadores

---

**Estratégias**: formas de particionar o algoritmo para possivelmente atingir desempenho

### Memória compartilhada
```cpp
int *p = malloc(100);
f(p);
```
Tanto `malloc` quanto `f` podem estar sendo executadas por processadores distintos. Nesse contexto, é permitido o accesso da memória por múltiplos processamentos.
Ligada ao uso de ponteiros

### Troca de mensagens
Toda informação é solicitada/dada.

### Heterogenidade
Diferenças entre latência, largura de banda, protocolos e recursos computacionais.

### Migração de processos/tarefas
Iniciar o processo em uma máquina e continuar em outra. Gerenciamento de migração é uma outra área de estudo.

---

#### Propriedades de sistemas distribuídos que interessam sistemas paralelos
A **confiabilidade** não é importante, não se perde tempo fazendo verificações, devido ao foco em **desempenho**. Procura-se saber onde cada processo está, abdicando a **transparência** e a **flexibilidade**. **Escalabilidade** é outro fator de foco, juntamente com o novo fator de **economia de energia**.

### Objetivos: Minimizar e Balancear
Minimizar o tempo total da aplicação ou maximizar o *throughput* do sistema ou minimizar recursos necessários ou maximizar a utilização dos recursos.

Balancear é tentar atingir múltiplos objetivos (se estiver sobrecarregado, distribui mais, etc)

---

## Classificação de arquiteturas paralelas

### Classificação de Flynn
Autalizada: trocar *instruction* para *process*

|                      | Single Data | Multiple Data |
| --------             | --------    | --------      |
| Single Instruction   | SISD        | SIMD          |
| Multiple Instruction | MISD        | MIMD          |

**SISD**: Arquitetura von Neumann, pode existir pipeline (pseudoparalelismo). Como em python, podem existir threads, mas elas apenas controlam em paralelo coisas como I/O e CPU.

**MISD**: Múltiplos fluxos de instruções atuando sobre um único fluxo de dados. Não é tecnicamente viável, exceto por algumas operações de um jeito bizarro. Não é implementável.

**SMID**: Uma única instrução é executada ao mesmo tempo sobre múltiplos dados. Máquinas arrays, múltiplos programas executados sobre diferentes dados. Existe na GPU.
```cpp
int a = 10;
int x[10];
x += a;
```

**MIMD**: Cada unidade de controle recebe um fluxo de instrução. Nuvem, muticore, etc.

### Classificação segundo o compartilhamento de memória
