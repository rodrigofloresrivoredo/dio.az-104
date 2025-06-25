# dio.az-104

Notas 

Modulo 1 – (compõe 20-25% do peso da prova)
Microsoft Entra ID ( antigo AD DC One primese)
O Microsoft Entra ID é um sistema na nuvem da Microsoft que cuida da identidade e segurança das pessoas que usam apps e serviços. É como um crachá digital que você apresenta ao entrar em cada sala virtual, e que confirma quem você é.
O que faz?
Ele ajuda empresas a controlar quem pode acessar o quê; e-mails, aplicativos e sistemas, com segurança.
•	Centraliza usuários e grupos em um só lugar.
•	Permite login único (SSO): você entra uma vez e acessa várias apps sem repetir login.
•	Define políticas de acesso condicional 
•	Integra apps de forma tranquila, tanto da Microsoft quanto de terceiros
•	Gera relatórios e logs.  (ajuda em auditoria e conformidade) 
É como se fosse uma recepcionista que só deixa passar quem está autorizado, e ainda registra quem entrou e saiu.
anotação mental: controle completo e registo confiável.
O que usa?
•	Usa protocolos modernos como OpenID e OAuth para verificar a identidade.
•	Oferece funções de segurança como MFA
Resumo: 
•	O que é?
Um sistema de controle de acesso na nuvem, que substituiu o antigo AD.
•	O que faz?
Centraliza identidades, oferece login único, reforça autenticação, aplica políticas seguras, integra apps e registra atividades.
•	Como faz?
Com autenticação e autorização, usando sincronização, políticas, verificação diária e monitoramento contínuo.
Questão de Prova: Criação de conta:  A criação de conta no on primese (AD DC) é replicado para Nuvem e continua a criação no AD dc e não ocorre o contrário.
Diferenças entre autenticação e autorização no Entrad ID.
Autenticação - O que é? Verificar a identidade de um usuário, aplicativo ou serviço.
Exemplo: Quando eu acesso o portal do Microsoft 365 com seu e-mail e senha, o Entra ID confirma que você realmente é quem diz ser.
Autorização - O que é? Determinar o que um usuário pode fazer ou acessar após ser autenticado.
Configurando o Microsoft Entra ID
Questão de prova - Implementando o SSPR
Planos e Preços do Entra ID
Questão de prova - PIM esta apenas para P2 (acesso somente por tempo necessário por autenticação, deve solicitar elevação por aprovação)
Que é? Privileged Identity Management (PIM) 
no Microsoft Entra ID é uma ferramenta para gerenciar e controlar o acesso a funções privilegiadas. Aqui está um resumo das suas principais características e funcionalidades:
Como funciona? 
O PIM permite que você gerencie, controle e monitore o acesso a funções críticas, garantindo que apenas usuários autorizados possam acessar recursos sensíveis.
Quando um usuário precisa assumir uma função específica, de forma temporária, o mesmo loga e solicita para uma aprovador a ativação do PIM. Isso ajuda a garantir que o acesso seja concedido apenas quando necessário.
Permite saber quem ativou quais funções e quando, é possível configurar a exigência de (MFA) ou 
Configurar identidades no Entra ID – BYOD, compatibilidade acima do Windows 10, IOS, Andoid, MacOS, pode ser inventariado pelo MDM e Microsoft Intune.
Dispositivos associados – Cenário 100% Nuvem ou os dois (One primese), ou seja, infraestrutura hibrida.
Gerenciamento de usuários
Questão de Prova: Os usuários excluídos podem ser restaurados por 30 dias. Deve ser identificado se passou dos 30 dias. Informações de log de auditoria e entrada, podem ser verificadas.
Atualizações em Massa 100% em Nuvem
Pode ser feito através de CSV, alimenta com os dados e faz o UpLoad para o Azure Entra ID Serve tanto para excluir quanto para criar usuários.
O SSPR
Questão de prova – Métodos de autenticação; Notificação, telefone celular, telefone comercial, Pergunta de segurança de 3 a 5 a serem registradas.
O que é? Ferramenta que habilita reset de senha/autodesbloqueio pelo usuário
O que faz o SSPR?
Reduz custos e tempo de suporte(Service desk) ao permitir que os usuários façam reset de senha por conta própria.
Os usuários recuperam acesso rapidamente de qualquer lugar 
Garante segurança com flexibilidade e registo de métodos combinados para MFA 
Como ativar: Pré-requisitos → Ativar SSPR no portal → definir métodos e políticas → registro dos usuários → redefinição via portal .
Definir métodos
•	Escolher quantos métodos serão exigidos? (por exemplo, 1 ou 2).
•	Selecionar métodos permitidos: e-mail, SMS, app Authenticator, perguntas de segurança.
•	Utilizar registro combinado para que usuários cadastrem SSPR e MFA ao mesmo tempo 
Criar contas de usuário
O que é? É o processo de adicionar uma nova identidade ao Microsoft Entra ID, que permite ao usuário acessar recursos da organização. 
O que faz? Gera uma conta com propriedades como nome, e-mail, tipo (membro ou convidado), e outros dados. Permite também atribuir funções, grupos ou unidades administrativas no momento da criação. 
Gerenciar contas de usuário
O que é? Abrange ações pós-criação da conta, como editar informações, redefinir senhas, habilitar bloqueios, delegar privilégios e outros.
O que faz? Permite alterar dados de identidade, função, grupo, informações de trabalho ou contato. Também possibilita conceder ou revogar privilégios administrativos. 
Executar atualizações em massa
O que é? É possível a criação ou modificação de contas e atribuições (como licenças), usando arquivos em massa ou scripts.
O que faz? Permite importar contas ou licenças para grandes grupos de usuários, economizando tempo e reduzindo erros manuais.
Como faz? usando modelo CSV no módulo “Configurar contas de usuário e de grupo”. Pode ser feito via powershell.
Criar contas de grupo
O que é?  Criação de objetos de grupo no Entra ID para organizar usuários e gerenciar atribuições coletivas.
O que faz? Cria grupos de segurança ou Microsoft 365, facilitando atribuição de políticas, licenças e funções em conjunto. 
Atribuir licenças a usuários e grupos
O que é? Atribuição de licenças do Microsoft 365 ou outros serviços aos usuários individualmente ou via grupo.
O que faz? Concede permissões de uso de produtos (como Office 365 e outros) de forma individual (manualmente) ou automática via associação a grupos.
Como faz? Usuários individuais: no Centro do Microsoft 365, acessar usuários ativos > licenças, selecionar o que adicionar.
Criar unidades administrativas
O que é?  Uma forma de isolar segmentos dentro do Entra ID, onde administradores gerenciam apenas suas unidades. Exemplo; A TI de uma empresa esta presente em São Paulo, Belo Horizonte e Porto Alegre. É criado uma unidade administrativa para o setor de TI em cada localidade. 
 
