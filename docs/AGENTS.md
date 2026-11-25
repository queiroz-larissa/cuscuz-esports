# AGENTS.md — Cuscuz Esports

## 1. Contexto do projeto

O Cuscuz Esports é um Projeto Individual acadêmico do curso de Análise e Desenvolvimento de Sistemas da SPTech, voltado à apresentação da comunidade competitiva de PUBG Mobile e ao gerenciamento e à consulta dos resultados de seus campeonatos internos.

A aplicação será composta por:

- Site institucional para apresentação da comunidade, sua história e identidade.
- Dashboard público para consulta de classificações, rankings, pontuações e indicadores coletivos de desempenho.
- Páginas de cadastro e login.
- Área administrativa restrita aos responsáveis pelo gerenciamento dos campeonatos e registro dos resultados.

O dashboard deverá ser acessível sem necessidade de cadastro ou login. A autenticação será necessária para acessar as funcionalidades administrativas, mediante autorização.

Os dados individuais dos jogadores serão armazenados no banco de dados para compor as estatísticas coletivas das equipes. Não haverá páginas de estatísticas individuais ou perfis estatísticos dos jogadores.

## 2. Tecnologias

Utilizar as tecnologias estabelecidas para o projeto:

| Tecnologia | Finalidade |
|---|---|

| HTML5 | Estruturação das páginas |
| CSS3 | Estilização e responsividade |
| JavaScript | Interatividade e lógica do front-end |
| Node.js | Desenvolvimento do back-end |
| Web-Data-Viz | Estrutura base da API disponibilizada pela SPTech |
| MySQL | Banco de dados relacional |
| Linux | Ambiente da máquina virtual destinada ao banco de dados |
| Chart.js | Construção dos gráficos do dashboard |
| Git | Controle de versionamento |
| GitHub | Hospedagem do repositório remoto |
| Git Bash | Terminal para execução dos comandos Git |

Não adicionar frameworks, bibliotecas ou tecnologias sem autorização prévia.

## 3. Comandos

### Instalação das dependências

```bash
npm i
```

Instala as dependências definidas no arquivo `package.json`.

### Inicialização da aplicação

```bash
npm start
```

Inicia a aplicação conforme as configurações existentes no projeto.

Os comandos devem ser executados no diretório que contém o arquivo `package.json`.

## 4. Arquitetura

A aplicação deverá respeitar a estrutura de desenvolvimento do Web-Data-Viz e a organização de arquivos já estabelecida no projeto.

### Estrutura de referência

```text
public/
├── assets/
│   └── imgs/
├── css/
├── dashboards/
├── html/
└── index.html

src/
├── routes/
├── controllers/
├── models/
└── database/
```

### Organização dos arquivos

| Arquivo ou diretório | Responsabilidade |
|---|---|

| `public/` | Arquivos do front-end |
| `index.html` | Página inicial da aplicação |
| `public/assets/imgs/` | Imagens, logos e recursos visuais |
| `public/css/` | Arquivos de estilização |
| `estilo.css` | Estilização conforme a organização existente |
| `public/dashboards/` | Páginas e recursos relacionados ao dashboard |
| `public/html/` | Demais páginas HTML |
| `src/` | Código do back-end |
| `src/routes/` | Definição das rotas da API |
| `src/controllers/` | Tratamento das requisições e respostas |
| `src/models/` | Consultas e operações no banco de dados |
| `src/database/` | Configuração e conexão com o banco de dados |

A estrutura apresentada é uma referência. A organização real do repositório deverá ser verificada antes da criação ou alteração de arquivos.

### Fluxo de comunicação

A comunicação entre o front-end e o banco de dados deverá seguir o padrão:

```text
Front-end
    ↓
Routes
    ↓
Controllers
    ↓
Models
    ↓
Database
    ↓
MySQL
```

O retorno das informações deverá seguir o caminho inverso, sendo disponibilizado ao front-end por meio da resposta da API.

Não realizar conexões diretas entre o front-end e o banco de dados.

## 5. Padrões de desenvolvimento

### JavaScript

- Utilizar `let` por padrão para variáveis que possam sofrer reatribuição.
- Utilizar `const` quando não houver necessidade de reatribuição.
- Não utilizar `var`.
- Utilizar nomes de variáveis claros, descritivos e preferencialmente em português.
- Nomear funções utilizando verbos que representem suas responsabilidades.
- Manter os padrões de nomenclatura existentes no projeto.

Exemplos de variáveis:

```javascript
let totalAbates = 0;
let quantidadePartidas = 0;
let pontuacaoTotal = 0;
```

Exemplos de funções:

```javascript
calcularPontuacao()
cadastrarCampeonato()
listarResultados()
validarCadastro()
atualizarRanking()
```

### Inputs

Utilizar o prefixo `ipt_` e a convenção snake_case nos identificadores dos campos de entrada.

Exemplos:

