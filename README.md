# Eduquation Project

## Introdução

Nos dias de hoje, a tecnologia tem sido cada vez mais utilizada em diversas áreas, inclusive no ambiente acadêmico. O uso de recursos computacionais em pesquisas, análises e outras atividades acadêmicas é fundamental, mas nem sempre é fácil ou acessível para todos os estudantes e pesquisadores. O estudo referenda pesquisa da Editora Moderna, de julho de 2022, na qual professores do ensino fundamental apontavam a falta de infraestrutura como o maior desafio da rede pública, à frente da falta de suporte familiar e das dificuldades no ensino remoto e da adaptação dos materiais à realidade dos alunos. A fiscalização encontrou também 63% das escolas sem bibliotecas, mesmo índice entre as que não possuem sala de leitura. O percentual de unidades que não possuem laboratório ou sala de informática é ainda maior, 88%.
“Quanto mais sucateada a escola pública, melhor para quem estuda na escola privada. Afinal, tudo que a família do estudante da escola privada quer é uma vaga na excelência do ensino superior público, porque é nas universidades públicas onde se encontram a graduação, a pesquisa e a extensão de qualidade”, analisa.

A conexão remota de recursos computacionais via cloud tem se mostrado uma solução promissora para esses desafios, permitindo que usuários acessem recursos poderosos e especializados de qualquer lugar, a qualquer hora, sem a necessidade de hardware ou software caros e complexos. Neste contexto, este projeto tem como objetivo trazer facilidade e acessibilidade a ambientes acadêmicos, através da conexão remota de recursos computacionais via AWS Cloud. Com isso, espera-se democratizar o acesso a recursos computacionais avançados e permitir que mais estudantes e pesquisadores possam realizar suas atividades com eficiência e qualidade.

## Problema e Oportunidade

A conexão remota de recursos computacionais via cloud apresenta diversas oportunidades e desafios para o ambiente acadêmico. Por um lado, essa tecnologia pode trazer uma série de benefícios, como o acesso a recursos poderosos e especializados que não estariam disponíveis de outra forma, a possibilidade de trabalhar de qualquer lugar, e a economia de recursos financeiros e de tempo. Por outro lado, o uso dessa tecnologia também pode apresentar desafios, como a necessidade de infraestrutura de rede adequada para suportar conexões remotas, a preocupação com a segurança dos dados e sistemas, e a curva de aprendizado para usuários que não estão familiarizados com essa tecnologia.
Entretanto, com a implementação adequada e a adoção consciente por parte das instituições acadêmicas, a conexão remota de recursos computacionais via cloud pode trazer grandes oportunidades para o ambiente acadêmico, facilitando o trabalho de estudantes e pesquisadores e impulsionando o avanço da ciência e tecnologia.


## Oportunidade de Negócio

Atualmente, a maior parte das instituições acadêmicas do país realizam o aporte de máquinas computacionais através do aluguel de computadores,  com quantidade conforme número de alunos esperado e processamento de acordo com o necessário para utilização de softwares que serão úteis nos cursos acadêmicos disponibilizados. Dessa forma, os alugueis das máquinas duram um período determinado de tempo e quando solicitados, limitam a capacidade de recursos que podem ser utilizados conforme o escopo das especificações daquela CPU.
Afim de resolver a limitação da restrição de recursos computacionais e trazer como vantagem a capacidade de estudantes e pesquisadores utilizarem componentes básicos de infraestrutura para acessar sistemas que ampliam as possibilidades de pesquisa e colaboração no ambiente acadêmico, foram propostas as seguintes soluções.

### Plataforma como Serviço: 

Capacidade de vender, através de contrato, uma infraestrutura totalmente auto-gerenciável e escalável que irá suprir toda a necessidade de hardware e sistema operacional das instituições que aderirem o serviço. 

### Software como Serviço:

Uma aplicação disponibilizada às instituições contemplando uma plataforma interativa para disponibilizar matérias, gerar conteúdo, abrir fórums entre os alunos, hospedar atividades.

## Casos de Uso