O que faz? Permite subdividir a organização para delegação de acesso administrativo local, controlando quem pode gerenciar quais usuários, grupos e políticas por segmento.
Modulo 2: Administrar Governança e Conformidade
Configurar Assinaturas
O que é?  Organização lógica das contas no Azure. A assinatura define limites de cobrança, recursos disponíveis e controle de acesso. Exemplo: o Entra ID é um serviço Global, disponível a todos.
O que faz? Permite separar recursos por ambiente, equipes ou projetos, aplicar políticas, RBAC e monitorar custos. 
Identificar Regiões 
O que é? São os locais geográficos onde os centros de dados do Azure estão disponíveis. 
Qual é? Influenciam latência, disponibilidade e conformidade. Também afetam quota e disponibilidade. 
Como faz? Use o portal ou CLI para listar regiões suportadas. Aplique políticas de “allowed locations” no nível de assinatura. 
Implementar Assinatura no Azure
Questão de prova: mesmo tendo uma conta, pode ter várias assinaturas. Uma assinatura não é suficiente? Resposta; “não” (por conta da administração do Entra ID, fica inviavel). Enfim para um gerenciamento de assinaturas organizadas, uma conta pode estar associada a várias assinaturas.
O que é? A ativação e configuração de uma assinatura.
O que faz? Adiciona recursos, define gestão de identidade, políticas e orçamentos para controlar implantação.
Como faz? Crie via portal, CLI ou API. habilite provedores de recurso, configurar RBAC.
Identificar o Uso da Assinatura
O que é? Monitoramento do consumo de recursos e gastos dentro de uma assinatura.
O que faz? Gera visibilidade de custos, métricas de uso do povo
Como faz? No portal, em Cost Management → Cost analysis, filtros por recurso, grupo, marcações ou período. 
Criar uma Assinatura
Já abordado em "Implementar Assinatura". A criação via portal ("Subscriptions" → "Add") inclui escolha do tipo e configuração inicial.
Determinar Cotas e Limites de Serviço
O que é? Valores máximos de recursos — como número de vCPUs, contas de armazenamento, instâncias de VMs — para cada assinatura. 
O que faz? Garante uso controlado, evita provisionamento excessivo e facilita planejamento. Permite solicitar aumentos se necessário.
Caso de Prova: AO tentar criar um recurso e apresenta um Erro, ultrapassou a cota. Voce abre umacaso de suporte para aumentar a cota. O recurso tem limite padrão, que é a cota de assinatura. É clicar no lapis se estiver habilitar e abrir o caso de suporte para Microsoft.
Grupo de Recursos
O que é? Um contêiner lógico dentro de uma assinatura do Azure que agrupa recursos relacionados (como VMs, bancos de dados, redes) .
•	Cada grupo possui uma localização específica para armazenar seus dados(não necessariamente os recursos estão na mesma região)  
•	Os recursos de um grupo compartilham a mesma governança, políticas e RBAC (controle de acesso por função)  
O que faz?
•	Gerencia recursos como um único conjunto: é possível implantar, atualizar ou remover todos os recursos juntos.
•	Permite aplicar RBAC, políticas e bloqueios no nível do grupo para governança e segurança.
•	Facilita monitoramento e controle de custos, pois o Azure permite filtragem e análise por grupo.
•	Organização lógica e flexível: agrupa recursos por aplicação, ambiente (Dev, Test, Prod), equipe ou projeto.
Como faz?
Via portal Azure
1.	busque por “Resource groups” 
2.	Clique em “+ Create”.
3.	Selecione a assinatura, informe o nome do grupo (deve ser globalmente único) e escolha a região (para armazenamento dos metadados) 
4.	(Opcional) Adicione tags para marcar o recurso (ex.: por departamento, ambiente) 
5.	Clique em “Review + create”, valide e depois em “Create” 
6.	Após a criação, o grupo aparece na lista em “Resource groups” no portal.
Atenção: Os recursos somente podem existir em um grupo de recursos. Os grupos podem ter recursos de muitos tipos diferentes (Serviços) e de muitas regiões diferentes.
Uma vez que o grupo de recursos foi criado, não pode ser renomeado e aninhados. Deve se criar outro e mover os recursos.
Criar uma Hierarquia de Recursos do Azure
Questão de Prova: Revisar com calma!
O que é? Estrutura com management groups, assinaturas, resource groups e recursos. 
 
