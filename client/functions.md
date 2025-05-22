# Funções disponíveis no Clientside através do **esx:getSharedObject**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX.ShowLoadingPrompt`    | void  | msg, type                        | Habilita o indicador de carregamento do GTA com uma mensagem.
| `ESX.HideLoadingPrompt`    | void  |                                  | Esconde o indicador de carregamento do GTA.
| `ESX.RequestNetworkControlOfEntity`  | void  | entity, showHelp, timeoutDuration |
| `ESX.Game.IsCurrentSessionValid`      | bool     |              | OBSOLETO: Retorna se a sessão atual é válida.
| `ESX.Game.GetNetIdFromEntity`   | number   | entity          | Retorna o NetId atribuído a uma Entity.
| `ESX.Game.GetVehicleFromNetId`  | Vehicle  | netId           | Retorna o Vehicle atribuído ao NetId.
| `ESX.Game.GetObjectFromNetId`   | Object   | netId           | Retorna o Object atribuído ao NetId.
| `ESX.Game.GetPedFromNetId`      | Ped      | netId           | Retorna o Ped atribuído ao NetId.
| `ESX.Game.IsPedUsingFreemodeSkin`   | bool    | ped            | Retorna se o Ped está utilizando um modelo de personagem do GTA:Online (`mp_m_freemode_01` e `mp_f_freemode_01`).
| `ESX.Game.GetHeadingBetweenCoords`   | number    | coordA, coordB, iParam6                        |
| `ESX.Game.IsEntityFacingDirection`   | bool    | entity, heading, distanceAmount                  |
| `ESX.Game.GetPedMugshot`   | Handle    | ped, useTransparentBg                        |
| `ESX.Game.GetPedMugshotAsBase64`   | string    | ped, useTransparentBg                        | Retorna uma string Base64 contendo um mugshot do Ped indicado. **NÃO** utilize esta função quando o jogo estiver com tela preta!
| `ESX.Game.Teleport`   | void    | entity, coords, cb, keepPedVeh                        |
| `ESX.Game.TeleportPlayer`   | void    | playerPed, coords, range, cb, keepPedVeh                        |
| `ESX.Game.StartLoadScene`   | bool    | coords, range, cb, duration, useFocusArea                        |
| `ESX.Game.SpawnNetObject`   | void    | model, coords, cb, waitForNetwork, isNotDynamic                        |
| `ESX.Game.SpawnObject`   | void    | model, coords, cb, showPrompt, isNotDynamic                        |
| `ESX.Game.SpawnLocalObject`   | void    | model, coords, cb, isNotDynamic                        |
| `ESX.Game.DeleteVehicle`   | void  | vehicle                | Destrói um Vehicle. Recomendo que utilize ESX_DeleteVehicle caso o Vehicle tenha sido criado por um script que não seja a framework. Ou destrua o Vehicle pelo lado do servidor.
| `ESX.Game.DeleteObject`   | void   | object                 | Destrói um Object. Recomendo que utilize ESX_DeleteObject caso o Object tenha sido criado por um script que não seja a framework. Ou destrua o Object pelo lado do servidor.
| `ESX.Game.DeletePed`   | void    | ped                      | Destrói um Ped. Recomendo que utilize ESX_DeletePed caso o Ped tenha sido criado por um script que não seja a framework. Ou destrua o Ped pelo lado do servidor.
| `ESX.Game.SpawnControlledVehicle`   | void    | modelName, coords, heading, onEntityReadyCb, onEntityLostCb, showPrompt, SocietyName, useDistController                        |
| `ESX.Game.SpawnVehicle`   | void    | modelName, coords, heading, onEntityReadyCb, showPrompt, SocietyName, useDistController                        |
| `ESX.Game.SpawnLocalVehicle`   | void    | modelName, coords, heading, cb, showPrompt                        |
| `ESX.Game.Sync.SpawnLocalVehicle`   | Vehicle    | modelName, coords, heading, showPrompt                        |
| `ESX.Game.GetObjects`   | [Object]    | onFoundFunc                        |
| `ESX.Game.GetClosestObject`   | Object    | filter, coords                        |
| `ESX.Game.GetClosestObjectOnList`   | Object    | objects, filter, coords                        |
| `ESX.Game.GetClosestPlayer`   | ID, number    | coords, canGetLocalPlayerPed                        | Retorna o ID do jogador mais próximo e a distância dele. Retornará -1 caso nenhum jogador seja encontrado.
| `ESX.Game.GetPlayersInArea`   | [ID]          | coords, area, returnServerIds                       | Retorna uma lista de jogadores próximos a uma localização e dentro de determinada distância.
| `ESX.Game.GetVehicles`   | [Vehicle]    | onFoundFunc                        |
| `ESX.Game.GetVehiclesInArea`   | [Vehicle]    | coords, area                        |
| `ESX.Game.GetVehicleInDirection`   | Vehicle    | range, checkMapHit, checkObjectHit                        |
| `ESX.Game.GetVehicleInDirectionOfEntity`   | Vehicle    | entity, range, zOffset, checkMapHit, checkObjectHit                        |
| `ESX.Game.GetClosestVehicle`   | Vehicle    | coords                        |
| `ESX.Game.IsSpawnPointClear`   | bool    | coords, radius, noVehsCheck, noObjsCheck, noPedsCheck                        |
| `ESX.Game.GetPeds`   | [Ped]    | ignoreList                        |
| `ESX.Game.GetClosestPed`   | Ped    | coords, ignoreList                        |
| `ESX.Game.ResetVehicleWheelsPairByDecor`   | void    | veh, type, pairId                        |
| `ESX.Game.ResetVehicleSuspensionHeightByDecor`   | void    | veh                        |
| `ESX.Game.Utils.DrawText3D`   | void    | coords, text, size                        |
| `ESX.SetTimeout`   | Handle    | msec, cb                        | Cria um Timeout e retorna um ID único que simboliza este Timeout.
| `ESX.ClearTimeout`   | void    | id                        | Destroi um Timeout criado através de **ESX.SetTimeout**.
| `ESX.IsPlayerLoaded`   | bool    |                         | Retorna **true** ou **false** caso PlayerData já tenha sido preenchido com dados do servidor. 
| `ESX.GetPlayerWhitelistData`   | json    | playerServerId                        |
| `ESX.GetPlayerData`   | json    |                         | Retorna os dados do conta do jogador recebidos do servidor. Caso os dados não estejam disponíveis ainda, retornará **NULL**.
| `ESX.SetPlayerData`   | void    | key, val                        |
| `ESX.IsPlayerSkinLoaded`   | bool    |                         |
| `ESX.TriggerServerCallback`   | void    | name, cb, ...                        | Envia um evento ao servidor e retorna a resposta do servidor através da callback.
| `ESX.GetPickups`   | [Handle]    |                         |
| `ESX.CalculateBestTickPacingByDistance`   | number    | distance                        |
| `ESX.UI.HUD.SetDisplay`   | void    | opacity                        |
| `ESX.UI.HUD.RegisterElement`   | void    | name, label, index, priority, html, data                        |
| `ESX.UI.HUD.RemoveElement`   | void    | name                        |
| `ESX.UI.HUD.UpdateElement`   | void    | name, data                        |
| `ESX.UI.HUD.RewriteElement`   | void    | name, html, data                        |
| `ESX.UI.HUD.RegisterMinimapElement`   | void    | name, index, priority, isVisible, data                        |
| `ESX.UI.HUD.RemoveMinimapElement`   | void    | name                        |
| `ESX.UI.HUD.UpdateMinimapElement`   | void    | name, isVisible, data                        |
| `ESX.UI.HUD.CreateProgressbar`   | Handle    | text, duration, color, onCompletionCb                        | Cria uma UI de barra de progresso e retorna um ID único que representa esta barra de progresso.
| `ESX.UI.HUD.CancelProgressbar`   | void    | id                        | Cancela uma barra de progresso através do ID único.
| `ESX.UI.Menu.RegisterType`   | void    | type, open, close                        |
| `ESX.UI.Menu.Open`   | Menu    | type, namespace, name, data, submit, cancel, change, close                        |
| `ESX.UI.Menu.Close`   | void    | type, namespace, name                        |
| `ESX.UI.Menu.CloseAll`   | void    |                         |
| `ESX.UI.Menu.GetOpened`   | Menu    | type, namespace, name                        |
| `ESX.UI.Menu.GetOpenedMenus`   | [Menu]    |                         |
| `ESX.UI.Menu.IsOpen`   | bool    | type, namespace, name                        |
| `ESX.UI.Menu.IsAnyOpened`   | bool    |                         |
| `ESX.UI.Menu.IsAnyNamespacedOpen`   | bool    | namespace                        |
| `ESX.UI.Menu.ChoosePlayersInArea`   | void    | areaRange, cb, onlyReacheablePlayers, menuTitle                        |
| `ESX.UI.Menu.ChoosePlayersNearbyPos`   | void    | coords, areaRange, cb, onlyReacheablePlayers, menuTitle                        |
| `ESX.UI.Menu.OpenYesNoDialog`   | void    | title, question, submitCb, denyCb, canGoOverNUIs                        |
| `ESX.UI.Menu.GetItemLabelWithExtraData`   | string    | itemData                        |
| `ESX.UI.Menu.GetValidItemAmmoTypeData`   | json, number    | itemData                        |
| `ESX.UI.ShowInventoryItemNotification`   | void    | add, itemData, count                        |
| `ESX.UI.ShowCashNotification`   | void    | add, accountData, symbol, money                        |
| `ESX.UI.ShowWeaponItemNotification`   | void    | add, weaponData, count                        |
| `ESX.NUI.SetNUIActive`   | void    | resourceName, hasFocus, hasCursor                        | Salva em cache o estado do uso de NUI de determinado SCRIPT. Não use esta função se não souber o que está fazendo! Caso esteja procurando uma alternativa a SetNuiFocus, use **ESX_SetNUIFocus**!
| `ESX.NUI.IsAnyNUIOpen`   | bool    | resourceNameToAvoid, withCursorOnly                        | Retorna se no cache da framework há algum script com o Foco na NUI ativo.
| `ESX.DisplayHelpText`   | void    | str, loop, duration                        |
| `ESX.DisplayLongHelpText`   | void    | str, loop, duration, beep, canBeQueued                        |
| `ESX.DisplayLongHelpTextThisFrame`   | void    | str                        |
| `ESX.DisplayMissionText`   | void    | text, time, drawNow                        |
| `ESX.DisplayLongMissionText`   | void    | text, time, drawNow                        |
| `ESX.ShowNotification`   | void    | msg, data                        | Emite uma notificação no jogo utilizando a interface do GTA.
| `ESX.ShowAdvancedNotification`   | void    | title, subject, msg, icon, iconType, data                        | Emite uma notificação no jogo utilizando a interface do GTA.
| `ESX.ShowNUINotification`   | void    | msg, data                        |
| `ESX.GetSocietyIntByName`   | number    | society                        |
| `ESX.GetSocietyNameByInt`   | string    | societyId                        |
| `ESX.GetSocietyLabelText`   | string    | societyInt                        |
| `ESX.GetInventoryItemCount`   | number    | itemName                        |
| `ESX.Camera.CreateTalkingCamera`   | [Camera]    | entity, camHeightOffset                        | Cria uma câmera de diálogo apontando a uma Entity. Retornará o Handle desta câmera.
| `ESX.Camera.DeleteTalkingCamera`   | void    | cam                        | Destrói uma câmera de diálogo.
| `ESX.Admin.GetGroup`   | string    |                         | Retorna o grupo da conta do jogador.