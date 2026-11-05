1. Objetivo --- O que o sistema fará?
O ALL IN ORDER será uma aplicação web de gestão financeira e
acompanhamento de obras, concebida para centralizar a informação
relativa aos projetos de construção civil e simplificar o controlo dos
respetivos orçamentos e despesas.

O sistema permitirá aos utilizadores criar e gerir obras, definir um
orçamento inicial, registar despesas associadas a cada obra e acompanhar
a evolução dos custos. Com base nos dados introduzidos, a aplicação
calculará automaticamente os custos acumulados e o saldo disponível,
apresentando a informação de forma organizada num painel de controlo.

O objetivo principal é reduzir a dispersão da informação, facilitar o
acompanhamento financeiro e apoiar decisões durante a execução das
obras.
2. Escopo --- Onde poderá ser usado?
O sistema destina-se principalmente a organizações e profissionais
ligados à construção civil, nomeadamente:
- Pequenas e médias empresas de construção civil.
- Empresas de remodelação e reabilitação de edifícios.
- Empreiteiros e subempreiteiros.
- Engenheiros civis e gestores de obra.
- Profissionais independentes que necessitem de controlar os custos
  dos seus projetos.
A aplicação poderá ser utilizada em contexto de escritório ou no local
da obra, desde que exista um dispositivo com navegador web e ligação à
Internet.

O âmbito inicial do projeto será o controlo financeiro de obras. Não
está previsto, nesta fase, substituir sistemas completos de
contabilidade, gestão de recursos humanos, compras, planeamento técnico
ou gestão de stocks.
3. Partes interessadas (Stakeholders)
  Parte interessada                  Relação com o sistema / benefício
  Proprietários e gestores de         Acompanham os orçamentos, custos e
empresas de construção              situação financeira das obras.

  Gestores de obra                    Consultam a informação financeira e
registam ou acompanham despesas dos
projetos sob a sua
responsabilidade.

  Engenheiros civis                   Consultam os custos associados às
obras e apoiam o acompanhamento dos
projetos.

  Empreiteiros e profissionais        Organizam os orçamentos e controlam
independentes                       as despesas de cada obra.

  Funcionários autorizados            Introduzem e consultam informação,
de acordo com as permissões
atribuídas.

  Equipa de desenvolvimento           Analisa requisitos, implementa,
testa e mantém a solução.
Docente da unidade curricular       Acompanha e avalia o
desenvolvimento do projeto
académico.
4. Equipa do projeto --- Time de Desenvolvimento
A equipa responsável pela análise, conceção, desenvolvimento e testes da
aplicação é constituída por:
- Renato Santos
- Henner Santos
- Analiel Ricardo
- Willbon
As responsabilidades específicas de cada elemento poderão ser
distribuídas pela equipa ao longo do projeto. A equipa, no seu conjunto,
será responsável por gerir os requisitos, definir a arquitetura,
implementar as funcionalidades, testar a aplicação e documentar o
trabalho desenvolvido.
5. Características do sistema --- Lista de funcionalidades
As funcionalidades previstas para a primeira versão web são:
5.1. Autenticação e acesso
- Iniciar e terminar sessão.
- Restringir o acesso às funcionalidades a utilizadores autenticados.
- Associar os registos ao utilizador ou à organização a que pertencem.
5.2. Gestão de obras
- Criar uma obra.
- Consultar a lista de obras.
- Visualizar os detalhes de uma obra.
- Editar os dados de uma obra.
- Eliminar uma obra, mediante confirmação.
- Registar informação como nome, morada e orçamento inicial.
5.3. Gestão de despesas
- Adicionar despesas a uma obra.
- Registar, pelo menos, uma descrição, categoria, valor e data.
- Consultar as despesas associadas a cada obra.
- Editar ou eliminar despesas, respeitando as permissões definidas.
5.4. Controlo financeiro
- Calcular automaticamente o total de despesas de cada obra.
- Calcular o saldo disponível através da diferença entre o orçamento
  inicial e as despesas registadas.
- Apresentar indicadores que permitam comparar o orçamento com os
  custos acumulados.
- Sinalizar situações em que as despesas ultrapassem o orçamento
  definido.
