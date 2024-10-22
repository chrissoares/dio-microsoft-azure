# Dominando o Armazenamento na Azure

## Contas de Armazenamento

Podem receber dados de vários tipos

**Blob do Azure**: Otimizado para o armazenamento de quantidades massivas de dados não estruturados, como texto ou dado binário.

**Disco do Azure**: fornece discos para máquinas virtuais, aplicativos e outros serviços acessarem e utilizarem.

**Fila do Azure**: serviço de armazenamento de mensagens que fornece armazenamento e recuperação para grandes quantidades de mensagens, cada uma com até 64KB.

**Arquivos do Azure**: configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo Bloco de Mensagens do Servidor.

**Tabelas do Azure**: fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.

### Criando uma conta de armazenamento

#### BÁSICO
 * Definir assinatura (já vem usando a padrão);
 * Grupo de Recursos;
 * Seu nome só pode possuir letras e números;
    * Deve ter entre 3 à 24 caracteres;
    * Deve ser unico entre todos as contas existentes na Azure;
 * Definir a região;
 * Definir o Desempenho:
    * Standard: 
        * Recomendado para a maioria dos cenários.
        * Cobrança conforme o uso do espaço;
    * Premium:
        * Recomendado para cenários que exigem baixa latência;
        * Cobrança pelo espaço total;
        * Discos mais perfomáticos;
 * Definir a redundância:
    * LRS - Três cópias no mesmo datacenter;
    * GRS - Uma cópia fora da região, redundância de zona;
    * ZRS - Três cópias cada uma em um datacenter;
    * GZRS - Uni o GRS e ZRS, cópia em vários Datacenters e redundância em outros Datacenters de uma outra zona;

#### AVANÇADO
 * Configurações de segurança;
 * Configuração de namespace;
 * Configuração do Armazenamento de Blobs:
    * Camada de Acesso:
        * Quente: Otimizado para Dados acessados com frequência, diáriamente;
        * Frio: Otimizado para cenários de backup e dados acessados com pouca frequência;

#### REDE
 * Configurações de acesso à rede:
    * Público de todas as redes;
    * Acesso público de redes virtuais e endereõs de IPs selecionados;
    * Desabilitar acesso público e usar acesso privado;
    
# PROTEÇÃO DE DADOS
 * Configurar recuperação de blobs:
    * Restauração pontual de contêineres;
    * Exclusão temporária para blobs;
    * Exclusão temporária para contêineres;
    * Exclusão temporária para compartilhamento de arquivo;
 * Habilitar controle de versão para blobs;
 * Habilitar o feed de alterações de blob;
 
## Visão de uma Conta de Armazenamento

### Compartilhamento de Arquivos
Compartilhamento de arquivos permite criar uma espécie de "pasta compartilhada" que depois pode ser definida como uma unidade no ambiente Windows (definindo uma letra de unidade).

Possui opções de Camada como Premium com baixa latência, Trasação otimizada, Quente para uso mais comum e Legal otimizado para armazenamento de arquivos online.

Possui opção para configurar o seu backup.

Ao abrir um Compartilhamento de Arquivos, é possível conectar a ele, utilizando a opção Conectar e escolhendo o sistema operacional que será utilizado para isto.

Para Windows, por exemplo, é possível definir uma letra da unidade e obter o script para realizar esta configuração. Uma observação é que como é utilizada a porta 445, mas esta porta pode estar bloqueada pelo fornecedor da internet, uma forma de contornar, é utilizar uma máquina virtual para acessá-la.

### Filas
 * Pode ser usado um nome conforme desejado.
 * Cada fila possui uma URL;
 * É utilizada para armazenar mensagens, onde se pode definir um tempo de expiração;
 * Usado normalmente em aplicações de mensagens; 

### Tabelas;
 * Pode usar nomes simples;
 * Possui uma URL;
 * Pode definir politicas de acesso;
 * Pode definir controle de acessos;

## Migrações do Azure

Permite se programar uma migração, criando uma ideia que vai sendo melhorada a medidade que mais informações vão sendo adicionadas.

Podemos criar projetos para migrar:
 * Servidores, Bancos de dados e aplicativos Web;
 * Banco de dados (apenas);
 * Explorar outros cenários;

Ao criar um projeto definimos a Assinatura e grupo de recursos. 

Nos detalhes do projeto, informamos o nome e o local geográfico onde será realizado.

Em avançado podemos escolher o Método de Conectividade, se é publico ou privado.

Uma das ferramentas disponíveis para realizar a cópia dos dados são:
 * Descobrir - para verificar a rede e localizar computadores;
 * Data Box - Para grande quantidade de dados, a partir de 1TB até 800TB. É fornecido um equipamento para que seja realizado a cópia dos dados;
 * AzCopy - Um aplicativo para realizar a cópia dos arquivos para um Storage Acoount (contêiner), através da configuração de um token de acesso compartilhado (com todas as permissões).
 As instruções estão disponíveis no no DOC's do AzCopy.
 * Gerenciador de Armazenamento do Microsoft Azure (Storage Explorer) - Permite visualizar os armazenamentos existentes, realizando seu gerenciamento, além de permitir que os dados da máquina local seja copiado.
 Deve ser baixado, de acordo com o SO, instalado no computador e realizar a conexão com a conta do Azure.

 