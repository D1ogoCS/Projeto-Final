# Projeto Final
## Implementação de mecanismos de autenticação e segurança em aplicações críticas: Caso de estudo - Sistema de gestão bancária

No meu projeto final de curso, realizei um caso de estudo/protótipo de um sistema de gestão bancária, com o objetivo de criar uma base de dados, uma aplicação de gestão e uma aplicação Web.

Nota final: 19 valores.

*__Nota:__ Este não é o projeto completo. Como o projeto é extenso, aqui estão apenas descritos os objetivos, os temas abordados, as funcionalidades, as ferramentas utilizadas, as tecnologias utilizadas e os resultados práticos obtidos. Os resultados apresentados são o reflexo do meu trabalho no desenvolvimento deste projeto. O código e os algoritmos não estão disponíveis para visualização, porque estou apenas a exibir o essencial.*

### Objetivos do projeto:

- Análise, avaliação e integração de mecanismos de proteção e segurança (blockchain, criptografia, etc...)
- Desenvolver dois protótipos funcionais que implementem e integrem vários mecanismos de segurança

### Temas abordados:

- Criptografia e Encriptação
- Tecnologia blockchain
- Chave Móvel Digital como método de autenticação
- Segurança em aplicações criticas
- Modelação do sistema - Casos de uso
- Diagrama de classes
- Modelo de dados
- Desenvolver e integrar serviços Web (SOAP)
- Desenvolver uma aplicação de gestão e uma aplicação Web

### Algumas implementações feitas no projeto:

- Relatórios em tempo real através do Report Viewer
- Códigos QR em relatórios
- Manipulação de ficheiros (documentos) através da aplicação de gestão
- Autenticação de dois fatores com a utilização do Google Authenticator
- Palavras-passe guardadas na base de dados encriptadas em código hash

### Funcionalidades:

- Registar novo Cliente
- Alterar estado de um cliente 
- Alterar dados de um cliente
- Adicionar documentos
- Apagar documentos
- Abrir documentos
- Editar o nome de um documento 
- Gestão de certificados
- Subscrever certificados
- Gestão de empréstimos
- Subscrever empréstimos
- Serviços HomeBanking 
- Alterar estado do HomeBanking
- Consultar histórico de atividades do HomeBanking
- Adicionar titulares
- Remover titulares
- Alterar tipo de titularidade 
- Alterar tipo de conta
- Visualizar movimentos bancários
- Visualizar detalhes de uma transação
- Efetuar transações 
- Criar contas bancárias 
- Alterar estado de uma conta
- Gestão de cartões bancários
- Renovar cartão bancário
- Criar novos cartões bancários
- Visualizar perfil pessoal
- Visualizar histórico de atividades
- Alterar palavra-passe
- Visualizar o perfil de um gestor
- Repor acesso
- Excluir e reativar gestores
- Adicionar um novo gestor
- etc...

### Ferramentas utilizadas:

- StarUML
- Oracle SQL Developer Data Modeler
- Microsoft SQL Server Management Studio 19
- Visual Studio 2022 Community Edition

### Tecnologias utilizadas:

- C#
- HTML
- CSS
- Windows Forms
- ASP .NET
- .NET Framework

### Resultados:

### 1. Serviços Web
Os serviços Web (ou Web services) são métodos que permitem a comunicação entre diferentes sistemas através da Web.

Os serviços Web são API’s (Application Programming Interface) que se comunicam por meio de redes e podem ser combinados para executar operações complexas. Utilizam principalmente o protocolo HTTP (Hyper Text Transfer Protocol), protocolo de comunicação responsável pela transferência de dados entre sistemas.

Os serviços Web não são aplicações Web, apenas transmitem informações entre sistemas.

__SOAP (Simple Object Access Protocol):__ Utiliza XML (Extensible Markup 
Language) para enviar mensagens e geralmente usa o protocolo HTTP para 
transportar dados. O SOAP define um padrão de protocolo de comunicação 
para a troca de mensagens realizadas em XML entre o cliente e o servidor.

Os serviços Web possuem as seguintes vantagens:
- __Integração de informações e sistemas:__ Os serviços Web simplificam a comunicação entre sistemas e aplicações.
- __Reutilização de sistemas existentes:__ Permitem adicionar funcionalidades a sistemas já existentes sem criar tudo do zero.

Foram desenvolvidos Serviços Web com a utilização do protocolo SOAP, de modo que a aplicação de gestão possa utilizar esses métodos.

