## Configurando uma instância de Banco de Dados na Azure

### Maquinas Virtuais (Imagem e Aquitetura)

 * Podemos escolher qual imagem (sistema da máquina virtual) estará disponível;
 * Para ajudar a escolher uma imagem, existem recomendações no momento da escolha;
 * Para o tamanho, já existe uma previsibilidade do valor mensal;
 * É possível adicionar discos além dos padrões;
 * Quanto a rede pose configurar:
    * Redes virtuais;
    * Endereçamento;
    * Se a máquina ficará exposta para internet;
* Em Gerenciamento podemos habilitar proteção, configurar conexão, habilitar o desligamento automático.
* A criação de uma máquina virtual se torna complexa quando vamos ser mais profissionais, entregando uma máquina virtual que atenda as necessidades sem desperdiçar recursos.

### Banco de Dados SQL
* Escolher em qual grupo de recursos será criado o banco de dados;
* Dar um nome único para o banco de dados;
* Deve estar em um Servidor do banco de dados SQL;
    * O servidor pode ser criado no momento;
    * Deve escolher em qual região será criado;
    * Deve ser definido o método de autenticação;
* Definir a camada de redundância do armazenamento de backup;
* Com base na configuração, já temos uma previsão do seu valor mensal;

