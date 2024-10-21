## Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

### Máquinas virtuais

Quando se vai criar uma máquina virtual, podemos optar por:

* Pode criar uma máquina do zero (mais complexo, resultados mais finos);
* Pode criar a partir de uma configuração prédefinida (simplifica o processo);
* Podemos criar a partir de umas configurações pré definidas e também que já vem com aplicações prontas como Wordpress. Simplificando o processo de criação pois os recursos necessários serão criados juntamente.

 ### Criando uma máquina virtual

 #### BÁSICO

  * Definir assinatura (já puxa automático);
  * Definir o Grupo de Recursos em que ela estará vinculada;
  * Definir um nome para esta máquina virtual;
  * Definir em qual região estará localizada;
  * Definir as opções de disponibilidade (relacionado ao SLA, redundância, zonas de disponibilidade);
    * Conjunto de Dimencionamento de Máquinas Virtuais: Possibilita dimencionar a maquina de forma que ela possa crescer de acordo com a demanda de serviço que ela receber, podendo ser de forma manual ou dinamica.
    * O Conjunto de Dimencionamento também pode ser configurado através de uma opção específica do portal do azure.
  * Azure Spot permite que tenha um desconto no valor da máquina virtual, mas seu recurso não é garantido, pois é mantido por recursos que não estão em uso dentro do Azure. Uma vez que esses recursos precisem ser alocados, a máquina virtual configurada com o desconto de Spot, pode ser derrubada para que os recursos alocados por ela sejam utilizados.
  * Definir um tamanho para a VM. Existe uma tabela que facilita identificar o tamanho recumendado de acordo com a necessidade do serviço
    * Pode ser utilizado um Disco de VM já configurado para facilitar estas definições. Bancos costumam usar esta abordagem;
  * Criar uma conta de administrador pra a VM.
  * Definir as portas de entrada:
    * Http (porta 80)
    * Https (porta 443)
    * SSH (porta 22)
    * RDP (porta 3389 - Para conexão remota)

#### DISCOS

 * Definir o Disco para SO:
    * Tamanho;
    * Tipo;
    * Definir se exluir o disco com a VM (evita gasto desnecessário qdo a máquina for removida)
 * Criar disco de dados ou anexar um disco existente;

#### REDE
 * Definir qual rede virtual será utilizada;
 * A rede deve estar na mesma região que a máquina;
 * Podemos definir um ou uma faixa de IP's para que tenham acesso as portas que deixamos expostas;
 * Configurar para que o IP publico seja excluído quando a VM for excluída, economizando nos valores do serviço;

#### GERENCIAMENTO
Configura como que a VM poderá ser gerenciada.

 * Pode utilizar uma Identidade gerenciada atribuída pelo sistema;
 * Pode ser utilizado o Azure AD;
 * Pode programar o desligamento automático da VM, mas não existe o Ligamento automático;
 * Habilitar o Backup
    * Vários backups diários;
    * Camada operacional de 1 a 30 dias;
    * Camada do cofre;
    * Camada de instantâneo resiliente de ZRS;
    Suporte para Início confiável e VMs confidênciais do Azure;

#### MONITORAMENTO

 * Podemos Alertas e definir as suas regras (é enviado um email para o endereço informado);
 * Diagnóstico de inicialização;
 
#### AVANÇADO
Permite instalar uma extensão na VM quando ela subir.
 
#### MARCAS
Pode ser adicionado, elas ajudam a classificar e identificar os recursos;

#### REVISAR + CRIAR
 * Exibe uma estimativa de preço;
 * Possui a descrição dos termos de serviço;
 * Inicia a criação da VM com todas as configurações definidas;

## Área de Trabalho Virtual do Azure

Semelhante a VM, permite a criação de uma área de trabalho virtual que pode ser:
 * Pessoal: 
    * Quando precisa de uma aplicação/software expecífico para a pessoa que vai utilizar;
 * Pool: 
    * Quando podemos compartilhar os recursos;
    * Possui balanceamento de carga;
    * Pode limitar o número máximo de usuários por host;

Pode escolher entre um grupo de Aplicativos:
 * Área de Trabalho;
 * RemoteApp;

Podemos adicionar máquinas virtuais e diversas outras opções.

## Aplicativos de Funções
* Pode se usar código ou uma imagem de contêiner;
* Sobre as linguagens podemos: 
    * Escolher qual utilizar;
    * Sua versão;
    * O sistema operacional (fica restrito para algumas linguagens como Python);
* Podemos escolher o sistema operacional para algumas liguagens;
