Este repositório documenta a experiência de configurar um Banco de Dados no Microsoft Azure, com base nas aulas do laboratório da DIO. O objetivo é servir como material de consulta e consolidar o conhecimento sobre os serviços de nuvem e a plataforma Azure.

Tipos de Serviços de Nuvem
Antes de iniciar a configuração, é fundamental entender os diferentes modelos de serviços de nuvem e como eles se aplicam à nossa experiência com o Azure.

IaaS (Infraestrutura como Serviço): O provedor oferece a infraestrutura básica (servidores, armazenamento, rede), mas o cliente é responsável por gerenciar o sistema operacional e as aplicações. Exemplo: Máquinas Virtuais.

PaaS (Plataforma como Serviço): O provedor gerencia a infraestrutura e o sistema operacional, permitindo que o cliente se concentre em desenvolver e implantar suas aplicações. O Azure SQL Database é um exemplo de PaaS, o que simplifica a gestão do banco de dados.

SaaS (Software como Serviço): O provedor gerencia tudo, e o cliente apenas usa a aplicação final pela internet. Exemplo: Microsoft Office 365, Gmail.

Passo a Passo da Configuração no Azure
Nesta seção, documentei as etapas essenciais para configurar uma instância de banco de dados no Microsoft Azure, utilizando o modelo PaaS (Plataforma como Serviço) para simplificar a gestão.

Acesso ao Portal do Azure

O primeiro passo foi acessar o Portal do Azure (portal.azure.com) com minha conta. Na página inicial, para criar um novo recurso, cliquei no botão + Criar um recurso no canto superior esquerdo.

Criação do Recurso

Na barra de busca, pesquisei por SQL Database e selecionei a opção correspondente. Fui redirecionado para a página de criação, onde preenchi as seguintes informações:

Assinatura: Selecionei a assinatura Azure for Students.

Grupo de Recursos: Criei um novo grupo de recursos chamado rg-dio-azure-lab para organizar o projeto.

Nome do Banco de Dados: Defini um nome único, como db-dio-lab-123.

Servidor: Cliquei em Criar novo para configurar um servidor de banco de dados, definindo um nome único, a localização (ex: Brazil South) e as credenciais de administrador.

Configurações de Conectividade

Para garantir que o banco de dados pudesse ser acessado de forma segura, configurei as regras de firewall. Na seção Rede, selecionei Ponto de extremidade público e habilitei a opção Permitir que serviços e recursos do Azure acessem este servidor. Em seguida, adicionei meu endereço IP de cliente para permitir o acesso.