O que faz? Facilita governança, aplicação de políticas, controle de acesso (RBAC) e organização lógica dos ambientes.
Como faz?
No portal: crie management groups, vincule assinaturas, crie resource groups dentro dessas assinaturas. Aplique políticas globais e RBAC no nível necessário.
Aplicar a Marcação de Recursos
Questão de Prova: A tag é uma marcação e não é repassado ao criar o recurso filho, vai receber? Não. O que pode ser repassado é os Locks e não as tag, a menos que eu coloque uma politica.
O que é? Uso de tags para recursos, grupos ou assinaturas para categorizar e organizar. 
O que faz? Permite identificar propriedade, ambiente, centro de custo; facilita relatórios, automações e alocação de custos. 
Como faz? 
No portal, em qualquer recurso, em “Tags” e definir pares. Pode aplicar via Azure Policy para padronização. Usar “tag inheritance” para propagar valores a recursos filhos. 
Gerenciar Custos
Os custos são específicos dos recursos
O custo de uso pode variar entre os locais (exemplo; Entre USA e Brazil)
Os custos das transferências de dados de entrada e saída diferem.
***  “O modelo de preço é previsível mais não está escrito na pedra.” É necessário usar o mínimo de de recurso de segurança.
É possível programar as VMs para start e Stop nós horários que a operação é baixa ou quase nenhuma.
O que é? Conjunto de práticas e ferramentas para controlar gastos no Azure. Envolve monitoramento, orçamento e otimização.
O que faz? Ajuda a evitar surpresas na fatura, identificar desperdícios, separar custos por equipe/projeto e planejar orçamentos. 
Como faz?
Utilize Cost Management: configure budgets com alertas, monitoramento e relatórios. 
Separe por tags, resource groups ou management groups.
Configurar o Azure Policy
O que é? Serviço de governança que aplica regras automatizadas a recursos no Azure para garantir conformidade, auditoria e correção 
Atenção: A política não que saber que é você! É acesso negado! Na cabeça! Garante a padronização de recurso, independente de que é.
O que faz? Avalia recursos existentes e novos; impõe regras (ex: negar SKUs, forçar tags), aplica correções automáticas, consolida conformidade em dashboards.
Como faz? Cria definições de política, agrupa em iniciativas, atribui a escopos (management groups, assinaturas, RGs); usa portal, CLI ou PowerShell.
Criar Políticas do Azure
O que é? Cria definições de política (Personalizada), que descrevem condições e efeitos aplicáveis a recursos do Azure.
O que faz? Define regras específicas (ex: negar série G de VMs, exigir tags obrigatórias) com aproveitamento de parâmetros.
Como faz? No portal, CLI ou PowerShell: redige JSON com policyRule, condições e efeitos (Audit, Deny, Append, DeployIfNotExists); adiciona parâmetros; publica a definição. 
Políticas do Azure
Caso de prova: Um iniciativa é um conjunto de políticas.  “Você está tentando criar, um recurso tal,que não esta dentro cenário da politica, e não esta dentro padrão e você conseguiu. Como, porque esta no grupo de exclusão”
O que é? Conjunto de deestáções de política (internas e personalizadas) que impõem conformidade em ambientes Azure.
O que faz? Audita e restringe ambientes de nuvem, aplica correções, registra conformidade em tempo real.

