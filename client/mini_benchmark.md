# Funções disponíveis no Clientside através de **mini_benchmark.lua**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `BeginMiniBenchmarkControllerThread`    | void  |                         | Inicia o thread único de benchmark que calcula a taxa de quadros atual do jogo.
| `StopMiniBenchmarkControllerThread`    | void  |                                  | Encerra o thread de benchmark ativo.
| `GetCurrentMiniBenchmarkFPS`  | number  |  | Retorna a quantidade de FPS atual calculada pelo thread de benchmark.