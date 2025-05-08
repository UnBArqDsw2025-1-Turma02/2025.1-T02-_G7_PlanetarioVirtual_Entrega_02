# Diagrama de Pacotes

## Introdução

O Diagrama de Pacotes é um dos principais artefatos usado para representar a organização modular de um sistema, evidenciando suas dependências e agrupamentos lógicos. Fornecendo uma visão geral da arquitetura, facilitando a compreensão da estrutura do software e contribuindo para a separação de responsabilidades.

Para o Planetário Virtual, parte da equipe elaborou e revisou o Diagrama de Pacotes como parte da documentação arquitetural, visando mapear os módulos que compõem o sistema tanto no backend quanto no frontend. A modelagem foi realizada coletivamente por todos os membros do grupo, garantindo uma visão compartilhada sobre as responsabilidades de cada componente e sobre as conexões entre as diferentes camadas da aplicação.

## Metodologia

Para a construção dos diagramas de pacotes, o grupo seguiu uma abordagem colaborativa, identificando os domínios funcionais, agrupamendo das classes e arquivos e definindo os relacionamentos entre pacotes.

Três diagramas criados:

- Um diagrama de alto nível da arquitetura geral.

- Um diagrama focado no backend.

- Um diagrama focado no frontend.

Durante o processo, a equipe utilizou ferramentas de modelagem UML para validar a estrutura e garantir a coerência com a implementação real do sistema. Todas as decisões foram discutidas em grupo, o que assegurou o alinhamento conceitual e técnico.

## Diagramas de Pacotes Criados

### Diagrama 1: Arquitetura em Alto Nível

A **figura 1** representa a visão geral do sistema, dividido em três pacotes principais:

<font size="3"><p style="text-align: center"><b>Figura 1:</b> Visão Geral do Sistema</p></font>

<center>

