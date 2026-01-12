# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: [09/01/2026]
Empresa: Abstergo Industries. 
Responsável: [John Peter Oyardo Manrique]

## Introdução
Este relatório apresenta o processo de implementação de ferramentas de nuvem (Cloud Computing) na empresa [Abstergo Industries], realizado por [John Peter Oyardo Manrique]. 

O objetivo do projeto é elencar três serviços da AWS com a finalidade de realizar a redução imediata de custos operacionais em uma empresa farmacêutica que não possui qualquer infraestrutura em nuvem instalada. A empresa analisada atua como uma farmácia distribuidora, funcionando como um hub de distribuição para outras farmácias, realizando a revenda de produtos farmacêuticos no modelo B2B (Business to Business).

Atualmente, a organização não possui experiência no uso de serviços em nuvem, nem dispõe de soluções baseadas em cloud computing. Diante desse cenário, torna-se necessário o desenvolvimento de um modelo de negócio em nuvem, estruturado em três etapas e baseado principalmente em três serviços centrais da AWS, com o objetivo de organizar, otimizar e tornar mais eficiente a estrutura de custos operacionais da empresa, garantindo escalabilidade e previsibilidade financeira.

Além disso, o projeto busca demonstrar como a adoção da computação em nuvem pode atuar como uma solução de otimização do modelo de negocios da empresa com foco na gestão financeira, apoiando a tomada de decisão estratégica para a redução de custos, ao mesmo tempo que evidencia as vantagens operacionais e de flexibilidade da nuvem em comparação com uma implementação tradicional baseada exclusivamente em infraestrutura física.

# Objetivo Estratégico da Solução

O presente projeto propõe a adoção gradual de computação em nuvem por uma empresa farmacêutica que atua como hub de distribuição B2B, atualmente sem infraestrutura em cloud. Pretende-se reduzir o investimento da empresa relacionado a altos custos fixos com servidores, softwares em geral e bases de dados, bem como mitigar a baixa elasticidade e os riscos operacionais inerentes à infraestrutura física tradicional.
O objetivo é reduzir custos imediatos, aumentar a previsibilidade financeira e modernizar a operação, utilizando três serviços principais da AWS, implementados em três etapas.

# Arquitetura da Solução AWS

A solução proposta estabelece os princípios para o desenvolvimento do modelo de negócios em nuvem, considerando a segurança dos dados, das transações, dos processos de pagamento e o desenvolvimento eficiente de cada uma das necessidades da empresa, sem depender de infra-estrutura física própria realizando uma implementação do modelo de negócio em cloud, considerando:

1.	Pagamento sob demanda (On-Demand Cost Model)
2.	Redução de investimentos iniciais (CapEx)
3.	Elasticidade automática conforme a demanda
4.	Alta disponibilidade e resiliência
5.	Simplicidade operacional e rápida adoção
6.	Implementação incremental com retorno rápido

A arquitetura em nuvem é concebida para endereçar três desafios centrais da distribuidora farmacêutica: 

  - Custos fixos elevados associados à infraestrutura local; 
  - Baixa flexibilidade operacional para absorver variações de demanda; e 
  - Risco financeiro decorrente da indisponibilidade de sistemas críticos.
  
Para isso, a solução utiliza apenas três serviços centrais da AWS, integrados de forma coerente, assegurando que a empresa pague exclusivamente pelos recursos efetivamente utilizados, escale automaticamente conforme o volume de pedidos e elimine a necessidade de investimentos antecipados em hardware. O foco da solução não está na complexidade tecnológica, mas na eficiência econômica, simplicidade operacional e no rápido retorno sobre o investimento.

O princípio adotado consiste no uso do Modelo de Custo Variável sob Demanda (On-Demand Cost Model), fornecido pela AWS, que permite à empresa utilizar infraestrutura de tecnologia sem a necessidade de adquirir servidores ou equipamentos antecipadamente, pagando apenas pelos recursos efetivamente utilizados. Nesse modelo, os custos acompanham o volume real da operação, eliminando gastos com infraestrutura ociosa e reduzindo significativamente o risco financeiro inicial do modelo de negócio da empresa farmacêutica.