```html
<input id="ipt_nome">
<input id="ipt_email">
<input id="ipt_senha">
<input id="ipt_nome_campeonato">
<input id="ipt_total_abates">
```

### Boas práticas

- Utilizar estruturas simples, legíveis e compatíveis com os conteúdos trabalhados na SPTech.
- Evitar soluções desnecessariamente complexas.
- Manter a separação de responsabilidades entre os arquivos.
- Reaproveitar funcionalidades existentes sempre que possível.
- Evitar duplicação de código.
- Adicionar comentários explicativos nos trechos criados ou modificados, esclarecendo a finalidade das alterações.
- Preservar os comentários existentes que sejam relevantes para a compreensão do código.

## 6. Identidade visual

A interface deverá respeitar a identidade visual oficial do Cuscuz Esports, inspirada no cenário competitivo de PUBG Mobile e na jersey da equipe.

O design deverá transmitir competitividade, profissionalismo, modernidade e identidade esportiva.

### Paleta de cores

| Cor | Código HEX | Aplicação |
|---|---|---|

| Laranja Cuscuz | `#FF7B01` | Cor principal, botões, destaques e elementos da marca |
| Preto | `#000000` | Fundos e elementos de contraste |
| Branco | `#FFFFFF` | Textos, títulos e elementos de contraste |
| Grafite | `#17191D` | Fundos secundários |
| Cinza escuro | `#292E35` | Cards, menus, tabelas e painéis |
| Cinza claro | `#B3B3B3` | Textos secundários e informações complementares |

As cores oficiais da marca são laranja, preto e branco. As demais cores são complementares e deverão ser utilizadas para estabelecer hierarquia visual, contraste e legibilidade.

Cores semânticas, como verde para sucesso e vermelho para erros, poderão ser utilizadas pontualmente em mensagens, alertas e indicadores.

### Tipografia

| Tipografia | Aplicação |
|---|---|

| Horta | Títulos e elementos de identidade visual |
| New Sun Playful | Elementos gráficos e títulos especiais |
| Montserrat | Subtítulos e elementos de navegação |
| Glacial Indifferent | Textos gerais |
| Poppins | Textos, formulários e componentes do dashboard |

Utilizar as fontes disponíveis no projeto, respeitando a hierarquia tipográfica existente.

### Diretrizes visuais

- Preservar a identidade visual e os elementos gráficos oficiais do Cuscuz Esports.
- Utilizar a jersey da equipe como referência para estampas, degradês e detalhes gráficos.
- Priorizar interfaces modernas, organizadas e responsivas.
- Manter consistência entre o site institucional, os formulários e o dashboard.
- Utilizar o laranja como cor de destaque, evitando seu uso excessivo.
- Garantir contraste e legibilidade dos textos.
- Manter a padronização visual dos botões, cards, tabelas, gráficos e menus.
- Não modificar logos, estampas ou elementos oficiais da marca sem autorização.
- Não substituir o layout ou a identidade visual existente sem solicitação.

## 7. Regras de negócio

### Campeonatos e classificação

Os resultados deverão ser calculados com base nos dados registrados no banco de dados e nos critérios de pontuação estabelecidos para cada campeonato.

- **PA — Pontos por Abate:** pontuação obtida pelos abates realizados.
- **PP — Pontos por Posição:** pontuação obtida pela colocação da equipe na queda.
- **PT — Pontuação Total:** soma dos Pontos por Abate e Pontos por Posição.

```text
PT = PA + PP
```

A classificação deverá ser organizada em ordem decrescente de Pontuação Total, respeitando os critérios de desempate definidos para a competição.

Não estabelecer critérios de pontuação ou desempate sem consultar as regras do campeonato.

### Estatísticas coletivas

O dashboard deverá apresentar informações relacionadas ao desempenho coletivo das equipes, incluindo, conforme o escopo definido:

- Classificação dos campeonatos;
- Pontuação por abates;
- Pontuação por posição;
- Pontuação total;
- Quantidade de abates;
- Média de abates por partida;
- Quantidade de partidas disputadas;
- Quantidade de campeonatos disputados;
- Quantidade de WWCDs;
- Melhor desempenho;
- Conquistas e colocações.

### Registro e consolidação dos dados

- Registrar os abates individualmente por jogador no banco de dados.
- Utilizar operações de agregação, como `SUM()`, para calcular o total de abates da equipe.
- Calcular as médias coletivas considerando a quantidade de partidas disputadas pela equipe.
- Evitar a duplicação de registros durante os cálculos e consultas.
- Contabilizar o WWCD (Winner Winner Chicken Dinner) uma única vez para a equipe vencedora de cada queda.
- Associar as conquistas e colocações finais às equipes correspondentes.
- Utilizar os dados individuais dos jogadores como origem para a consolidação dos indicadores coletivos.

Não implementar páginas de estatísticas individuais, rankings individuais ou contabilização individual de WWCDs.

### Controle de acesso

O dashboard e as informações institucionais deverão permanecer públicos.