Pegadinha do Malandro: foi criando uma política e a policy não esta funcionando? Pede um print da tela “Assign Policy” e verifique se o “check box policy enforcement” está marcado?  Tem que estar habilitado!
Criar Definições de políticas
O que é? Definição de política é a regra em JSON; nome, descrição e parâmetros.
O que faz? Modela condições (ex: tipo de recurso, SKU, tags) e define ações (negar, auditar, anexar, corrigir) a aplicar quando condições não são atendidas 
Definir o Escopo da Definição da Iniciativa
O que é? É o alvo da aplicação de uma iniciativa (Policy Set): pode ser um grupo de gestão, assinatura, grupo de recursos ou recurso individual 
O que faz? Determina onde as políticas da iniciativa serão aplicadas e quais recursos serão impactados; define exclusões para sub‑escopos 
Como faz? Na atribuição de iniciativa, seleciona escopo desejado, opcionalmente adiciona exclusões; herda aplicação automática aos filhos do escopo.
Determinar a conformidade
O que é? Esta tudo dentro das regras do jogo!? Qual é estado de recursos das políticas atribuídas, indicando se estão conformes ou não conformes!
O que faz? Mostra dashboards de conformidade, sinaliza recursos violadores, permite ações corretivas manuais ou automatizadas 
Como faz? Azure Policy avalia periodicamente (eventos de CRUD ou diariamente); consolida dados no portal e em Workbooks; dispara correções ou alertas, conforme configuração.
Configurar Recursos do Azure com ferramentas
O que é?  Automatizar as coisas com ferramentas como Azure CLI, PowerShell, Visual Studio Code e pipelines para provisionar e gerenciar recursos no Azure.
O que faz? Permite criar, atualizar e excluir recursos de forma que agente repetindo o mesmo processar, até vir a cometer erros. Permite automatizar.
Como faz? Utiliza comandos CLI (az), scripts PowerShell ou integrações com IDEs como VS Code + extensões, além de pipelines CI/CD (Azure DevOps, GitHub Actions) 
Configurar Recursos com Modelos ARM
O que é? Modelo ARM é um arquivo JSON declarativo usado pelo Azure Resource Manager para definir a infraestrutura como código 
O que faz? Define toda a estrutura e configuração dos recursos de forma centralizada, permitindo implantações repetíveis, consistentes e gerenciáveis 
Como faz? Cria um template JSON com seções como resources, parameters, variables e outputs, usando ferramentas como VS Code + extensão ARM Tools, e implanta via az deployment ou PowerShell.
Explorar o Esquema de Modelo JSON
O que é? É a estrutura padronizada do template ARM, que segue um schema JSON oficial do Azure para templates.
O que faz? Assegura que o template tenha sintaxe e elementos válidos (versão de schema, recursos, parâmetros, etc.), permitindo validação e implantação corretas.
Explorar os Parâmetros do Modelo JSON
O que é? Elementos parameters que permitem configurar valores dinamicamente em um modelo ARM, tornando-o reutilizável.
O que faz? Permite personalizar valores como nomes, localizações, SKUs etc., sem alterar o template principal, facilitando reutilização e em módulos.
Como faz? Define parâmetros no JSON com tipos, valores padrão e validações.
Considere os Arquivos do Bicep de Azure
O que é? Bicep é uma linguagem que simplifica a criação de templates ARM.
MODULO 4 : Administrar Redes Virtuais
Nota Metal: A parte de rede é onde ocorre mais perguntas de certificação do Azure. Maior pontuação!
Configurar Redes Virtuais
O que é? Rede privada isolada no Azure, permitindo comunicação entre recursos, internet e ambientes híbridos 
O que faz? Cria ambientes de rede isolados, segmenta em sub-redes, conecta VMs, PaaS e on‑premises via VPN ou ExpressRoute 
Como faz? Usando ARM templates, CLI (az network vnet create), PowerShell, ou direto no Portal. Define espaço de endereço e opções como DNS ou emparelhamento.
🛡️ Pontos de atenção:
Escolha espaços IP não sobrepostos, especialmente se integrar com on‑premises 
Use CIDR adequado: /16 para grandes ambientes, /24 para pequenos 
Configurar Grupos de Segurança de Rede (NSG)
O que é? Conjunto de regras de firewall na camada 3 e 4 aplicadas a sub-redes ou interfaces de rede 
O que faz? Permite ou nega tráfego com base em IP, porta e protocolo, controlando tráfego de entrada e saída.
Como faz? Cria NSG com regras (priority, direction, access) via Portal, ARM, CLI ou PowerShell.