Na presente solução, considera-se a infraestrutura de hardware e software como base do modelo operacional e seu impacto direto no negócio da empresa. Na prática, para este caso, evidencia-se como as soluções fornecidas pela AWS representam um diferencial relevante em relação ao modelo tradicional. Por exemplo, um banco de dados gerenciado na AWS (Amazon RDS) pode custar aproximadamente US$ 25 a US$ 40 por mês para instâncias de pequeno porte e entre US$ 120 e US$ 180 por mês para uma instância de produção de porte médio, operando 24 horas por dia, já incluindo backups automáticos e alta disponibilidade. O armazenamento de dados no Amazon S3 apresenta custos escalonáveis e otimizados, com valores médios de US$ 0,023 por GB/mês para dados ativos, US$ 0,0125 por GB/mês para dados pouco acessados (Standard-IA) e cerca de US$ 0,004 por GB/mês para arquivos históricos no Glacier (valores são só exemplos de referência).

Em consequência, considerando a solução proposta neste projeto — composta por Amazon RDS, Amazon S3 e AWS Amplify — o custo mensal total da infraestrutura em nuvem situa-se, de forma conservadora, entre US$ 180 e US$ 280 por mês, variando conforme o volume de dados e acessos ao sistema. Em contraste, uma infraestrutura tradicional sem o uso de nuvem exigiria um investimento inicial típico entre US$ 8.000 e US$ 15.000 em servidores e licenças, além de custos mensais recorrentes com energia, refrigeração, manutenção e suporte técnico, frequentemente superiores a US$ 400 a US$ 600 por mês, mesmo quando a capacidade instalada não é plenamente utilizada.

Dessa forma, a adoção da AWS converte custos fixos elevados em custos variáveis previsíveis, melhora o controle financeiro, reduz a necessidade de capital imobilizado e diminui riscos operacionais, oferecendo uma base tecnológica escalável, segura e financeiramente mais eficiente para o crescimento da empresa farmacêutica.

Arquitetura Geral da Solução em Nuvem: A arquitetura proposta para o desenvolvimento de um hub de distribuição farmacêutico baseia-se em um modelo web centralizado, altamente escalável e financeiramente previsível, operando integralmente na AWS Cloud. Essa arquitetura é organizada em três camadas principais, cada uma responsável por uma função específica do negócio e suportada por serviços gerenciados da AWS.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, seráo descritas as etapas do projeto:

Etapa 1: 
- [AWS Amplify]
- [O AWS Amplify é um serviço gerenciado da AWS voltado à hospedagem, implantação e operação de aplicações web modernas, abstraindo a complexidade da infraestrutura do negocio. O serviço elimina a necessidade de servidores web dedicados, balanceadores de carga manuais ou configurações complexas de rede, oferecendo implantação automatizada, gerenciamento simplificado e escalabilidade nativa da aplicação. Além da hospedagem, o Amplify integra um conjunto de ferramentas que facilita a construção de aplicações full-stack, permitindo a integração do front-end com serviços de backend da AWS, como autenticação de usuários, armazenamento de arquivos e APIs, sem exigir conhecimento aprofundado em infraestrutura de nuvem. Essa abordagem acelera o desenvolvimento e reduz o esforço operacional ao longo do ciclo de vida da aplicação.]
- [Descrição de caso de uso: Esta camada representa o ponto de entrada do negócio e o principal canal de interação entre as farmácias clientes e os gestores internos. O acesso ao sistema ocorre por meio 
de um portal web seguro, hospedado no AWS Amplify. Farmácias clientes acessam o portal web do hub, hospedado e gerenciado pelo AWS Amplify. A escalabilidade ocorre de forma automática, permitindo que o sistema suporte desde baixos volumes de acesso até picos elevados de demanda — como campanhas comerciais ou períodos de fechamento mensal — sem necessidade de intervenção técnica ou reprovisionamento manual de recursos. Impacto financeiro direto: A empresa elimina custos fixos associados à infraestrutura web tradicional e reduz significativamente o esforço operacional e os custos de manutenção.]

