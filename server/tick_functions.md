# Funções disponíveis no Serverside através de **tick_functions.lua**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX_Round`    | number  | value, numDecimalPlaces                        |
| `ESX_StringHTMLSanitization`    | string  | text                        |
| `ESX_GetDistanceBetweenCoords`    | number  | pointA, pointB, useZ                        |
| `ESX_TriggerClientEventForPlayersListIndexed`    | void  | eventName, playersList, ...                        |
| `ESX_TriggerClientEventForPlayersListed`    | void  | eventName, playersList, ...                        |
| `ESX_FindPlayerIdentifier`    | string  | source, str                        |
| `ESX_GetPlayerIdentifiersIndexedList`    | [string]  | source                        |