As funcionalidades de gerenciamento, inserção e alteração de resultados deverão ser restritas aos usuários autenticados e autorizados.

As permissões deverão ser verificadas no back-end, não apenas na interface.

## 8. Versionamento e commits

### Branches

Todas as alterações realizadas pelo agente deverão ser feitas na branch:

```text
revisao
```

Antes de iniciar uma alteração, verificar a branch atual e a situação dos arquivos do repositório.

- Não realizar commits diretamente na branch `main`.
- Não realizar merge com a `main` sem autorização.
- Não sobrescrever alterações existentes realizadas pela desenvolvedora.
- Não realizar operações destrutivas no repositório.
- Não enviar alterações ao repositório remoto sem autorização.

### Padrão de commits

Utilizar o padrão Conventional Commits:

```text
tipo(escopo): descrição
```

| Tipo | Finalidade |
|---|---|

| `feat` | Nova funcionalidade |
| `fix` | Correção de erro |
| `docs` | Alteração na documentação |
| `style` | Formatação de código sem alteração de comportamento |
| `perf` | Melhoria de desempenho |
| `refactor` | Refatoração de código |
| `test` | Criação ou alteração de testes |
| `chore` | Manutenção e configurações |

### Descrição dos commits

As descrições deverão ser curtas, objetivas, específicas e escritas em português, utilizando verbos no presente.

Evitar:

```text
feat(login): fiz o login
fix(cadastro): arrumei um erro
docs(readme): mudanças
style(tela): deixei mais bonito
```

Preferir:

```text
feat(login): adiciona validação de e-mail
fix(cadastro): corrige validação de senha
docs(readme): adiciona instruções de execução
feat(dashboard): adiciona gráfico de pontuação
fix(ranking): corrige cálculo da pontuação total
fix(dashboard): corrige espaçamento dos cards
refactor(model): simplifica consulta de resultados
style(css): padroniza indentação do código
```

Cada commit deverá representar uma alteração coerente e identificável.

## 9. Cuidados e restrições

O agente deverá respeitar o escopo acadêmico, a arquitetura e os padrões de desenvolvimento estabelecidos pela desenvolvedora.

É proibido:

- Alterar a arquitetura do projeto sem autorização.
- Substituir a estrutura base do Web-Data-Viz.
- Modificar funcionalidades existentes que não estejam relacionadas à solicitação.
- Reescrever arquivos inteiros quando uma alteração pontual for suficiente.
- Criar funcionalidades que não estejam previstas no escopo do projeto.
- Inventar jogadores, equipes, campeonatos, resultados ou regras de negócio.
- Alterar tabelas, atributos ou relacionamentos do banco de dados sem autorização.
- Criar arquivos, rotas, funções ou consultas duplicadas.
- Expor senhas, credenciais ou informações sensíveis.
- Utilizar tecnologias ou técnicas incompatíveis com os conhecimentos trabalhados no curso sem autorização.
- Remover arquivos ou funcionalidades existentes sem autorização.
- Exigir autenticação para acessar o dashboard público.

Caso seja necessário realizar alguma alteração fora do escopo solicitado, apresentar a justificativa e aguardar autorização antes de implementá-la.

## 10. Procedimento para implementação

Antes de implementar uma alteração:

1. Ler e respeitar as orientações deste documento.
2. Analisar os arquivos existentes relacionados à solicitação.
3. Verificar a branch atual e as alterações pendentes.
4. Identificar as dependências e possíveis impactos da implementação.
5. Verificar as tabelas e relacionamentos existentes, quando houver envolvimento do banco de dados.
6. Identificar a solução mais simples e compatível com o projeto.

Durante a implementação:

1. Trabalhar na branch `revisao`.
2. Alterar somente os arquivos necessários.
3. Respeitar os padrões de desenvolvimento e a identidade visual.
4. Comentar os trechos criados ou modificados.
5. Preservar as funcionalidades existentes.

Após a implementação:

1. Verificar o funcionamento da alteração.
2. Conferir possíveis erros e impactos em outras funcionalidades.
3. Informar quais arquivos foram criados ou modificados.
4. Explicar brevemente as alterações realizadas e suas finalidades.
5. Informar os testes realizados e eventuais limitações.
6. Registrar as alterações seguindo o padrão de commits estabelecido.

## 11. Regra geral

Antes de implementar qualquer alteração, seguir as tecnologias, arquitetura, identidade visual, convenções, regras de negócio e restrições descritas neste documento.

Caso alguma informação esteja ausente, analisar o código existente e seguir os padrões já adotados no projeto.

Em caso de dúvidas relacionadas ao escopo, às regras de negócio ou a alterações estruturais, consultar a desenvolvedora antes de prosseguir.

Priorizar soluções simples, funcionais, compreensíveis e compatíveis com o caráter acadêmico do projeto, permitindo que a desenvolvedora compreenda, explique e mantenha o código produzido.