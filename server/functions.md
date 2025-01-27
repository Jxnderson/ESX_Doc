# Funções disponíveis no Serverside através do **esx:getSharedObject**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX.SaveLog`    | void  | message, fileName                        |
| `ESX.SaveCmdLog`    | void  | message, source, playersInfos                        |
| `ESX.SavePanelLog`    | void  | message, source                        |
| `ESX.SaveServiceLog`    | void  | message, source                        |
| `ESX.Logs.RegisterExploit`    | void  | source, eventName, eventDesc, data, isHighRisc                        |
| `ESX.Trace`    | void  | str                        |
| `ESX.StringHTMLSanitization`    | string  | text                        |
| `ESX.GetDistanceBetweenCoords`    | number  | pointA, pointB, useZ                        |
| `ESX.GetItemData`    | dynamic  | item                        |
| `ESX.IsItemsListLoaded`    | bool  |                         |
| `ESX.GetBagData`    | dynamic  | item                        |
| `ESX.IsBagsListLoaded`    | bool  |                         |
| `ESX.SetTimeout`    | Handle  | msec, cb                        |
| `ESX.ClearTimeout`    | void  | id                        |
| `ESX.RegisterServerCallback`    | void  | name, cb                        |
| `ESX.TriggerServerCallback`    | void  | name, requestId, source, cb, ...                        |
| `ESX.DropPlayerItems`    | void  | xPlayer, reason                        |
| `ESX.SavePlayer`    | void  | xPlayer, endCb, isBeingDropped, dropReason                        |
| `ESX.SavePlayers`    | void  | endCb                        |
| `ESX.StartDBSync`    | void  |                         |
| `ESX.GetPlayers`    | [ID]  |                         |
| `ESX.GetJobPlayers`    | [ID]  | jobName                        |
| `ESX.GetJobPlayersIndexed`    | [ID]  | jobName                        |
| `ESX.TriggerFunctionForAllPlayers`    | void  | cb                        |
| `ESX.TriggerFunctionForPlayersNearPos`    | void  | cb, coords, range                        |
| `ESX.TriggerFunctionForJobPlayers`    | void  | cb, jobName                        |
| `ESX.TriggerFunctionForJobsPlayers`    | void  | cb, jobsList                        |
| `ESX.TriggerClientEventForJobPlayers`    | void  | eventName, jobName, ...                        |
| `ESX.TriggerClientEventForJobsPlayers`    | void  | eventName, jobsList, ...                        |
| `ESX.TriggerClientEventForPlayersListIndexed`    | void  | eventName, playersList, ...                        |
| `ESX.TriggerClientEventForPlayersListed`    | void  | eventName, playersList, ...                        |
| `ESX.GetPlayerFromId`    | xPlayer  | source                        |
| `ESX.GetPlayerFromIdentifier`    | xPlayer  | identifier                        |
| `ESX.GetPlayerFromWhitelistId`    | xPlayer  | id                        |
| `ESX.RegisterUsableItem`    | void  | itemName, cb                        |
| `ESX.UseItem`    | void  | source, itemName, itemIndex, xPlayer                        |
| `ESX.CreatePickup`    | Handle,dynamic  | type, name, count, label, player, extraData                        |
| `ESX.DeletePickup`    | void  | id                        |
| `ESX.GetPickupRequestPosString`    | string  | id                        |
| `ESX.CreateDisconnectionBag`    | void  | xPlayer, reason, placedAt, carriedMoney, accountsList, itemsList, weaponsList                        |
| `ESX.DeleteDisconnectionBag`    | void  | id                        |
| `ESX.FindPlayerIdentifier`    | string  | source, str                        |
| `ESX.GetPlayerIdentifiersIndexedList`    | [string: string]  | source                        |
| `ESX.GetNextEmptyRoutingBucket`    | number  |                         |