1. Escolas e Faculdades: possibilidade de compartilhamento de recursos, onde vários usuários podem ter acesso a um mesmo ambiente de trabalho, facilitando a colaboração em projetos acadêmicos. Com a adoção dessa tecnologia, é possível que estudantes e pesquisadores tenham acesso a recursos de alta capacidade sem precisar investir em infraestrutura própria, ampliando as possibilidades de pesquisa e colaboração no ambiente acadêmico.
2. Centros de Pesquisa: a conexão remota de recursos via cloud permite a realização de experimentos em ambientes virtualizados, permitindo que estudantes e pesquisadores testem diferentes cenários em ambientes seguros e controlados,  permitindo o processamento de grandes volumes de dados em áreas como a inteligência artificial e aprendizado de máquina, com recursos de alta capacidade de processamento, como servidores com GPUs especializadas.
3. Pequenas empresas e startups: o escopo deste projeto permite que seja avaliado, para empresas de pequeno porte em número de funcionários, a capacidade de disponibilizar aos colaboradores a realização do trabalho remotamente (home-office) ou num modelo híbrido caso preferível. É possível estabelecer uma relação de confiança entre o domínio AD gerenciado da AWS e o domínio local utilizado pela empresa, gerenciando facilmente os usuários já existentes e sua capacidade de acesso ao novo ambiente disponibilizado na nuvem.

## Roadmap

### Desenvolvimento do Projeto:
![Alt text](eduquation-development-documents/eduquation%20roadmap.png?raw=true "Alcance de público-alvo")

### Alcance de público-alvo:
![Alt text](eduquation-development-documents/publico%20roadmap.png?raw=true "Alcance de público-alvo")

## Definição de Equipe

### Nossa equipe está divida em:

* Product Owner: Leonardo Bonato Bizaro
* Scrum Master: Ariel Pereira dos Santos
* Desenvolvedor: Pedro de Souza Silva

## Soluções Propostas

### Plataforma como Serviço:

#### Solução A
![Alt text](eduquation-development-documents/plataforma-solucao-A.png?raw=true "Solução A PaaS")

Instâncias gerenciadas através do Amazon EC2, que seriam criadas diretamente com conexão ativa ao AD gerenciado da AWS, este por sua vez responsável pelo gerenciamento de todos os usuários que serão criados para aquela instituição. As instâncias seriam criadas a partir de imagens customizadas de Windows 10, criadas via pipeline do EC2 Image Builder, contendo os softwares e ferramentas básicas para realização de determinados cursos.


#### Solução B
![Alt text](eduquation-development-documents/plataforma-solucao-B.png?raw=true "Solução B PaaS")

Instâncias gerenciadas através do AWS Workspaces, que seriam criadas diretamente com conexão ativa ao AD gerenciado da AWS, este por sua vez responsável pelo gerenciamento de todos os usuários que serão criados para aquela instituição. As instâncias seriam criadas a partir de imagens de Windows 10 padronizadas em Bundles do Workspaces, e teriam agendamento de iniciar e pausar instâncias através do EventBridge Scheduler.

### Software como Serviço:

![Alt text](eduquation-development-documents/classroom-solucao.png?raw=true "Solução SaaS")

Instâncias criadas através do Amazon EC2 e gerenciadas pelo EC2 Auto Scaling para garantir sempre a existência de servidores disponíveis, realizando health check na porta 443 do index da aplicação. Além disso, a aplicação roda por trás de um Application Load Balancer para garantir distribuição de carga entre as diferentes instâncias e um IP único de acesso, que é utilizado pelo Amazon Route 53 para fazer resolução de DNS para o endereço eduquation.portal.edu da aplicação. Todo o controle de acesso entre as máquinas e a internet é feito pelo Route Table, que garante acesso do Security Group para o Internet Gateway presente nesta solução, além da garantia de criptografia SSL/TLS do protocolo https através do AWS Certificate Manager.


## Análise de viabilidade econômica

### Plataforma como Serviço:

#### Solução A - Projeção de Custos:

Observação: os cálculos de custos a seguir foram baseados na região de Norte Virgínia - EUA (us-east-1)

Esta solução foi projetada para atender as necessidades de implementação tendo como prioridade a maior redução de custos possível.

Utilizando como base uma escola pública que possui 400 alunos, é possível atingir os seguintes calculos:


* Directory Service AWS Managed Microsoft AD - Standard Edition  ~~USD 86.40/mês, incluindo dois controladores de domínio para alta disponibilidade com 30 dias de free-trial.
* Amazon CloudWatch - Métricas padrões das instâncias não recorrem a custos adicionais; os Logs gerados e armazenados possuem valor de 0,90 USD por GB para Coleta, e 0,0408 USD por GB para Armazenamento. Neste caso, para utilizar o Armazenamento de Logs será necessário realizar configurações adicionais nas instâncias. 
* Amazon EC2 - com tipos de instância para Spot Instances:

![Alt text](eduquation-development-documents/ec2spot-cost-projection.png?raw=true "EC2 Spot Cost Projection")

