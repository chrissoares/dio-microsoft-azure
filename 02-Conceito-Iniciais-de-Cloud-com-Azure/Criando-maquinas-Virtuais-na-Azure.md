# Criando máquinas Virtuais na Azure

### Opções de SLA 

Quando falamos de SLA, quanto mais noves, menos tempo o recurso podertá ficar indisponível, ex:
| SLA | Tempo de inatividade por semana | Tempo de Inatividade por mês | Tempo de Inatividade por Ano |
| --- | ------------------------------- | ---------------------------- | ---------------------------- |
| 99%    | 1,68 horas                   | 7,2 horas                    | 3,65 dias por ano            |
| 99,9%  | 10,1 minutos                 | 43,2 minutos                 | 8,76 horas por ano           |
| 99,95% | 1,01 minuto                  | 4,32 minutos                 | 52,56 minutos                |
|99,99%  | 5 segundos                   | 25,9 segundos                | 5,26 Minutos                 |

### Como Criar uma máquina virtual

* Pode se escolher a região em que deseja que esta máquina seja criada;

* A opção de disponibilidade esta ligado diretamente ao SLA.

* Quando escolhemos mais de uma Zona de disponibilidade, outras instâncias da máquina que configuramos serão criadas nestas outras zonas.

* Os ícones com um "i" dentro de um circulo mostram dicas rápida sobre a opção em que ele esta inserido, e se clicar na opção Saiba mais, dentro da dica, é aberto um artigo de ajuda sobre aquela opção.
### Armazenamento

* Possui opção de reduncância:
    * Local (em outros equipamentos)
    * Geográfica (em uma outra região secundária)
    * Zona (em um Datacenter de outra zona)
    * Zona Geográfica (em uma zona em outra região geográfica)