🛡️ Pontos de atenção: Priorize regras: restritivas (deny all) devem vir antes das permissivas (ex: HTTP/HTTPS) 
Aplique NSG por subnet e/ ou NIC, conforme granularidade desejada 
Configurar o DNS do Azure
O que é? Serviço de resolução de nomes dentro de VNets, para recursos Azure, híbridos e públicos.
O que faz? Permite resolver nome de VMs, PaaS, endereços públicos/privados, e integra DNS customizado via VNet.
Como faz? Especificando servidores DNS no nível da VNet ou NIC via Portal, CLI ou PowerShell.
🧩 Pontos de atenção:
Use DNS privados para nomes internos; híbrido requer integração do DNS on‑premises.
Planejar Redes Virtuais
O que é? Planejamento estratégico do design de rede: topologia, sub-redes, endereçamento e segurança 
O que faz? Garante escalabilidade, isolamento, integração com ambientes externos e facilita governança.
Como faz? Definindo espaços IP, sub-redes, NSGs, emparelhamentos, VPN/ExpressRoute, e adotando padrões organizacionais 
🚨 Pontos de atenção:
Reserve espaços para crescimento: evite uso de faixas muito pequenas .
Mantenha buffers entre VNets para evitar conflito 
Criar Redes Virtuais
O que é? Implantação concreta de uma VNet com faixa de IP e configurações iniciais.

O que faz? Provisiona o contêiner de rede que sustenta VMs, recursos PaaS e conectividade.
Criar Sub‑redes
O que é? Segmentação lógica da VNet para isolar funções de rede.
O que faz? Aplicar segurança (NSGs), roteamento e distribuição de carga funcional.
Como faz? CLI ou ARM adicionando sub-redes dentro do prefixo da VNet.
🛡️ Pontos de atenção: Sub-redes dividem contêiner de broadcast e permitem aplicar NSG individualmente 
Planejar o Endereçamento IP
O que é? Definição de esquema IP (prefixos, públicos/privados, estáticos/dinâmicos) .
O que faz? Assegura comunicação eficiente, evita conflitos e considera cenários híbridos.
⚠️ Pontos de atenção:
Planejamento que evite sobreposição com redes on‑premises é crítico 
Criar Endereços IP Públicos
O que é? Recursos IP estáticos ou dinâmicos visíveis externamente.
O que faz? Permite acesso externo e define IP fixo para recursos como VMs ou gateways.
Associar Endereços IP Públicos
O que é? Ligação de um IP público a um recurso, como uma interface de rede ou load balancer.
O que faz? Habilita comunicação entre o recurso e a internet ou redes externas.
Como faz? Via Portal ou script que atribui a NIC ou configuração ICP.
Alocar ou Atribuir IPs Privados
O que é? Configuração de IPs internos nas VNets: estático ou dinâmico.
O que faz? Define IP fixo ou automático para comunicação interna.
Como faz? Durante criação de NIC ou VM, especifique --private-ip-address (estático) ou deixe padrão (dinâmico).


