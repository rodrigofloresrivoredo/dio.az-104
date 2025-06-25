 Gerenciamento de Máquinas Virtuais no Azure

Objetiva: Resumo, anotações como referência para estudo em laboratorios futuros.
________________________________________
 Planejar Máquinas Virtuais
O que é?
A definição dos recursos e estrutura da VM antes da criação.
 O que faz?
Permite escolher o tamanho da VM, imagem base, região, grupo de recursos e armazenamento.
 Onde está no Azure?
Via portal do Azure 
Como fazer?
•	Escolha o Resource Group
•	Defina região geográfica
•	Selecione imagem (Linux, Windows)
•	Defina tamanho da máquina (Standard, e ou outros)
________________________________________
 Criar uma Virtual Machine
 O que é?
Instância de um sistema operacional com recursos alocados em nuvem.
 O que faz?
Executa aplicações, serviços e cargas de trabalho.
 Onde está no Azure?
No menu Máquinas Virtuais
 Como fazer?
az vm create \
  --name minhaVM \
  --resource-group meuRG \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
________________________________________
 Configurar Máquinas Virtuais
•	O que é? Personalização da VM após a criação.
•	O que faz? Define rede, NSGs, discos adicionais, extensões, backup e mais.
•	Onde está? Portal do Azure > VM > Configurações.
•	Como fazer? Configure IPs, instale agentes, adicione discos via portal ou CLI.
________________________________________
 Configurar Disponibilidade de Máquina Virtual
•	O que é? Estratégia de tolerância a falhas e manutenção.
•	O que faz? Evita downtime usando conjuntos de disponibilidade ou zonas.
•	Onde está? Opção ao criar VMs ou via configuração posterior.
•	Como fazer? Use Availability Sets ou Zones.
________________________________________
 Virtual Machine Scale Set
•	O que é? Conjunto de VMs idênticas com escalabilidade automática.
•	O que faz? Escala horizontal conforme demanda.
•	Onde está? "Conjuntos de escalas" no portal.
•	Como fazer? Via Azure CLI ou portal com load balancer e regras de escalabilidade.
________________________________________
Availability Set
•	O que é? Conjunto lógico de VMs distribuídas por domínios de falha e atualização.
•	O que faz? Garante que nem todas VMs sejam afetadas por falha ou manutenção simultânea.
•	Onde está? Durante criação da VM.
•	Como fazer?

az vm availability-set create \
  --name meuAvailabilitySet \
  --resource-group meuRG \
  --platform-fault-domain-count 2 \
  --platform-update-domain-count 5
________________________________________
 Gerenciar Discos (Desanexar/Anexar)
•	O que é? Operação para mover discos entre VMs.
•	O que faz? Permite reaproveitar dados ou migrar volumes.
•	Onde está? No menu de Discos da VM.
•	Como fazer?
1.	Pare a VM
2.	Desanexe o disco
3.	Anexe em outra VM via portal ou CLI
________________________________________
 Dimensionamento da VM
•	O que é? Ajuste de recursos computacionais da VM.
•	O que faz? Garante performance adequada e otimização de custos.
•	Onde está? Menu "Tamanho" da VM.
•	Como fazer? Escolha novo SKU/tamanho e aplique.
________________________________________
 Armazenamento de VM
•	O que é? Tipos e configurações de disco.
•	O que faz? Impacta desempenho de leitura/escrita e custo.
•	Onde está? Seção "Discos" da VM.
•	Como fazer? Escolha entre HDD, SSD, Premium, Ultra
________________________________________
 Conectar-se à VM (Windows)
•	O que é? Acesso via RDP.
•	O que faz? Permite controlar a máquina remotamente.
•	Onde está? Botão "Conectar" > RDP no Portal.
________________________________________
Conectar-se à VM (Linux)
•	O que é? Acesso via SSH.
•	O que faz? Permite administração remota.
•	Onde está? Botão "Conectar" > SSH no Portal.
•	Como fazer? Gere chave SSH e acesse via terminal.
________________________________________
Criar VM do Zero
•	O que é? VM sem imagem padrão (VHD personalizado).
•	O que faz? Usada para migrações ou sistemas customizados.
•	Onde está? Menu "Imagens" ou "Armazenamento".
•	Como fazer? Envie VHD ao Blob e crie VM a partir dele.
________________________________________
Disk Encryption
•	O que é? Criptografia em nível de disco.
•	O que faz? Protege dados em repouso.
•	Onde está? Menu "Discos" > "Criptografia".
•	Como fazer? Configure Azure Key Vault + Azure Disk Encryption.
________________________________________
Planejar Manutenção e Downtime
•	O que é? Prevenção de indisponibilidade.
•	O que faz? Minimiza impactos usando domínios de falha/update e zones.
•	Onde está? Availability Set e Azure Advisor.
•	Como fazer? Distribua VMs corretamente e habilite notificação de manutenção.
________________________________________
Conjuntos de Escalas
•	O que é? Agrupamento de VMs para escalar automaticamente.
•	O que faz? Adiciona ou remove instâncias baseado em demanda.
•	Onde está? Menu "Escalabilidade".
•	Como fazer? Configure regras de CPU, memória ou fila com regras de ação automática.
________________________________________
Comparar Escala Horizontal × Vertical
•	Vertical: aumenta recursos da mesma VM.
•	Horizontal: adiciona múltiplas VMs idênticas.
•	Recomendação: Use horizontal para alta disponibilidade e redundância.
________________________________________
Como configurar Dimensionamento Automático
•	Vá até VM > Escalabilidade
•	Crie regras: CPU > 70% → adicionar VM
•	CPU < 30% → remover VM
•	Defina limites mínimo e máximo

OBS: desculpem, tive dificuldades com a ferramenta.