5.5. Dashboard e relatórios
- Apresentar uma visão geral das obras e dos respetivos indicadores
  financeiros.
- Consultar os principais valores de cada obra.
- Gerar e exportar relatórios em PDF.
As funcionalidades e regras de negócio serão detalhadas e validadas
durante a análise de requisitos.
6. Arquitetura de referência
A arquitetura de referência proposta segue uma organização em camadas,
separando a interface web, a lógica de negócio e a persistência de
dados.
Descrição dos componentes
- Navegador e interface web: permitem ao utilizador interagir com
  o sistema, consultar obras e introduzir dados.
- API / Backend: recebe os pedidos da interface, valida os dados e
  coordena a execução das operações.
- Autenticação e autorização: controla a identidade dos
  utilizadores e o acesso às funcionalidades e aos dados.
- Serviço de gestão de obras: trata da criação, consulta,
  alteração e remoção de obras.
- Serviço de gestão de despesas: gere os registos de despesas
  associados a cada obra.
- Serviço de cálculo financeiro: calcula os custos acumulados e o
  saldo disponível.
- Serviço de relatórios PDF: prepara os dados e gera relatórios
  para consulta ou exportação.
- Base de dados: armazena os utilizadores, as obras, as despesas e
  os restantes dados necessários à aplicação.
A tecnologia concreta de frontend, backend e base de dados será
escolhida e documentada pela equipa durante a fase de desenho técnico. O
diagrama representa uma arquitetura lógica de referência, não uma
decisão definitiva sobre tecnologias ou infraestrutura.
7. Restrições do produto
O funcionamento do sistema estará sujeito às seguintes restrições:
- Ligação à Internet: por ser uma aplicação web, a utilização
  normal dependerá de uma ligação à rede e da disponibilidade do
  servidor.
- Disponibilidade do servidor: falhas ou períodos de manutenção do
  servidor poderão impedir temporariamente o acesso.
- Compatibilidade do navegador: a aplicação deverá ser utilizada
  num navegador moderno e atualizado; navegadores antigos poderão não
  suportar todas as funcionalidades.
- Acesso e permissões: os utilizadores só deverão conseguir
  consultar ou alterar dados para os quais tenham autorização.
- Qualidade dos dados: os cálculos financeiros dependem da
  introdução correta dos orçamentos e das despesas. O sistema não
  consegue garantir a veracidade dos valores introduzidos.
- Âmbito funcional: a versão inicial não substitui software de
  contabilidade certificada nem sistemas especializados de planeamento
  e gestão integral de construção.
- Integrações externas: funcionalidades que dependam de serviços
  externos, como envio de e-mails ou armazenamento externo, dependerão
  da disponibilidade e configuração desses serviços.
- Segurança e proteção de dados: a aplicação deverá proteger
  credenciais e informação financeira, aplicar controlo de acessos e
  evitar a exposição de dados entre utilizadores ou organizações.
8. Integração de LLM (opcional)
Como possibilidade de evolução, o ALL IN ORDER poderá integrar um modelo
de linguagem de grande dimensão (LLM) para disponibilizar um assistente
que ajude os utilizadores a interpretar a informação financeira das
obras.

Exemplos de utilização:
- Responder a perguntas em linguagem natural sobre os dados de uma
  obra, como: "Quanto já foi gasto nesta obra?".
- Produzir resumos dos custos registados num determinado período.
- Identificar e explicar possíveis desvios entre o orçamento inicial e
  as despesas acumuladas.
- Ajudar a gerar uma descrição textual para acompanhar um relatório
  financeiro.
A integração deverá respeitar algumas condições:
- O LLM apenas poderá aceder aos dados a que o utilizador autenticado
  tem permissão.
- Os valores financeiros apresentados deverão ser obtidos a partir dos
  dados e cálculos do sistema, não inventados pelo modelo.
- O LLM deverá funcionar como ferramenta de apoio, não como substituto
  dos cálculos, regras de negócio ou decisões do utilizador.
- A eventual utilização de um serviço externo deverá considerar a
  privacidade dos dados, os custos e a disponibilidade da API.
A integração de LLM é opcional e não constitui um requisito obrigatório
para a primeira versão do sistema.