![Web Service SOAP](https://github.com/D1ogoCS/Projeto-Final/blob/main/webServiceSOAP.png)

*Web Service SOAP*

### 2. Base de dados

Uma base de dados é um conjunto de informações organizadas, armazenadas e geridas de forma estruturada.

Funciona como se fosse uma caixa onde podemos guardar nomes, números de telefone, endereços e outras informações. Essa caixa ajuda-nos a encontrar essas informações rapidamente quando precisamos. As bases de dados são utilizadas noscomputadores para guardar os dados de forma organizada e segura.

A implementação de uma base de dados numa organização é fundamental nos dias atuais, pois permite gerir grandes quantidades de dados e facilita a organização, manutenção e pesquisa dos mesmos. Além disso, as bases de dados são vitais para as organizações, pois são a principal peça dos sistemas de informação e segurança.

#### 2.1 Tabelas

A base de dados do sistema, contém um total de 26 tabelas que resultam da aplicação das regras de transposição do modelo de classes para o modelo relacional, mas apenas oito são responsáveis por garantir as funcionalidades de autenticação e segurança da aplicação. As oito tabelas são as seguintes:

- Tabela “Atividades”

![Tabela “Atividades”](https://github.com/D1ogoCS/Projeto-Final/blob/main/tabelaAtividades.png) 

*Tabela “Atividades”*

- Tabela "Clientes"

![Tabela "Clientes"](https://github.com/D1ogoCS/Projeto-Final/blob/main/tabelaClientes.png) 

*Tabela "Clientes"*

- Tabela "Contas"

![]() 

**

- Tabela "Credenciais"
- Tabela "Gestores"
- Tabela "HistoricoAtividadesClientes"
  
![Tabela "HistoricoAtividadesClientes"](https://github.com/D1ogoCS/Projeto-Final/blob/main/historicoAtividadesClientes.png) 

*Tabela "HistoricoAtividadesClientes"*

- Tabela "HistoricoAtividades"

![Tabela "HistoricoAtividades"](https://github.com/D1ogoCS/Projeto-Final/blob/main/historicoAtividades.png) 

*Tabela "HistoricoAtividades"*

- Tabela "Transacoes"


#### 2.2 Medidas de segurança

- Para evitar os ataques por SQL Injection, são utilizadas consultas parametrizadas ou parâmetros preparados nas aplicações, para evitar a introdução direta de valores nos comandos SQL (Structured Query Language).

- Para uma maior segurança, as palavras-passe guardadas na base de dados, estão codificadas em hash através da utilização do algoritmo SHA-256.

![Palavras-passe codificadas em hash](https://github.com/D1ogoCS/Projeto-Final/blob/main/passwordHash.png) 

*Palavras-passe codificadas em hash através do algoritmo SHA-256*

- Todas as atividades que possam ser executadas nas aplicações (incluindo a autenticação) e que seja necessário o registo do utilizador que as realizou, são executadas através de procedimentos armazenados que estão presentes na base de dados. Todos os procedimentos armazenados possuem em comum alguns parâmetros que identificam o utilizador e indicam a data em que a atividade é realizada. 
Como medida de segurança e auditoria, as atividades realizadas no sistema pelos utilizadores, são registadas nas tabelas apropriadas, nomeadamente na tabela “HistoricoAtividades” e na tabela “HistoricoAtividadesClientes”. Ambas as tabelas possuem trigger’s que não permitem registar atividades em utilizadores que não estejam ativos no sistema, nem permitem que os dados registados sejam alterados.

- A base de dados possui diversos trigger´s em diversas tabelas, o que permite automatizar o sistema.

### 3. Aplicação de gestão
Uma aplicação de gestão (ou aplicação standalone) é uma aplicação completamente autossuficiente. Isso significa que não depende de nenhum software auxiliar para ser executada.

O protótipo da aplicação foi desenvolvido com a utilização do Windows Forms, que é projetado para ser executado em sistemas operativos Windows. 

Oferece uma interface gráfica que permite aos utilizadores interagirem com a aplicação de forma intuitiva.

A aplicação de gestão é utilizada apenas pelos gestores e administradores. 

O gestor realiza diversas atividades no sistema, como a manutenção das contas bancárias e dos produtos dos clientes.
O administrador pode realizar as mesmas atividades do gestor e ainda pode fazer a administração dos gestores do sistema.

![Aplicação de gestão](https://github.com/D1ogoCS/Projeto-Final/blob/main/aplicacaoGestao.png)

*Aplicação de gestão*

#### 3.1 Adicionar um serviço Web
A aplicação de gestão executa alguns serviços Web. Para adicionar os serviços Web à aplicação, foi necessário executar os passos a seguir:

1 - No gestor de soluções do Visual Studio, é necessário clicar com o botão direito do rato em __Connected Services__ e de seguida em __Adicionar Referência de Serviço__.

![Gestor de soluções do Visual Studio](https://github.com/D1ogoCS/Projeto-Final/blob/main/gestorDeSolucoes.png)

*Gestor de soluções do Visual Studio*

![Adicionar Referência de Serviço](https://github.com/D1ogoCS/Projeto-Final/blob/main/adicionarReferencia.png)

*Adicionar referência de serviço no Visual Studio*

2 - Por fim, é necessário configurar o endereço do serviço na janela de Adicionar Referência de Serviço e clicar no botão __Ok__.

![Configurar o serviço Web no Visual Studio](https://github.com/D1ogoCS/Projeto-Final/blob/main/configurarServico.png)

*Configurar o serviço Web no Visual Studio*

#### 3.2 Atenticação
Quando a aplicação é executada, a janela de autenticação é exibida para que o utilizador possa introduzir as suas credenciais e entrar na aplicação.

![Janela de autenticação](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAutenticacao.png)

*Janela de autenticação*

Para o utilizador entrar na aplicação, necessita introduzir o seu nome de utilizador e a sua palavra-passe e depois clicar no botão __Entrar__.

![Introdução das credenciais na janela de autenticação](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAutenticacao2.png)

*Introdução das credenciais na janela de autenticação*

Se as informações introduzidas pelo o utilizador estiverem corretas, o que indica que as credenciais correspondem a um 
utilizador que está registado no sistema, a autenticação passa para a etapa a seguir, onde o utilizador deve introduzir o código de autenticação de dois fatores associado à sua conta.

![Janela para introduzir código de autenticação de dois fatores](https://github.com/D1ogoCS/Projeto-Final/blob/main/2FA.png)

*Janela para introduzir código de autenticação de dois fatores*

![Introdução do código de autenticação de dois fatores](https://github.com/D1ogoCS/Projeto-Final/blob/main/introducao2FA.png)

*Introdução do código de autenticação de dois fatores*

Quando o utilizador introduz o código de autenticação de dois fatores e clica novamente no botão __Entrar__, o código introduzido é verificado por um algoritmo de autenticação de dois fatores da biblioteca “Google.Authenticator”, que oferece métodos para gerar códigos de verificação e verificar a autenticidade dos códigos introduzidos pelo utilizador.

A biblioteca “Google.Authenticator” é gratuita e necessita de ser instalada a partir do gestor NuGet presente no Visual Studio (https://www.nuget.org/packages/GoogleAuthenticator/3.2.0). 

A biblioteca funciona em conjunto com a aplicação Google Authenticator para dispositivos móveis. O Google Authenticator é uma ferramenta gratuita para autenticação de dois fatores,que gera códigos temporários que são usados em combinação com a palavra-passe para adicionar uma camada extra de segurança à autenticação (https://support.google.com/accounts/answer/1066447?hl=en&co=GENIE.Platform%3DAndroid).

#### 3.3 Menu
Após a autenticação do utilizador na aplicação, é apresentado o menu. Existe um menu específico para cada tipo de utilizador.

![Menu dos gestores](https://github.com/D1ogoCS/Projeto-Final/blob/main/menuGestor.png)

*Menu dos gestores*

![Menu dos administradores](https://github.com/D1ogoCS/Projeto-Final/blob/main/menuAdmin.png)

*Menu dos administradores*

Se for a primeira vez que o utilizador entra na aplicação é exibida uma janela solicitando altere a palavra-passe da sua conta.

![Janela para o utilizador alterar a palavra-passe quando faz login pela primeira vez](https://github.com/D1ogoCS/Projeto-Final/blob/main/alterarPassword.png)

*Janela para o utilizador alterar a palavra-passe quando faz login pela primeira vez*

#### 3.4 Gestão de clientes
É possivel visualizar todos os clientes que estão registados no sistema. É exibida uma janela que contém uma tabela com todos os clientes registados no sistema.

![Janela "Ver Clientes"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaVerClientes.png)

*Janela "Ver Clientes"*

O utilizador pode pesquisar um cliente na barra de pesquisa através do NIF (Número de Identificação Fiscal).

Para o utilizador conseguir visualizar os dados de um cliente em específico, necessita de clicar no botão __Ver detalhes__ da tabela de clientes. Em seguida, é exibida uma janela com todas as informações pessoais do cliente, documentos pessoais e outros dados.

![Janela com as informações do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaInfoCliente.png)

*Janela com as informações do cliente*

![Tabela com os documentos pessoais do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/docsCliente.png)

*Tabela com os documentos pessoais do cliente*

![Outros dados do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/outrasInfoCliente.png)

*Outros dados do cliente*

#### 3.4 Registar novo cliente

![Janela “Adicionar cliente”](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAdicionarCliente.png)

*Janela “Adicionar cliente”*

![Campos obrigatórios que não foram preenchidos](https://github.com/D1ogoCS/Projeto-Final/blob/main/erroAdicionarCliente.png)

*Campos obrigatórios que não foram preenchidos*

Se necessário, é possivel imprimir um documento com os dados do registo do novo cliente

![Janela para confirmar a impressão do documento](https://github.com/D1ogoCS/Projeto-Final/blob/main/confirmarAdicionarCliente.png)

*Janela para confirmar a impressão do documento*

![Impresso com os dados pessoais do client](https://github.com/D1ogoCS/Projeto-Final/blob/main/folhaDadosPessoais.png)

*Impresso com os dados pessoais do cliente (dados fictícios)*

Os documentos da aplicação são construídos através da biblioteca Microsoft Report Viewer, que oferece diversas ferramentas para o desenvolvimento de relatórios. É uma biblioteca gratuita e necessita de ser instalada a partir do gestor NuGet presente no Visual Studio (https://learn.microsoft.com/en-us/sql/reporting-services/application-integration/using-the-winforms-reportviewer-control?view=sql-server-ver16).

#### 3.5 Adicionar documentos
Quando um documento é adicionado, uma cópia do mesmo é guardada numa pasta do computador que guarda os documentos pessoais dos clientes. Os documentos nunca são guardados na base de dados, apenas é guardado a localização dos mesmos. 

![Tabela "Documentos"](https://github.com/D1ogoCS/Projeto-Final/blob/main/tabelaDocumentos.png)

*Tabela "Documentos"*

#### 3.6 Apagar documentos
Antes de apagar o documento, é verificado na base de dados se existe alguma referenciação do documento que se pretende apagar do sistema. Se existir, o documento não é apagado do sistema, apenas o valor da coluna “documentoAtivo” da tabela “Documentos” é alterado para “False”, o que faz com que o documento deixe de aparecer na tabela de documentos pessoais. Se não existir referenciação, a linha que está associada ao documento na tabela “Documentos” é apagada, e consequentemente também é apagado o documento da pasta do computador onde o mesmo está guardado.

#### 3.7 Gestão de certificados

![Janela com os dados de um certificado](https://github.com/D1ogoCS/Projeto-Final/blob/main/gestaoCertificados.png)

*Janela com os dados de um certificado*

![Campo para indicar as unidades que o cliente quer resgatar](https://github.com/D1ogoCS/Projeto-Final/blob/main/resgateUnidades.png)

*Campo para indicar as unidades que o cliente quer resgatar*

É possivel alterar o número da conta bancária associada ao certificado e também resgatar unidades do certificado, imprimir os dados do certificado e visualizar os documentos associados ao mesmo.

Para resgatar unidades do certificado, é necessario indicar a quantidade que o cliente pretende retirar do certificado. A quantia introduzida é adicionada à conta bancária que está associada ao certificado.

#### 3.8 Subscrever certificados

![Janela “Adicionar certificado”](https://github.com/D1ogoCS/Projeto-Final/blob/main/adicionarCertificado.png)

*Janela “Adicionar certificado”*

Se for necessário anexar algum documento pessoal do cliente à subscrição do certificado, o utilizador deve selecionar as caixas de seleção correspondentes aos documentos pretendidos.

![Escolher documentos para anexar na subscrição do certificado](https://github.com/D1ogoCS/Projeto-Final/blob/main/adicionarCertificado2.png)

*Escolher documentos para anexar na subscrição do certificado*

![Gráfico com a projeção dos lucros do certificado](https://github.com/D1ogoCS/Projeto-Final/blob/main/projecaoCertificado.png)

*Gráfico com a projeção dos lucros do certificado*

É possivel imprimir os dados do novo certificado subscrito.

![Impresso com os dados do novo certificado](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoCertificado.png)

*Impresso com os dados do novo certificado (dados fictícios)*

#### 3.9 Gestão de empréstimos

![Janela com os dados de um empréstimo](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaEmprestimo.png)

*Janela com os dados de um empréstimo*

![Tabela com todas as prestações do empréstimo](https://github.com/D1ogoCS/Projeto-Final/blob/main/prestacoesEmprestimo.png)

*Tabela com todas as prestações do empréstimo*

![Tabela com as prestações pendentes do empréstimo](https://github.com/D1ogoCS/Projeto-Final/blob/main/pagarPrestacoes.png)

*Tabela com as prestações pendentes do empréstimo*

#### 3.10 Subscrever empréstimos

![Janela “Adicionar empréstimo”](https://github.com/D1ogoCS/Projeto-Final/blob/main/adicionarEmprestimo.png)

*Janela “Adicionar empréstimo”*

![Escolher documentos para anexar na subscrição do empréstimo](https://github.com/D1ogoCS/Projeto-Final/blob/main/adicionarEmprestimo2.png)

*Escolher documentos para anexar na subscrição do empréstimo*

Após a subscrição, é possivel imprimir os dados do novo empréstimo.

![Impresso com os dados do novo empréstimo](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoEmprestimo.png)

*Impresso com os dados do novo empréstimo (dados fictícios)*

#### 3.11 Serviços HomeBanking
Quando um novo cliente é adicionado ao sistema, o mesmo ainda não possui as credenciais de acesso necessárias para utilizar os serviços online. Apenas os utilizadores que têm acesso à aplicação de gestão podem alterar o estado das credenciais dos clientes.
Quando o cliente não possui credenciais de acesso para o HomeBanking, o campo “Estado” possui o valor de “Inativo”.

![Janela “HomeBanking”](https://github.com/D1ogoCS/Projeto-Final/blob/main/servicosHomeBanking.png)

*Janela “HomeBanking”*

![Botões HomeBanking](https://github.com/D1ogoCS/Projeto-Final/blob/main/botoesHomeBanking.png)

*Botões HomeBanking*

Para atribuir credenciais de acesso ao cliente, o gestor necessita de clicar no botão __Ativar__.

O botão __Cancelar HomeBanking__, serve para o gestor cancelar as credenciais de acesso do cliente à aplicação Web.

Quando o cliente falha cinco vezes a autenticação na aplicação Web, as credenciais ficam bloqueadas. Para as desbloquear o gestor necessita de clicar no botão __Desbloquear Acesso__. Também é possível executar a operação inversa, ou seja, bloquear as credenciais, para isso o gestor necessita de clicar no botão __Bloquear Acesso__.

O botão __Repor Acesso__, permite ao gestor gerar novas credenciais de acesso para o cliente, se o mesmo se esquecer das credenciais atuais ou se houver suspeita de alguém saber das suas informações de acesso à aplicação Web.

Sempre que o gestor desbloqueia, ativa, ou repõe o acesso das credenciais do cliente, necessita de imprimir um documento que contém o nome de utilizador, a palavra-passe e um código QR (código de resposta rápida) para utilizar na aplicação Google Authenticator.

![Impresso com as credenciais de acesso do HomeBanking do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoHomeBanking.png)

*Impresso com as credenciais de acesso do HomeBanking do cliente (dados fictícios)*

Na janela “HomeBanking”, é possível consultar as atividades que o cliente executa na aplicação Web.
Para o gestor visualizar as atividades, necessita de escolher um intervalo de tempo e se for necessário, filtrar os resultados por tipo de atividade.

![Tabela do histórico de atividades do HomeBanking preenchida com algumas atividades](https://github.com/D1ogoCS/Projeto-Final/blob/main/historicoHomeBanking.png)

*Tabela do histórico de atividades do HomeBanking preenchida com algumas atividades*

![Tabela do histórico de atividades do HomeBanking preenchida com algumas atividades através do filtro](https://github.com/D1ogoCS/Projeto-Final/blob/main/historicoHomeBanking2.png)

*Tabela do histórico de atividades do HomeBanking preenchida com algumas atividades através do filtro*

#### 3.12 Gestão de contas bancárias

![Janela com as informações de uma conta bancária](https://github.com/D1ogoCS/Projeto-Final/blob/main/gestaoConta.png)

*Janela com as informações de uma conta bancária*

É possivel modificar os titulares da conta, imprimir as informações, efetuar transações, associar cartões bancários, visualizar os movimentos de conta e ainda alterar o estado da conta.

Para se adicionar um novo titular a uma conta bancária, é necessario introduzir o NIF do novo titular no campo “NIF do titular” (o novo titular já deve estar previamente registado no sistema) e de seguida clicar no botão __Adicionar__.

Quando um cliente deixa de ser titular de uma conta, um trigger é responsável por alterar a conta que está associada aos empréstimos e certificados do cliente que foi removido e que tinham essa mesma conta associada. Assim, os certificados e empréstimos do cliente ficam associados à primeira conta bancária que está registada e que o cliente possui.

Quando um cliente deixa de ser titular de uma conta, um trigger é responsável por desativar todos os cartões que estão associados ao cliente e à conta bancária.

Quando uma conta bancária é excluida do sistema (a conta nunca sai do sistema, é apenas alterado o valor do seu estado na base de dados), todos os cartões bancários associados a esta conta são desativados.

Para se conseguir visualizar os movimentos bancários de uma conta, é necessario na secção “Transações” selecionar a partir de que data se deseja obter os movimentos bancários (mensal, anual ou personalizado).
O botão __Extrato mensal__ exibe todos os movimentos do mês atual do sistema, o botão __Extrato anual__ exibe todos os movimentos do ano atual do sistema e o botão __Pesquisar__ exibe todos os movimentos entre as datas selecionadas (a data inicial necessita de ser inferior à data final).

![Secção “Transações”](https://github.com/D1ogoCS/Projeto-Final/blob/main/seccaoTransacao.png)

*Secção “Transações”*

![Tabela com os movimentos bancários (extrato mensal)](https://github.com/D1ogoCS/Projeto-Final/blob/main/transacoesConta.png)

*Tabela com os movimentos bancários (extrato mensal)*

Os movimentos bancários também podem ser impressos.

![Excerto do impresso com os movimentos bancários](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoTransacoes.png)

*Excerto do impresso com os movimentos bancários (dados fictícios)*

Para visualizar as informações de uma transação, é necessario de clicar no botão __Ver detalhes__ e de seguida, é exibida uma janela com as informações da transação pretendida.

![Janela com informações sobre o pagamento de uma prestação](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaTransacao.png)

*Janela com informações sobre o pagamento de uma prestação*

![Janela com informações sobre uma transferência bancária](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaTransacao2.png)

*Janela com informações sobre uma transferência bancária*

![Impresso com os detalhes de uma transferência bancária](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoDadosTransacao.png)

*Impresso com os detalhes de uma transferência bancária*

#### 3.13 Transação

![Janela "Transação"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaEfetuarTransacao.png)

*Janela "Transação"*

É necessario escolher qual é o tipo da transação, podendo ser um dos seguintes:

→ Levantamento;

→ Depósito;

→ Transferência.

Se a transação for um levantamento ou um depósito, só é necessário indicar a quantia a depositar ou a debitar.

No levantamento, a quantia introduzida deve ser sempre menor ou igual ao saldo disponível na conta.

No caso de ser uma transferência, é necessário indicar a quantia que o cliente quer que seja transferida, bem como o número da conta do destinatário.

![Transação do tipo "Transferência"](https://github.com/D1ogoCS/Projeto-Final/blob/main/transferencia.png)

*Transação do tipo "Transferência"*

Quando se clica no botão __Procurar__, é obtido o nome do titular da conta do destinatário.

Quando se clica no botão __Confirmar__, independentemente do tipo de transação, é executado o Serviço Web “inserirTransacao()”

Depois de se clicar no botão __Confirmar__, para confirmar a transação, é possivel imprimir um documento com informações sobre a transação realizada.

#### 3.14 Criar conta bancária

![Janela "Adicionar conta"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAdicionarConta.png)

*Janela "Adicionar conta"*

Para indicar os clientes que serão titulares da conta, é necessario inserir o NIF de cada titular no campo “NIF do titular” e de seguida, clicar no botão __Adicionar__.

![Os titulares da nova conta são exibidos na tabela](https://github.com/D1ogoCS/Projeto-Final/blob/main/titularesNovaConta.png)

*Os titulares da nova conta são exibidos na tabela*

Para cada titular da conta, deve ser indicado o tipo de titularidade.
Depois de indicar os titulares da nova conta bancária, é necessário especificar qual é o tipo de conta bancária.

![Impresso com os dados da nova conta bancária](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoNovaConta.png)

*Impresso com os dados da nova conta bancária (dados fictícios)*

#### 3.15 Alterar o estado de uma conta bancária

![Botões para alterar o estado da conta](https://github.com/D1ogoCS/Projeto-Final/blob/main/botoesConta.png)

*Botões para alterar o estado da conta*

Os botões quando são acionados, alteram o valor que está presente na coluna “estadoConta” da tabela “Contas”.

Quando se clica no botão __Bloquear Conta__, a coluna “estadoConta” fica com o valor “Bloqueada”. Nesse estado, não é possível alterar os dados da conta, criar cartões bancários para a conta, realizar transações ou receber transferências bancárias. Apenas é possível visualizar os movimentos bancários da conta. 
Para reverter esse estado, é necessario clicar no botão __Ativar Conta__, para alterar o valor da coluna “estadoConta” para “Ativa”.

Através do botão __Apagar Conta__, é possivel fechar uma conta bancária. No entanto, a conta não é excluída do sistema, apenas o valor da coluna “estadoConta” é alterado para “Inativa”. Isso faz com que a conta nunca mais seja visível na aplicação, ou seja, é como se nunca tivesse existido. Por outro lado, as informações relacionadas à conta na base de dados permanecem visíveis.
Quando uma conta bancária é excluida do sistema, todos os cartões bancários associados a esta conta são desativados.

Para excluir uma conta, o saldo necessita de ser nulo, e não pode haver certificados ou empréstimos associados à conta, em que o estado dos mesmos seja "Pendente".

#### 3.16 Gestão de cartões

![Janela com informações de um cartão bancário](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaCartoes.png)

*Janela com informações de um cartão bancário*

Na janela, é possível visualizar o número do cartão, a data de validade, o estado do cartão, o número da conta bancária associada, e ainda se podem realizar as operações de bloquear e desbloquear o cartão, restaurar o PIN (Personal Identification Number) e cancelar o cartão.

![Janela "Adicionar cartão"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAdicionarCartao.png)

*Janela "Adicionar cartão"*

#### 3.17 Perfil Pessoal (utilizador da aplicação de gestão)

![Janela do perfil pessoal](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaPerfilPessoal.png)

*Janela do perfil pessoal*

O utilizador consegue visualizar as atividades e a data em que as mesmas foram realizadas no sistema. Para visualizar as atividades, o utilizador deve selecionar um intervalo de tempo e, se necessário, escolher um tipo de atividade na lista de opções para filtrar as atividades.

![Lista de opções de atividades realizadas pelo utilizador](https://github.com/D1ogoCS/Projeto-Final/blob/main/listaAtividadesRealizadas.png)

*Lista de opções de atividades realizadas pelo utilizador*

As atividades presentes na lista de opções, são atividades que o utilizador já realizou no sistema.

Depois de o utilizador escolher o intervalo de tempo e eventualmente uma atividade para filtrar, necessita de clicar no botão __Pesquisar__ para a tabela ser preenchida com as atividades realizadas no intervalo de tempo escolhido. 

#### 3.18 Alterar Palavra-passe

![Janela para alterar a palavra-passe](https://github.com/D1ogoCS/Projeto-Final/blob/main/alterarPassword.png)

*Janela para alterar a palavra-passe*

Para alterar a palavra-passe, o utilizador deve cumprir algumas regras mínimas de segurança. Estas incluem:

→ Ter entre 10 e 20 caracteres;

→ Ter no mínimo um caracter especial;

→ Ter no mínimo um caracter maiúsculo.

Após o utilizador preencher os campos para alterar a palavra-passe, se todas as regras tiverem sido cumpridas, as linhas que exibem as regras ficarão verdes

![Janela de alterar a palavra-passe com as regras cumpridas](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaPasswordVerde.png)

*Janela de alterar a palavra-passe com as regras cumpridas*

#### 3.19 Gestão de gestores

A gestão dos utilizadores da aplicação de gestão está disponível apenas para utilizadores que sejam administradores do sistema.

![Janela "Ver Gestores"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaVerGestores.png)

*Janela "Ver Gestores"*

Para facilitar a procura de um gestor em específico, pode-se utilizar a barra de pesquisa para filtrar os gestores por nome de utilizador.

![Filtrar os gestores por nome de utilizador](https://github.com/D1ogoCS/Projeto-Final/blob/main/filtrarGestores.png)

*Filtrar os gestores por nome de utilizador*

Para o administrador visualizar o perfil de um gestor, necessita de clicar no botão __Ver detalhes__

![Janela do perfil de um gestor](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaPerfilGestor.png)

*Janela do perfil de um gestor*

O administrador tem a capacidade de aceder ao histórico de atividades do gestor, repor o acesso do gestor à aplicação, alterar o nome e a função do gestor no sistema e ainda, excluir o gestor do sistema.

Se um gestor ou administrador perder o acesso à aplicação, um outro administrador pode repor o acesso.

Após repor o acesso, o administrador deve imprimir o comprovativo com os novos dados de acesso que o gestor vai utilizar para efetuar login na aplicação.

![Impresso com os novos dados do gestor](https://github.com/D1ogoCS/Projeto-Final/blob/main/impressoDadosGestor.png)

*Impresso com os novos dados do gestor*

O administrador pode ainda excluir e reativar os gestores do sistema. O gestores nunca são apagados do sistema, apenas o valor da coluna “estadoGestor” da tabela “Gestores” é alterado para “Inativo”.

#### 3.20 Adicionar gestor

![Janela "Adicionar Gestores"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaAdicionarGestor.png)

*Janela "Adicionar Gestores"*

É necessário indicar o nome do novo gestor e o tipo de função que vai desempenhar no sistema.

Após o administrador preencher todos os campos obrigatórios, necessita de clicar no botão __Confirmar__ e por fim imprimir o documento que contém os dados de acesso à aplicação.

### 4. Aplicação Web

As aplicações Web são acessíveis de qualquer lugar do mundo com conexão à internet. Isso permite que os utilizadores usem serviços e funcionalidades sem restrições geográficas. Podem ser protegidas centralmente no servidor, reduzindo riscos de segurança nos dispositivos dos utilizadores e atendendo a um grande número de utilizadores em simultâneo.

#### 4.1 Autenticação

Para utilizar qualquer funcionalidade da aplicação Web, é necessário estar previamente autenticado. Todas as páginas Web da aplicação possuem um algoritmo que deteta se o utilizador se encontra autenticado ou não. Se o utilizador ainda não estiver autenticado, é redirecionado para a página de autenticação.

A autenticação é essencial na aplicação, para registar todas as atividades realizadas pelo utilizador autenticado no sistema. Cada ação realizada pelo utilizador é registada na tabela “HistoricoAtividadeClientes”, que armazena informações como a data, a atividade e a identificação do utilizador.

A autenticação da aplicação Web, segue a mesma lógica de implementação da autenticação da aplicação standalone.

Na página de autenticação, o cliente (utilizador da aplicação) deve introduzir as suas credenciais de acesso e, se estiverem corretas, inserir o código de autenticação de dois fatores.

![Página de autenticação da aplicação](https://github.com/D1ogoCS/Projeto-Final/blob/main/loginWeb.png)

*Página de autenticação da aplicação*

![Página para introduzir o código da autenticação de dois fatores](https://github.com/D1ogoCS/Projeto-Final/blob/main/codigo2FWeb.png)

*Página para introduzir o código da autenticação de dois fatores*

![Código de autenticação de dois fatores introduzidos na página Web](https://github.com/D1ogoCS/Projeto-Final/blob/main/codigoIntroduzidoWeb.png)

*Código de autenticação de dois fatores introduzidos na página Web*

A palavra-passe que o utilizador introduz, é enviada para o servidor para depois ser encriptada em código hash.

Como o valor introduzido é enviado para o servidor, sem estar previamenteencriptado em hash, qualquer pessoa com acesso ao canal de comunicação, pode visualizar as informações que estão a ser transmitidas. Assim, para melhorar a segurança da aplicação Web, são utilizados os protocolos HTTPS e SSL (Secure Sockets Layer).

O SSL é um protocolo de segurança da Internet que faz a autenticação da identidade de um website e cria um canal criptografado entre o utilizador e o servidor.

Se o cliente inserir uma palavra-passe incorreta, um contador presente na base de dados aumenta, até um máximo de cinco tentativas erradas. Quando o limite máximo de tentativas erradas é atingido, as credenciais de acesso do cliente à aplicação Web ficam bloqueadas e só podem ser desbloqueadas por meio da aplicação de gestão.

Quando o cliente acede à aplicação Web com as credenciais temporárias pela primeira vez, após inserir as credenciais e o código de autenticação de dois fatores, é redirecionado para uma página para alterar o nome de utilizador e a palavra-passe

![Página Web para alterar as credenciais de acesso à aplicação](https://github.com/D1ogoCS/Projeto-Final/blob/main/alterarCredenciaisWeb.png)

*Página Web para alterar as credenciais de acesso à aplicação*

Para alterar as credenciais de acesso à aplicação, o cliente tem de seguir algumas regras de segurança ao alterar o nome de utilizador e a palavra-passe. As regras aplicadas à alteração das credenciais são as seguintes:

→ O nome de utilizador tem de ser único, necessita de ter no mínimo 10 caracteres e pelo menos um caracter maiúsculo;

→ A palavra-passe necessita de ter no mínimo 10 caracteres e precisa de ter pelo menos um caractere especial e um caracter maiúsculo;

→ O nome de utilizador não pode ser igual a palavra-passe.

Após a autenticação do cliente, o menu da aplicação Web é exibido.

![Menu da aplicação Web](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaPrincipalWeb.png)

*Menu da aplicação Web*

#### 4.2 Perfil 

![Perfil do cliente na aplicação Web](https://github.com/D1ogoCS/Projeto-Final/blob/main/perfilWeb.png)

*Perfil do cliente na aplicação Web*

#### 4.3 Alterar palavra-passe

![Página Web para alterar a palavra-passe](https://github.com/D1ogoCS/Projeto-Final/blob/main/alterarPasswordWeb.png)

*Página Web para alterar a palavra-passe*

O cliente deve inserir a palavra-passe atual e a nova palavra-passe e, em seguida, clicar no botão __Continuar__. As regras aplicadas à alteração da palavra-passe são as mesmas descritas anteriormente.

Após clicar no botão, é exibida uma página web para o cliente inserir o código de autenticação de dois fatores e confirmar a alteração da senha.

![Introdução do código de autenticação dois fatores para confirmar alteração da palavra-passe](https://github.com/D1ogoCS/Projeto-Final/blob/main/alterarPasswordWeb2.png)

*Introdução do código de autenticação dois fatores para confirmar alteração da palavra-passe*

#### 4.4 Histórico de atividades

Através da aplicação Web, o cliente tem acesso às atividades que realizou na aplicação.

![Página Web do histórico de atividades do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/ultimasAtividadesWeb.png)

*Página Web do histórico de atividades do cliente*

#### 4.5 Gestão de contas

Com a aplicação, o cliente tem acesso a várias informações sobre as suas contas bancárias, incluindo as últimas transações realizadas, o saldo disponível, os titulares da conta, entre outros.

![Página Web da gestão de contas](https://github.com/D1ogoCS/Projeto-Final/blob/main/contasWeb.png)

*Página Web da gestão de contas*

#### 4.6 Gestão de cartões

A aplicação Web permite que o cliente visualize os cartões bancários das suas contas.

![Página Web com informações dos cartões bancários](https://github.com/D1ogoCS/Projeto-Final/blob/main/cartoesWeb.png)

*Página Web com informações dos cartões bancários*

#### 4.7 Transferência bancária

O cliente através da aplicação Web pode efetuar uma transferência bancária.

![Página Web para realizar uma transferência bancária](https://github.com/D1ogoCS/Projeto-Final/blob/main/transferenciaWeb.png)

*Página Web para realizar uma transferência bancária*

O cliente, por meio da lista de opções, pode escolher a conta da qual deseja debitar o dinheiro para a transferência. Após o preenchimento de todos os campos, é apenas necessário clicar no botão __Continuar__, que vai exibir uma página Web para confirmar a transferência.

![Página Web de confirmação da transferência](https://github.com/D1ogoCS/Projeto-Final/blob/main/transferenciaWeb2.png)

*Página Web da confirmação da transferência*