Etapa 2: 
- [Amazon RDS]
- [O Amazon RDS (Relational Database Service) é um serviço de banco de dados totalmente gerenciado da AWS, que simplifica a configuração, operação e escalabilidade de bases de dados relacionais em nuvem. O serviço automatiza tarefas operacionais como provisionamento, backups, atualizações, aplicação de patches e recuperação de falhas, permitindo que a empresa concentre seus esforços na operação 
do negócio, e não na administração da infraestrutura. O RDS oferece suporte a motores de banco de dados amplamente utilizados no mercado, como PostgreSQL e MySQL, além de recursos de alta disponibilidade por 
meio de implantações Multi-AZ, garantindo redundância e failover automático. A escalabilidade é ajustada conforme o crescimento da operação, atendendo tanto a cargas moderadas quanto a aumentos significativos no volume de transações.]
- [Descrição de caso de uso: No núcleo da arquitetura encontra-se a camada de processamento e dados, sustentada por um banco de dados relacional gerenciado por meio do Amazon RDS. Essa camada é responsável pelo armazenamento e gerenciamento das informações críticas do negócio, incluindo pedidos realizados pelas farmácias clientes, dados de estoque e o histórico de vendas e transações. Todas essas funcionalidades são disponibilizadas sem a necessidade de uma equipe dedicada para administração do banco de dados, As solicitações de pedidos e consultas de estoque são processadas pela aplicação e registradas de forma transacional no Amazon RDS, reduzindo a complexidade operacional, os custos de suporte especializado e o risco de indisponibilidade de sistemas críticos.Impacto financeiro direto: Redução de custos com administração especializada, diminuição do risco de falhas críticas e eliminação de paradas não planejadas que poderiam resultar em perdas financeiras.]

Etapa 3: 
- [Amazon S3]
- [O Amazon S3 (Simple Storage Service) é um serviço de armazenamento de objetos totalmente gerenciado pela AWS, projetado para armazenar e recuperar grandes volumes de dados com alta escalabilidade, segurança e durabilidade. O serviço oferece disponibilidade líder de mercado e durabilidade de 99,999999999%, sendo amplamente utilizado em cenários corporativos que exigem confiabilidade e conformidade regulatória. Uma das principais características do Amazon S3 é a possibilidade de classificar os dados em diferentes classes de armazenamento conforme sua frequência de acesso. Essa abordagem permite otimizar custos operacionais ao manter dados frequentemente acessados em camadas de maior desempenho, enquanto informações históricas ou pouco utilizadas são armazenadas em camadas de menor custo, como o S3 Standard-IA e o S3 Glacier.]
- [DescriÃ§Ã£o de caso de uso: A camada de armazenamento é suportada pelo Amazon S3, que atua como o repositório central de documentos e conteúdos corporativos da empresa. Nela são armazenados catálogos de medicamentos, notas fiscais, relatórios financeiros e de auditoria, bem como documentos exigidos por órgãos reguladores. Essa estratégia elimina a necessidade de servidores de arquivos locais, Catálogos de produtos, documentos fiscais e relatórios gerenciais são armazenados e acessados diretamente a partir do Amazon S3, reduz custos com backup e garante que cada tipo de informação seja armazenado no nível de custo mais adequado ao seu uso, evitando desperdícios de recursos e assegurando conformidade legal a um custo mínimo. Impacto financeiro direto: Substituição completa de servidores de arquivos locais, redução dos custos com backup e atendimento a requisitos de conformidade legal com custo mínimo e alta confiabilidade.]



## Conclusão
A implementação de ferramentas na empresa *[Abstergo Industries] tem como esperado [Economia de recursos e custo, Escalabilidade, Elasticidade e Disponibilidade]*, o que aumentarÃ¡ a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

[lista de anexos, como manuais, documentos, planilhas, entre outros]

Assinatura do Responsável pelo Projeto:

[John Peter Oyardo Manrique jpomanrique@gmail.com]





