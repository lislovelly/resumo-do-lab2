# resumo-do-lab2

## Criando Máquinas Virtuais na Azure e Compreendendo a SLA
A criação de máquinas virtuais (VMs) no Microsoft Azure é um processo essencial para a maioria das operações em nuvem, e entender o Acordo de Nível de Serviço (SLA) é crucial para garantir a disponibilidade e a confiabilidade dos serviços. Aqui está uma visão geral do que aprendi sobre este processo e os diferentes níveis de SLA oferecidos pela Azure.

## Entendendo a SLA
A SLA (Service Level Agreement) define o tempo de atividade garantido por um serviço. No contexto do Microsoft Azure, a SLA estabelece o tempo de inatividade aceitável para diferentes serviços e modelos de implementação. É fundamental compreender essas garantias ao criar serviços na nuvem, pois elas influenciam diretamente a resiliência e a continuidade dos negócios.

## Tempo de Inatividade para Cada Modelo de SLA
O tempo de inatividade aceitável varia de acordo com o nível de SLA contratado. Aqui estão os principais níveis de SLA e seus respectivos tempos de inatividade:

99% de SLA: Aproximadamente 7,31 horas de inatividade por mês.

99,9% de SLA: Aproximadamente 43,8 minutos de inatividade por mês.

99,95% de SLA: Aproximadamente 21,9 minutos de inatividade por mês.

99,99% de SLA: Aproximadamente 4,38 minutos de inatividade por mês.

99,999% de SLA: Aproximadamente 26,3 segundos de inatividade por mês.

## Criando uma Arquitetura com SLA
Ao criar uma arquitetura na Azure, é essencial associar os recursos de forma a atender aos requisitos de disponibilidade desejados. Quanto mais "noves" na SLA (como 99,99% ou 99,999%), menor será o tempo de inatividade aceitável. Em contrapartida, SLAs com menos "noves" terão maior tempo de inatividade, o que pode impactar a continuidade dos serviços.

## Criando uma Máquina Virtual
Na criação de uma VM na Azure, você pode escolher opções de disponibilidade que impactam a SLA:

Conjuntos de Disponibilidade: Agrupam VMs para garantir que não todas estejam no mesmo rack físico, oferecendo maior resiliência a falhas de hardware.

Zonas de Disponibilidade: Garantem que VMs estejam em diferentes datacenters dentro de uma mesma região, aumentando a tolerância a falhas.

Regiões: Implantar VMs em diferentes regiões geográficas para máxima resiliência.

Cada opção de disponibilidade tem um ícone informativo (i) com um resumo das informações e um link para a documentação detalhada, permitindo que os usuários aprendam mais sobre as implicações de cada escolha.

## Contas de Armazenamento e Estratégias de Replicação
A estratégia de replicação dos dados também influencia a SLA e o custo dos serviços de armazenamento:

LRS (Locally Redundant Storage): Replica dados dentro de um único datacenter.
ZRS (Zone-Redundant Storage): Replica dados entre diferentes zonas de disponibilidade na mesma região.
GRS (Geo-Redundant Storage): Replica dados entre regiões geográficas, garantindo maior resiliência a desastres.
GZRS (Geo-Zone-Redundant Storage): Combina a replicação entre zonas e regiões para a máxima disponibilidade e resiliência.
Influência de Datacenters e Regiões
A escolha de datacenters e regiões para hospedar suas VMs e dados tem impacto direto na SLA e nos custos. Datacenters em regiões diferentes podem ter diferentes níveis de SLA e custos associados, com opções de replicação e redundância variando conforme a localização.
