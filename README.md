# HAR Workers

O software propõe uma estratégia baseada em sistemas inteligente para monitoramento de trabalhadores na realização de suas tarefas na indústria, visando prevenir doenças ocupacionais. Dados do sensoriamento de atividades rotineiras de um trabalhador são avaliados pelo software, que implementa reconhecimento de atividade humana, tendo como foco principal limitar o tempo máximo de execução de uma mesma atividade repetitiva.

## Segmentação dos dados

Para segmentação do conjunto de dados coletado, optou-se por uma estratégia baseada em algoritmo de janela deslizante (do inglês, sliding window segmentation) adaptativo, que corrige o tamanho da j-ésima janela com base na maior similaridade em relação a uma possível janela j + 1 subsequente. As janelas são consideradas consecutivas, e não há sobreposição de janelas (overlap), apenas o ajuste de seus tamanhos. Como medida de similaridade entre as janelas, utiliza-se a Correlação de Pearson

## Testes dos algoritmos

O software recebe como entrada um conjunto de dados gerados por acelerômetros triaxiais, que descrevem os movimentos realizados por um trabalhador em suas atividades. Para que seja possível o aprendizado do sistema inteligente de monitoramento, parte desses dados precisam estar devidamente rotuladas com a atividade respectiva que representam. A aquisição de dados não é parte integrante do software, sendo que os dados podem ser obtidos a partir de dispositivos como smartphones e smartwatches;

O software executa o processo de aprendizado de máquina a partir do conjunto de dados de atividades rotuladas, implementando as etapas de treino e teste;

Os classificadores de aprendizado de máquinas gerados podem então ser usados para classificar conjuntos de dados similares, a partir das atividades aprendidas;

O software permite controlar o número limite de repetições de uma atividade repetitiva, de modo a indicar quando é necessária uma pausa ou troca de atividade, com o objetivo de prevenir lesões e doenças laborais.
