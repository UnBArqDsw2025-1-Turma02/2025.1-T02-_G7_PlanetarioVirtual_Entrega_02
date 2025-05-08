# Diagrama de Casos de Uso

## Introdução

O Diagrama de Casos de Uso é um dos principais diagramas comportamentais da UML (Unified Modeling Language), utilizado para capturar e representar as funcionalidades de um sistema do ponto de vista do usuário <sup>[1](#ref1)</sup>. Ele permite identificar os atores (usuários ou sistemas externos) e os casos de uso (funções ou serviços oferecidos pelo sistema), evidenciando como os atores interagem com o sistema para atingir determinados objetivos <sup>[2](#ref2)</sup>.

Esse tipo de diagrama é particularmente útil nas fases iniciais do desenvolvimento de software, pois auxilia na elicitação e validação de requisitos funcionais de forma clara e acessível tanto para a equipe técnica quanto para os stakeholders não técnicos. Os elementos são representados graficamente por elipses (casos de uso), figuras estilizadas de pessoas (atores) e linhas que indicam interações. Também é possível utilizar relacionamentos como inclusão, extensão e generalização, para representar variações e dependências entre os casos de uso.

Além de servir como guia para o desenvolvimento e para a escrita de cenários de testes, o Diagrama de Casos de Uso também contribui para a comunicação entre os membros da equipe e para a compreensão global do sistema que está sendo construído. Sua simplicidade e foco nas interações tornam-no uma ferramenta eficaz para garantir que as funcionalidades previstas estejam alinhadas às necessidades dos usuários <sup>[4](#ref4)</sup>.

## Metodologia

Na UML, o Diagrama de Casos de Uso segue uma notação padronizada para representar visualmente as funcionalidades do sistema e as interações com os usuários ou sistemas externos. A seguir, detalhamos os principais elementos gráficos e suas representações neste tipo de diagrama.

## Representação dos Atores

Os atores representam usuários, sistemas ou entidades externas que interagem com o sistema modelado. São geralmente representados por figuras estilizadas de pessoas (bonecos palito) <sup>[2](#ref2)</sup>.

<font size="3"><p style="text-align: center"><b>Figura 1:</b> Atores</p></font>
<center>

![Atores](./assets/AtoresCasosDeUso.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>


## Representação dos Casos de Uso

Os casos de uso são as ações que os atores podem fazer no sistema. São representados por elipses contendo o nome da ação no centro <sup>[2](#ref2)</sup>.

<font size="3"><p style="text-align: center"><b>Figura 2:</b> Casos de uso</p></font>
<center>

![Casos de Uso](./assets/CasosDeUso.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>

## Conexões (Associações)

A relação entre um ator e um caso de uso é mostrada por uma linha reta simples, indicando que o ator pode executar aquela funcionalidade <sup>[2](#ref2)</sup>.

<font size="3"><p style="text-align: center"><b>Figura 3:</b> Associações</p></font>
<center>

![Associacoes](./assets/Associacoes.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>

## Relacionamentos Especiais

### Inclusão (<< include >>)

O relacionamento de inclusão é usado quando uma funcionalidade obrigatória de um caso de uso sempre envolve a execução de outro caso de uso. Ou seja, um caso de uso sempre inclui um comportamento comum, reutilizável, dentro de outro.

**O caso de uso "Alterar senha" sempre inclui a ação "Validar senha".**

<font size="3"><p style="text-align: center"><b>Figura 4:</b> Include</p></font>
<center>

![include](./assets/InlcudeCasoDeUso.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>

### Extensão (<< extend >>)

O relacionamento de extensão é usado quando um comportamento opcional pode ser adicionado a um caso de uso, dependendo de alguma condição. Ou seja, o caso de uso base pode ser estendido por outro caso de uso de forma condicional.

**Pgit ara o caso de uso "Visualizar Dados" ser executado, o usuário deve primeiro passar pelo caso de uso "Login".**

<font size="3"><p style="text-align: center"><b>Figura 5:</b> Extend</p></font>
<center>

![include](./assets/ExtendCasoDeUso.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>

## Organização Visual

- Um **diagrama** típico é composto por <sup>[2](#ref2)</sup>:
  1. Um **retângulo de sistema** (opcional) que delimita os **casos de uso internos**.
  2. **Atores** posicionados **fora do sistema**.
  3. **Casos de uso** dispostos **dentro do retângulo**, conectados por **linhas de associação e setas de relacionamento**.

## Diagrama de Casos de Uso

<font size="3"><p style="text-align: center"><b>Figura 6:</b> Diagrama de Casos de uso</p></font>
<center>

![Diagrama de casos de uso](./assets/DiagramaCasoUso.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [João Pedro](https://github.com/JoaoPedrooSS), [Rafael Pereira](https://github.com/rafgpereira), [Milena Rocha](https://github.com/milenafrocha), [Manoel Moura](https://github.com/manoelmoura) e [Raphaela Guimarães](https://github.com/raphaiela), 2025.</p></font>


## Referências Bibliográficas

>1. <a id="ref1"></a> FOWLER, Martin. **UML Essencial**. 3. ed. Rio de Janeiro: Alta Books, 2010.  
>
>2. <a id="ref2"></a> Bóson Treinamentos. **Curso de UML - O que são Diagramas de Casos de Uso**. YouTube, 2020. Disponível em: <https://www.youtube.com/watch?v=K-BaRfFx0mA>. Acesso em: 07 maio 2025. 
>
>3. <a id="ref3"></a>  LARMAN, Craig. **Utilizando UML e Padrões: Uma Introdução à Análise e ao Projeto Orientados a Objetos**. 3. ed. Porto Alegre: Bookman, 2007.
>
>4. <a id="ref4"></a>  SOMMERVILLE, Ian. **Engenharia de Software**. 10. ed. São Paulo: Pearson, 2019.
 


## Histórico de Versões

| Versão | Data       | Descrição                                      | Autor               | Revisor            |
|--------|------------|------------------------------------------------|---------------------|--------------------|
| 1.0    | 07/05/2025 | Criação do documento com divisões a serem preenchidas conforme o padrão | [João Pedro](https://github.com/JoaoPedrooSS) | [Rafael Pereira](https://github.com/rafgpereira) |
