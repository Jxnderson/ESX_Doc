# Funções disponíveis no Serverside através do **esx:getSharedObject**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX.SaveLog`    | void  | message, fileName                        |
| `ESX.SaveCmdLog`    | void  | message, source, playersInfos                        |
| `ESX.SavePanelLog`    | void  | message, source                        |
| `ESX.SaveServiceLog`    | void  | message, source                        |
| `ESX.Logs.RegisterExploit`    | void  | source, eventName, eventDesc, data, isHighRisc                        |
| `ESX.Trace`    | void  | str                        |
| `ESX.StringHTMLSanitization`    | string  | text                        | Sanitiza um texto para que ele não contenha tags ou elementos que possam gerar vulnerabilidades em HTML.
| `ESX.GetDistanceBetweenCoords`    | number  | pointA, pointB, useZ                        | Calcula a distância entre duas coordenadas.
| `ESX.GetItemData`   | dynamic  | itemName                        | Retorna as informações gerais de um item pelo seu nome. Retornará NULO caso não existam informações para o nome informado.
| `ESX.IsItemsListLoaded`    | bool  |                         | Retorna TRUE caso a framework tenha carregado as informações dos itens do Banco de dados.
| `ESX.GetBagData`    | dynamic  | itemName                        | Retorna as informações gerais de uma mochila pelo seu nome. Retornará NULO caso não existam informações para o nome informado.
| `ESX.IsBagsListLoaded`    | bool  |                         | Retorna TRUE caso a framework tenha carregado as informações das mochilas do Banco de dados.
| `ESX.SetTimeout`    | Handle  | msec, cb                        | Funciona igual ao SetTimeout nativo, porém retorna um ID único que pode ser usado na função `ESX.ClearTimeout` para cancelar um timeout antes que ele aconteça.
| `ESX.ClearTimeout`    | void  | id                        | Cancela um Timeout que foi criado através da função `ESX.SetTimeout`.
| `ESX.RegisterServerCallback`    | void  | name, cb                          | Registra um callback que pode ser usado pelo cliente para requisitar informações ao servidor.
| `ESX.TriggerServerCallback`     | void  | name, requestId, source, cb, ...  | Usado internamente para receber e executar callbacks de jogadores.
| `ESX.DropPlayerItems`    | void  | xPlayer, reason                        |
| `ESX.SavePlayer`    | void  | xPlayer, endCb, type, dropReason            | `type`: (0 - Save completo | 1 - Save completo devido a quit | 2 - Save de dinheiro)
| `ESX.SavePlayers`    | void  | endCb, doSimpleSave                        |
| `ESX.StartDBPeriodicSyncTimer` | void  |                         |
| `ESX.GetPlayers`    | [ID]  |                         | Retorna uma lista com o ID temporário de todos os jogadores logados.
| `ESX.GetJobPlayers`    | [ID]  | jobName                        | Retorna uma lista com o ID temporário de todos os jogadores logados e que fazem parte de um emprego específico.
| `ESX.GetJobPlayersIndexed`    | [ID: bool]  | jobName                        | Retorna uma lista com o ID temporário de todos os jogadores logados e que fazem parte de um emprego específico.
| `ESX.TriggerFunctionForAllPlayers`     | void  | cb                        | Executa uma função em todos os jogadores logados.
| `ESX.TriggerFunctionForPlayersNearPos` | void  | cb, coords, range                  | Executa uma função em todos os jogadores logados e próximos a determinada coordenada.
| `ESX.TriggerFunctionForJobPlayers`     | void  | cb, jobName                        | Executa uma função em todos os jogadores logados e pertencentes a um emprego específico.
| `ESX.TriggerFunctionForJobsPlayers`    | void  | cb, jobsList                       | Executa uma função em todos os jogadores logados e pertencentes a empregos específicos.
| `ESX.TriggerClientEventForJobPlayers`     | void  | eventName, jobName, ...                        | Envia um evento para todos os jogadores logados e pertencentes a um emprego específico.
| `ESX.TriggerClientEventForJobsPlayers`    | void  | eventName, jobsList, ...                       | Envia um evento para todos os jogadores logados e pertencentes a empregos específicos.
| `ESX.TriggerClientEventForPlayersListIndexed` | void  | eventName, playersList, ...                | Envia um evento para jogadores específicos.
| `ESX.TriggerClientEventForPlayersListed`  | void  | eventName, playersList, ...                    | Envia um evento para jogadores específicos.
| `ESX.GetPlayerFromId`    | xPlayer  | source                        | Retorna o xPlayer de um jogador conectado através do ID temporário.
| `ESX.GetPlayerFromIdentifier`    | xPlayer  | identifier                        | Retorna o xPlayer de um jogador conectado através do ID da conta, ou através de um identifier (caso seja passada uma string de identifier).
| `ESX.GetPlayerFromWhitelistId`    | xPlayer  | id                        | Retorna o xPlayer de um jogador conectado através do ID da whitelist.
| `ESX.RegisterUsableItem`    | void  | itemName, cb                        | Registra um item como usável. Ao ser usado por um jogador, irá executar a função do parâmetro `cb`.
| `ESX.UseItem`    | void  | source, itemName, itemIndex, xPlayer                        | Usado internamente para receber e processar o uso de um item.
| `ESX.CreatePickup`    | Handle,dynamic  | type, name, count, label, player, extraData                        |
| `ESX.DeletePickup`    | void  | id                        |
| `ESX.CreateDisconnectionBag`    | void  | xPlayer, reason, placedAt, carriedMoney, accountsList, itemsList, weaponsList                        |
| `ESX.DeleteDisconnectionBag`    | void  | id                        |
| `ESX.FindPlayerIdentifier`    | string  | source, str                        |
| `ESX.GetPlayerIdentifiersIndexedList`    | [string: string]  | source                        |
| `ESX.GetNextEmptyRoutingBucket`    | number  |                         |