Com o Amazon EventBridge Scheduler configurado para 4h/dia de execução durante segunda à sexta, totaliza-se, em média, 5.35$/mês para instâncias em Linux e 11.46$/mês para instâncias em Windows. 
Caso a necessidade seja de possuir apenas um laboratório contendo 40 computadores para serem utilizados de forma gradual à todos os alunos, o custo giraria em torno de 214$ para instâncias Linux e 458.65$ para instâncias Windows, ou cerca de R$1050 e R$2200 neste exemplo. 

Por ser um ambiente auto-gerenciável, custos relacionados a despesas operacionais como manutenção, energia elétrica, gerenciamento de servidores, são desconsiderados, e será oferecido suporte ao ambiente do contratado.


#### Solução B - Projeção de Custos:

Observação: os cálculos de custos a seguir foram baseados na região de São Paulo - Brasil (sa-east-1)

Utilizando como base uma faculdade que possui 1440 alunos, é possível atingir os seguintes calculos:


* Directory Service AWS Managed Microsoft AD - Standard Edition  ~~USD 86.40/mês, incluindo dois controladores de domínio para alta disponibilidade com 30 dias de free-trial.
* Amazon CloudWatch - Métricas padrões das instâncias não recorrem a custos adicionais; os Logs gerados e armazenados possuem valor de 0,90 USD por GB para Coleta, e 0,0408 USD por GB para Armazenamento. Neste caso, para utilizar o Armazenamento de Logs será necessário realizar configurações adicionais nas instâncias.      
* Workspaces - Standard with Windows 10 e preços baseados em poder de CPU e processamento:

![Alt text](eduquation-development-documents/workspaces-cost-projection.png?raw=true "WorkSpaces Cost Projection")

Com AutoStop configurado para 4h/dia de execução durante segunda à sexta, totaliza-se, em média, 54$/mês por instância. O custo total de instâncias destinadas para todos os alunos da instituição daria em torno de $77.760.

Importante destacar que esse custo total seria destinado à uma instituição que, neste exemplo, deseja possuir instâncias exclusivas para cada aluno. Caso a necessidade seja de possuir apenas um laboratório contendo 30 computadores para serem utilizados de forma gradual à todos os alunos, o custo giraria em torno de $1.680, ou cerca de R$8.000 neste exemplo. 

Por ser um ambiente auto-gerenciável, custos relacionados a despesas operacionais como manutenção, energia elétrica, gerenciamento de servidores, são desconsiderados, e será oferecido suporte ao ambiente do contratado.

#### Education Pricing

O preço educacional está disponível para WorkSpaces for Qualified Educational Users do Microsoft Windows. Com esta oferta, as organizações educacionais economizam US$ 3,52 por usuário por mês ou US$ 0,03 por usuário por hora usando os descontos de licenciamento da Microsoft. Você pode aproveitar esse desconto se estiver qualificado, com base nos Termos e Documentação de Licenciamento da Microsoft. Caso a instituição esteja elegível para este desconto, ela pode solicitar através do suporte AWS.

### Software como Serviço:

Nossa aplicação de Classroom foi desenvolvida para atingir diversos clientes simultâneamente, com um ambiente escalável e otimizado para suprir as cargas de trabalho que forem necessárias.


* Amazon CloudWatch - Métricas padrões das instâncias não recorrem a custos adicionais; os Logs gerados e armazenados possuem valor de 0,90 USD por GB para Coleta, e 0,0408 USD por GB para Armazenamento. Neste caso, para utilizar o Armazenamento de Logs será necessário realizar configurações adicionais nas instâncias.      
* Instâncias de EC2: utilizando T2.Micro, temos o custo de $0.0116/h,  estimando em 8$ por mês para cada instância rodando 24h/dia.
* DynamoDB Free Tier conta com 25 GB de armazenamento, 25 WCU/mês e 25 RCU/mês. Para nosso primeiro cliente, o Free Tier será suficiente, e para cada GB de armazenamento, o custo aumenta em 0.25$. Conforme a escalabilidade do nosso projeto e o alcanço de novos clientes, podemos utilizar o modo On-demand do banco de dados, atingindo os seguintes valores como projeção:

![Alt text](eduquation-development-documents/dynamodb-cost-projection.png?raw=true "DynamoDB Cost Projection")

* Certificate Manager: 0.75$ por certificado, somente um sendo utilizado (produção).
*  Route53: Domínio .com por 13$ anualmente, somente um sendo utilizado (produção).
* Application Load Balancer - 16$ por ALB funcional/mês, somente um sendo utilizado (produção).

## Personas

### Zé Felipe:

* Arquétipo: Diretor da Instituição;
* 57 anos, casado com 2 filhos, mora no Canhema;
* Prático, utiliza os recursos que tem para resolver os problemas mais imediatos;
* Tem pouco orçamento para a instituição (escola não tem condições de suprir o crescimento da demanda tecnológica);
* Não tem facilidade para organizar/gerenciar os dados da instituição (gasta tempo e recursos além do necessário e não gerencia da forma mais eficiente possível);
* Objetivo: proporcionar uma transformação técnica e de consciência nos alunos que estudam em sua instituição;
* Motivação: sua filha Alice e seu filho Pedro, de 7 e 8 anos respectivamente, que também não tem as melhores condições educacionais.

### Eduardo Rosalém:

* Arquétipo: Professor;
* 28 anos, noivo há 2 anos, mora em St André;
* Analítico, está sempre buscando maneiras de melhorar seus processos;
* Conta apenas com recursos tradicionais para ensino (gerando desvantagem para seus alunos em comparação com alunos de instituições com recursos tecnológicos);
* Precisa de uma forma automatizada para avaliar os desempenhos individuais e de cada classe, para traçar melhor seu plano de ensino;
* Objetivo: atender as necessidades de seus alunos e faze-los ir além do que a instituição oferece;
* Motivação: seu irmão Leonardo de 17 anos que está passando por complicações estudantis por falta de oportunidades quando criança.

### Manoel Gomes:

* Arquétipo: Aluno;
* 13 anos, "nerd", mora no Canhema;
* Introvertido, tem dificuldade de se enturmar, fazer amigos e pedir ajuda;
* Não possui acesso a recursos tecnológicos voltados para a educação;
* Não possui acesso a internet, fora o celular da mãe;
* Tem desvantagens em comparação a alunos de escolas com melhor capacitação tecnológica;
* Objetivo: se tornar um desenvolvedor de jogos profissional;
* Motivação: se interessa muito por vídeos de jogos que vê no youtube, através do celular de familiares quando têm a permissão deles.



## Macro funcionalidades do sistema 

Nosso Product Backlog está atualmente dividido nas seguintes funcionalidades:

*  Criação de Infraestrutura como Serviço 
*  Catálogo de Hardware 
*  ERP - Controle de Processos Internos 
*  Relatório do monitoramento dos recursos 
*  Plataforma como Serviço - Classroom em formato moodle 

## Ambiente de gestão de código e Pipeline

Para versionamento e gestão de código, será utilizado o GitHub, o AWS CodeCommit e AWS CodePipeline para criação de pipelines de CI/CD. 
![Alt text](eduquation-development-documents/aws-codepipeline-cicd.png?raw=true "Gestão de CI/CD")
O AWS CodeBuild será responsável por criar AWS CloudFormations Stacks que separarão os diferentes deployments em ambientes de DEV, HOM e PROD.
![Alt text](eduquation-development-documents/CICD%20base.png?raw=true "Gestão de CI/CD")
## Ambiente da solução 

Todo o ambiente será disponibilizado pela plataforma da Amazon Web Services, aproveitando de todos os recursos existentes e a capacidade de garantir alta disponibilidade, elasticidade e resistência a falhas, podendo cumprir facilmente metas de SLA a serem definidas.


## Arquitetura do sistema


### Plataforma como Serviço:


![Alt text](eduquation-development-documents/plataforma-solucao-B.png?raw=true "Plataforma Infra")

* Oferecendo às instituições todos os recursos necessários para hospedar todos os recursos computacionais em nuvem de forma autogerenciável.

![Alt text](eduquation-development-documents/event-driven-computer-create.png?raw=true "Plataforma Infra")

* Automações que garantem gerenciamento automático dos usuários registrados no domínio do Active Directory e suas respectivas máquinas, com a criação de máquinas e usuários através do AWS Lambda, que se conecta com o AD utilizando as credenciais salvas no Key Management Service, e realiza essa criação.

![Alt text](eduquation-development-documents/event-driven-computer-delete.png?raw=true "Plataforma Infra")

* Automações que garantem gerenciamento automático dos usuários registrados no domínio do Active Directory e suas respectivas máquinas, com a exclusão de máquinas e usuários através do AWS Lambda, que se conecta com o AD utilizando as credenciais salvas no Key Management Service, e realiza essa limpeza.

### Software como Serviço:

![Alt text](eduquation-development-documents/app-classroom-diagram.png?raw=true "App Infra")

* Oferecendo às instituições um software de Classroom para garantir aos alunos e professores a capacidade de gerenciar conteúdos letivos de todas as matérias.


## Autores 
Leonardo Bonato Bizaro, contato: leonardobonatob@gmail.com