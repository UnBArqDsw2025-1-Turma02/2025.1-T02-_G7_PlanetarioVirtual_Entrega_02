# Diagrama de Classes

## Introdução

O Diagrama de Classes é um dos principais artefatos da UML (Unified Modeling Language), uma linguagem de modelagem gráfica amplamente utilizada para representar sistemas de software <sup>1</sup>. Especificamente, ele faz parte dos diagramas estruturais da UML, que descrevem os elementos estáticos de um sistema orientado a objetos, como classes, atributos, métodos e os relacionamentos entre eles <sup>2</sup>.

Este diagrama descreve a estrutura estática do sistema, representando os tipos de objetos que podem existir e como eles se relacionam. As classes são representações de entidades do mundo real e atuam como tipos personalizados que encapsulam dados (atributos) e comportamentos (métodos) <sup>3</sup>. Visualmente, cada classe é representada como um retângulo dividido em três partes: nome da classe, atributos e métodos. As relações entre classes — como associação, herança, composição e dependência — são indicadas por linhas e setas com notações específicas <sup>4</sup>.

Além disso, os diagramas de classes servem como base para a implementação de sistemas em linguagens orientadas a objetos, e seu uso é essencial tanto na fase de análise quanto na de projeto. Em projetos grandes, as classes são organizadas em pacotes, facilitando a compreensão e manutenção do sistema <sup>5</sup>. Como ferramenta de modelagem, o Diagrama de Classes contribui diretamente para a comunicação entre os membros da equipe, para a documentação do projeto e para a construção de uma arquitetura de software sólida <sup>6</sup>.

## Metodologia

Na UML, o **Diagrama de Classes** utiliza uma notação padronizada para representar visualmente os elementos de um sistema orientado a objetos. A seguir, detalhamos os principais símbolos e representações utilizados neste tipo de diagrama.

### Representação de Atributos

Os atributos descrevem as **características** de uma classe, ou seja, os dados que seus objetos manterão. São representados com a seguinte notação:

```
visibilidade nome: tipo
```

#### Símbolos de visibilidade:

- `+` **(público)**: o atributo é acessível por qualquer classe.
- `-` **(privado)**: o atributo só é acessível dentro da própria classe.
- `#` **(protegido)**: o atributo é acessível na própria classe e nas suas subclasses.
- `~` **(pacote)**: o atributo é acessível somente dentro do mesmo pacote.

**Exemplo**:
```text
- nome: String
+ idade: int
```

Isso indica que o atributo `nome` é privado e do tipo `String`, e que o atributo `idade` é público e do tipo `int`.

---

### Representação de Métodos (Operações)

Os métodos (ou operações) definem os **comportamentos** de uma classe — ou seja, o que os objetos daquela classe podem fazer. A notação é semelhante à dos atributos:

```
visibilidade nome(parâmetros): tipo_de_retorno
```

**Exemplo**:
```text
+ calcularSalario(horas: int): float
```

Isso indica que o método é público, recebe um parâmetro `horas` do tipo `int` e retorna um `float`.

---

### Tipos de Relacionamentos e Setas

No diagrama, as **relações entre classes** são representadas por **linhas e setas** com significados específicos. Abaixo, explicamos cada tipo:

#### 1. Associação

- Representada por uma **linha simples** entre duas classes.
- Indica que uma classe **usa ou conhece** a outra.
- Pode incluir **multiplicidade** (ex: 1..*, 0..1) indicando quantos objetos estão envolvidos.

```
Pessoa -------- Endereço
```

#### 2. Agregação

- Representada por uma **linha com losango branco** na extremidade.
- Indica uma **relação todo-parte**, onde a parte pode existir **independentemente** do todo.

```
Turma ◇-------- Aluno
```

Turma *agrega* vários alunos, mas os alunos podem existir sem a turma.

#### 3. Composição

- Representada por uma **linha com losango preto**.
- Também é uma relação todo-parte, mas com **forte dependência** — a parte **não pode existir** sem o todo.

```
Casa ◆-------- Cômodo
```

Se a `Casa` for destruída, os `Cômodos` também deixam de existir.

#### 4. Generalização (Herança)

- Representada por uma **linha com seta aberta (triângulo) apontando para a superclasse**.
- Indica que uma classe herda atributos e métodos de outra.

```
Funcionario ◁─── Gerente
```

`Gerente` herda de `Funcionario`.

#### 5. Dependência

- Representada por uma **linha tracejada com seta**.
- Indica que uma classe depende temporariamente da outra (ex: usa como parâmetro de método).

```
Pedido - - - - -> Cliente
```

---

### Organização Visual

- Cada classe é representada por um **retângulo com três compartimentos**:
  1. **Nome da classe** (em negrito ou sublinhado, dependendo do tipo).
  2. **Atributos** listados com visibilidade, nome e tipo.
  3. **Métodos** listados com assinatura completa.

---

Essa padronização na representação é fundamental para garantir a clareza e a compreensão entre analistas, desenvolvedores e outros stakeholders ao longo do projeto de software <sup>7</sup>.




## Referências Bibliográficas

>1. <a name="1"></a> FOWLER, Martin. *UML Essencial*. 3. ed. Rio de Janeiro: Alta Books, 2010.  
>
>2. <a name="2"></a> Bóson Treinamentos. **Curso de UML - O que é um Diagrama de Classes**. YouTube, 2020. Disponível em: <https://www.youtube.com/watch?v=5jR3ZT9bz5M>. Acesso em: 1 maio 2025.  
>
>3. <a name="3"></a> GUEDES, Gilleanes. **Diagrama de Pacotes - UML**. YouTube, 2020. Disponível em: <https://www.youtube.com/watch?v=HZJ2DLFOwyo>. Acesso em: 1 maio 2025.  
>
>4. <a name="4"></a> OLIVEIRA, George. **Diagrama de Sequência**. YouTube, 2021. Disponível em: <https://www.youtube.com/watch?v=zgWY8LRJ-90>. Acesso em: 1 maio 2025.  
>
>5. <a name="5"></a> GUEDES, Gilleanes. **Engenharia de Software e UML**. Canal YouTube, várias datas.  
>
>6. <a name="6"></a> FOWLER, Martin. *UML Essencial*. Trechos adaptados do PDF: *UML-Essencial-Martin-Fowler.pdf*. 
>7. <a name="1"></a> FOWLER, Martin. *UML Essencial*. 3. ed. Rio de Janeiro: Alta Books, 2010.

## Histórico de Versões

| Versão | Data       | Descrição                                      | Autor               | Revisor            |
|--------|------------|------------------------------------------------|---------------------|--------------------|
| 1.0    | 30/04/2025 | Criação do documento com divisões a serem preenchidas conforme o padrão | [Milena Rocha](https://github.com/milenafrocha)          | [Rafael Pereira](https://github.com/rafgpereira)  |
| 1.1    | 01/05/2025 | Adição de introdução e metodologia bem como suas respectivas referências | [Milena Rocha](https://github.com/milenafrocha)          | [Rafael Pereira](https://github.com/rafgpereira)  |


