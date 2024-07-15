# Projeto Final
## Implementação de mecanismos de autenticação e segurança em aplicações críticas: Caso de estudo - Sistema de gestão bancária

No meu projeto final de curso, realizei um caso de estudo/protótipo de um sistema de gestão bancária, com o objetivo de criar uma base de dados, uma aplicação de gestão e uma aplicação Web.

### Objetivos do projeto:

- Análise, avaliação e integração de mecanismos de proteção e segurança (blockchain, criptografia, etc);
- Desenvolver dois protótipos funcionais que implementem e integrem vários mecanismos de segurança.

### Temas abordados:

- Criptografia e Encriptação;
- Tecnologia blockchain;
- Chave Móvel Digital como método de autenticação;
- Segurança em aplicações criticas;
- Modelação do sistema - Casos de uso;
- Diagrama de classes;
- Modelo de dados;
- Desenvolver e integrar serviços Web (SOAP);
- Desenvolver uma aplicação de gestão e uma aplicação Web.

### Algumas implementações feitas no projeto:

- Relatórios em tempo real através do Report Viewer;
- Códigos QR em relatórios;
- Manipulação de ficheiros (documentos) através da aplicação de gestão;
- Autenticação de dois fatores com a utilização do Google Authenticator;
- Palavras-passe guardadas na base de dados encriptadas em código hash.

### Ferramentas utilizadas:

- StarUML;
- Oracle SQL Developer Data Modeler;
- Microsoft SQL Server Management Studio 19;
- Visual Studio 2022 Community Edition.

### Tecnologias utilizadas:

- C#;
- HTML;
- CSS;
- Windows Forms.
- ASP .NET;
- .NET Framework;

## Resultados:

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


### 2. Segurança na base de dados
Para uma maior segurança, as palavras-passe guardadas na tabela “Gestores” e na tabela "Credenciais" da base de dados, estão codificadas em hash através da utilização do algoritmo SHA-256.

![Palavras-passe codificadas em hash](https://github.com/D1ogoCS/Projeto-Final/blob/main/passwordHash.png) 

*Palavras-passe codificadas em hash através do algoritmo SHA-256*

### 3. Aplicação de gestão
Uma aplicação standalone é uma aplicação completamente autossuficiente. Isso significa que não depende de nenhum software auxiliar para ser executada.

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

A biblioteca “Google.Authenticator” é gratuita e necessita de ser instalada a partir do 
gestor NuGet presente no Visual Studio (https://www.nuget.org/packages/GoogleAuthenticator/3.2.0). 

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
O gestor pode visualizar todos os clientes que estão registados no sistema. É exibida uma janela que contém uma tabela com todos os clientes registados no sistema.

![Janela "Ver Clientes"](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaVerClientes.png)

*Janela "Ver Clientes"*

O gestor pode pesquisar um cliente na barra de pesquisa através do NIF (Número de Identificação Fiscal).
Para o gestor conseguir visualizar os dados de um cliente em específico, necessita de clicar no botão __Ver detalhes__ da tabela de clientes. Em seguida, é exibida uma janela com todas as informações pessoais do cliente, documentos pessoais e outros dados.

![Janela com as informações do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/janelaInfoCliente.png)

*Janela com as informações do cliente*

![Tabela com os documentos pessoais do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/docsCliente.png)

*Tabela com os documentos pessoais do cliente*

![Outros dados do cliente](https://github.com/D1ogoCS/Projeto-Final/blob/main/outrasInfoCliente.png)

*Outros dados do cliente*