![Visão Geral do Sistema](./assets/visãogeralPacotes.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [Carlos Paz](https://github.com/dudupaz), [João Lucas](https://github.com/jlucasiqueira), [Letícia Martins](https://github.com/leticiatmartins), [Taynara Gabrielle](https://github.com/taybalau) e [Antônio José](https://github.com/antonioleaojr), 2025.</p></font>

- Visão Geral: Backend se comunica com Frontend

- Frontend: Responsável pela interface com o usuário e pela lógica de apresentação.

- Backend: Contém as regras de negócio e a lógica de processamento do sistema.

### Especificação Estendida – Diagrama 1: Arquitetura em Alto Nível

| Elemento                 | Descrição                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **Objetivo**             | Apresentar uma visão macro do sistema Planetário Virtual, destacando a separação entre frontend e backend e suas responsabilidades.        |
| **Escopo**               | Toda a aplicação do Planetário Virtual, incluindo suas principais camadas lógicas.                                                         |
| **Pacotes Representados**| `Frontend`, `Backend`, `Comunicação entre pacotes`                                                                                        |
| **Descrição Detalhada**  | O diagrama demonstra a arquitetura em três grandes divisões: o pacote `Frontend`, o pacote `Backend` e a relação entre eles. O Frontend é responsável por toda a interação com o usuário e exibição de dados, enquanto o Backend centraliza as regras de negócio e acesso a dados externos (como a API da NASA). A seta entre os pacotes indica dependência unidirecional do Frontend para o Backend. |
| **Justificativa Arquitetural** | Esta separação de responsabilidades segue o padrão MVC adaptado para aplicações web modernas, facilitando a manutenção, escalabilidade e testabilidade do sistema. |
| **Ferramenta Utilizada** | Lucidchart                                                                                                                                 |
| **Autores**              | Carlos Paz, João Lucas, Letícia Martins, Taynara Gabrielle e Antônio José                                                                 |


---

### Diagrama 2: Diagrama de Pacotes do Backend

A **figura 2** detalha a estrutura de Diagrama de Pacotes do Backend

<font size="3"><p style="text-align: center"><b>Figura 2:</b> Diagrama de Pacotes do Backend</p></font>

<center>

![Visão Geral do Sistema](./assets/backendPacotes.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [Carlos Paz](https://github.com/dudupaz), [João Lucas](https://github.com/jlucasiqueira), [Letícia Martins](https://github.com/leticiatmartins), [Taynara Gabrielle](https://github.com/taybalau) e [Antônio José](https://github.com/antonioleaojr), 2025.</p></font>

- Controllers usa Services

- Services usa Repositories

- Services usa Utils

- Models e Repositories tem um relacionamento bidirecional

- Models é usado por Services

- Repositories acessa a API da NASA

### Especificação Estendida – Diagrama 2: Pacotes do Backend

| Elemento                 | Descrição                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **Objetivo**             | Detalhar a arquitetura interna da camada de backend do Planetário Virtual, destacando as dependências entre seus módulos.                 |
| **Escopo**               | Camada de backend do sistema.                                                                                                              |
| **Pacotes Representados**| `Controllers`, `Services`, `Repositories`, `Models`, `Utils`                                                                              |
| **Descrição Detalhada**  | O diagrama evidencia as seguintes relações entre pacotes:<br>• `Controllers` dependem de `Services`.<br>• `Services` utilizam tanto `Repositories` quanto `Utils` para aplicar a lógica de negócio.<br>• `Repositories` acessam diretamente a API da NASA.<br>• `Models` possuem relação bidirecional com `Repositories` e são também utilizados por `Services`. |
| **Justificativa Arquitetural** | O design segue princípios de separação de responsabilidades e desacoplamento entre as camadas. Permite alta coesão dentro dos pacotes e baixo acoplamento entre eles, aderindo aos princípios da Clean Architecture. |
| **Ferramenta Utilizada** | Lucidchart                                                                                                                                 |
| **Autores**              | Carlos Paz, João Lucas, Letícia Martins, Taynara Gabrielle e Antônio José                                                                 |


---

### Diagrama 3: Diagrama de Pacotes do Frontend

A **Figura 3** detalha a estrutura de Diagrama de Pacotes do Frontend

<font size="3"><p style="text-align: center"><b>Figura 3:</b> Diagrama de Pacotes do Frontend</p></font>

<center>

![Visão Geral do Sistema](./assets/frontendPacotes.png)

</center>

<font size="3"><p style="text-align: center"><b>Autores</b>: [Carlos Paz](https://github.com/dudupaz), [João Lucas](https://github.com/jlucasiqueira), [Letícia Martins](https://github.com/leticiatmartins), [Taynara Gabrielle](https://github.com/taybalau) e [Antônio José](https://github.com/antonioleaojr), 2025.</p></font>

- Pages usa Components

- Pages usa Services

- Pages usa Assets

- Components usa Styles

- Components usa Assets

### Especificação Estendida – Diagrama 3: Pacotes do Frontend

| Elemento                 | Descrição                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **Objetivo**             | Representar a organização modular da camada de frontend, demonstrando as dependências entre seus principais componentes.                  |
| **Escopo**               | Interface do usuário (camada de frontend) da aplicação Planetário Virtual.                                                                |
| **Pacotes Representados**| `Pages`, `Components`, `Services`, `Assets`, `Styles`                                                                                     |
| **Descrição Detalhada**  | As relações entre os pacotes estão organizadas da seguinte forma:<br>• `Pages` importa `Components`, `Services` e `Assets`.<br>• `Components` usa `Styles` para estilização e `Assets` para recursos visuais.<br>• `Services` fornece acesso a dados e lógica de integração para `Pages`. |
| **Justificativa Arquitetural** | A separação dos pacotes melhora a reutilização de componentes e a organização do código. O uso de `Pages` como entrada principal da aplicação reflete práticas comuns em frameworks modernos como React e Next.js. |
| **Ferramenta Utilizada** | Lucidchart                                                                                                                                 |
| **Autores**              | Carlos Paz, João Lucas, Letícia Martins, Taynara Gabrielle e Antônio José                                                                 |

## Referências Bibliográficas

>1. <a id="ref1"></a> GitMind. **Diagrama de pacotes**. Disponível em: https://gitmind.com/pt/diagrama-de-pacotes. Acesso em: 8 mai. 2025.
>
>2. <a id="ref2"></a> Visual Paradigm. **What is Package Diagram?** Disponível em: https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-package-diagram/. Acesso em: 8 mai. 2025.
>

