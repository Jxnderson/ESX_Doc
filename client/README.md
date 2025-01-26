# Funções disponíveis no Clientside através do **esx:getSharedObject**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX.ShowLoadingPrompt`    | void  | msg, type                        |
| `ESX.HideLoadingPrompt`    | void  |                                  |
| `ESX.RequestNetworkControlOfEntity`  | void  | entity, showHelp, timeoutDuration |
| `ESX.Game.IsCurrentSessionValid`      | bool     |              |
| `ESX.Game.GetNetIdFromEntity`   | number    | entity          |
| `ESX.Game.GetVehicleFromNetId`   | Vehicle    | netId                        |
| `ESX.Game.GetObjectFromNetId`   | Object    | netId                        |
| `ESX.Game.GetPedFromNetId`   | Ped    | netId                        |
| `ESX.Game.IsPedUsingFreemodeSkin`   | bool    | ped                        |
| `ESX.DisplayHelpText`   | void    | str, loop, duration                        |
| `ESX.DisplayLongHelpText`   | void    | str, loop, duration, beep, canBeQueued                        |
| `ESX.DisplayLongHelpTextThisFrame`   | void    | str                        |
| `ESX.DisplayMissionText`   | void    | text, time, drawNow                        |
| `ESX.DisplayLongMissionText`   | void    | text, time, drawNow                        |
| `ESX.ShowNotification`   | void    | msg, data                        |
| `ESX.ShowAdvancedNotification`   | void    | title, subject, msg, icon, iconType, data                        |
| `ESX.ShowNUINotification`   | void    | msg, data                        |
| `ESX.Game.GetHeadingBetweenCoords`   | number    | coordA, coordB, iParam6                        |
| `ESX.Game.IsEntityFacingDirection`   | bool    | entity, heading, distanceAmount                        |
| `ESX.Game.GetPedMugshot`   | Handle    | ped, useTransparentBg                        |
| `ESX.Game.Teleport`   | void    | entity, coords, cb, keepPedVeh                        |
| `ESX.Game.TeleportPlayer`   | void    | playerPed, coords, range, cb, keepPedVeh                        |
| `ESX.Game.StartLoadScene`   | bool    | coords, range, cb, duration, useFocusArea                        |
| `ESX.Game.SpawnNetObject`   | void    | model, coords, cb, waitForNetwork, isNotDynamic                        |
| `ESX.Game.SpawnObject`   | void    | model, coords, cb, showPrompt, isNotDynamic                        |
| `ESX.Game.SpawnLocalObject`   | void    | model, coords, cb, isNotDynamic                        |
| `ESX.Game.DeleteVehicle`   | void    | vehicle                        |
| `ESX.Game.DeleteObject`   | void    | object                        |
| `ESX.Game.DeletePed`   | void    | ped                        |
| `ESX.Game.SpawnControlledVehicle`   | void    | modelName, coords, heading, onEntityReadyCb, onEntityLostCb, showPrompt, SocietyName, useDistController                        |
| `ESX.Game.SpawnVehicle`   | void    | modelName, coords, heading, onEntityReadyCb, showPrompt, SocietyName, useDistController                        |
| `ESX.Game.SpawnLocalVehicle`   | void    | modelName, coords, heading, cb, showPrompt                        |
| `ESX.Game.Sync.SpawnLocalVehicle`   | Vehicle    | modelName, coords, heading, showPrompt                        |
| `ESX.Game.GetObjects`   | [Object]    | onFoundFunc                        |
| `ESX.Game.GetClosestObject`   | Object    | filter, coords                        |
| `ESX.Game.GetClosestObjectOnList`   | Object    | objects, filter, coords                        |
| `ESX.Game.GetClosestPlayer`   | ID    | coords, canGetLocalPlayerPed                        |
| `ESX.Game.GetPlayersInArea`   | [ID]    | coords, area, returnServerIds                        |
| `ESX.Game.GetVehicles`   | [Vehicle]    | onFoundFunc                        |
| `ESX.Game.GetVehiclesInArea`   | [Vehicle]    | coords, area                        |
| `ESX.Game.GetVehicleInDirection`   | Vehicle    | range, checkMapHit, checkObjectHit                        |
| `ESX.Game.GetVehicleInDirectionOfEntity`   | Vehicle    | entity, range, zOffset, checkMapHit, checkObjectHit                        |
| `ESX.Game.GetClosestVehicle`   | Vehicle    | coords                        |
| `ESX.Game.IsSpawnPointClear`   | bool    | coords, radius, noVehsCheck, noObjsCheck, noPedsCheck                        |
| `ESX.Game.GetPeds`   | [Ped]    | ignoreList                        |
| `ESX.Game.GetClosestPed`   | Ped    | coords, ignoreList                        |
| `ESX.Game.ResetWheelsPairByDecor`   | void    | veh, type, pairId                        |
| `ESX.Game.ResetVehicleSuspensionHeightByDecor`   | void    | veh                        |
| `ESX.Game.GetBetterTickByDistance`   | number    | distance                        |
| `ESX.Game.GetPlayerWhitelistData`   | json    | playerServerId                        |
| `ESX.Game.GetPedMugshotAsBase64`   | string    | ped, useTransparentBg                        |
| `ESX.SetTimeout`   | Handle    | msec, cb                        |
| `ESX.ClearTimeout`   | void    | id                        |
| `ESX.IsPlayerLoaded`   | bool    |                         |
| `ESX.GetPlayerData`   | json    |                         |
| `ESX.SetPlayerData`   | void    | key, val                        |
| `ESX.IsPlayerSkinLoaded`   | bool    |                         |
| `ESX.TriggerServerCallback`   | void    | name, cb, ...                        |
| `ESX.GetPickups`   | [Handle]    |                         |
| `ESX.UI.HUD.SetDisplay`   | void    | opacity                        |
| `ESX.UI.HUD.RegisterElement`   | void    | name, label, index, priority, html, data                        |
| `ESX.UI.HUD.RemoveElement`   | void    | name                        |
| `ESX.UI.HUD.UpdateElement`   | void    | name, data                        |
| `ESX.UI.HUD.RewriteElement`   | void    | name, html, data                        |
| `ESX.UI.HUD.RegisterMinimapElement`   | void    | name, index, priority, isVisible, data                        |
| `ESX.UI.HUD.RemoveMinimapElement`   | void    | name                        |
| `ESX.UI.HUD.UpdateMinimapElement`   | void    | name, isVisible, data                        |
| `ESX.UI.HUD.CreateProgressbar`   | Handle    | text, duration, color, onCompletionCb                        |
| `ESX.UI.HUD.CancelProgressbar`   | void    | id                        |
| `ESX.UI.Menu.RegisterType`   | void    | type, open, close                        |
| `ESX.UI.Menu.Open`   | Menu    | type, namespace, name, data, submit, cancel, change, close                        |
| `ESX.UI.Menu.Close`   | void    | type, namespace, name                        |
| `ESX.UI.Menu.CloseAll`   | void    |                         |
| `ESX.UI.Menu.GetOpened`   | Menu    | type, namespace, name                        |
| `ESX.UI.Menu.GetOpenedMenus`   | [Menu]    |                         |
| `ESX.UI.Menu.IsOpen`   | bool    | type, namespace, name                        |
| `ESX.UI.Menu.IsAnyOpened`   | bool    |                         |
| `ESX.UI.Menu.IsAnyNamespacedOpen`   | bool    | namespace                        |
| `ESX.NUI.SetNUIActive`   | void    | resourceName, hasFocus, hasCursor                        |
| `ESX.NUI.IsAnyNUIOpen`   | bool    | resourceNameToAvoid, withCursorOnly                        |
| `ESX.UI.Menu.ChoosePlayersInArea`   | void    | areaRange, cb, onlyReacheablePlayers, menuTitle                        |
| `ESX.UI.Menu.ChoosePlayersNearbyPos`   | void    | coords, areaRange, cb, onlyReacheablePlayers, menuTitle                        |
| `ESX.UI.Menu.OpenYesNoDialog`   | void    | title, question, submitCb, denyCb, canGoOverNUIs                        |
| `ESX.UI.Menu.GetItemLabelWithExtraData`   | string    | itemData                        |
| `ESX.UI.Menu.GetValidItemAmmoTypeData`   | json, number    | itemData                        |
| `ESX.UI.ShowInventoryItemNotification`   | void    | add, itemData, count                        |
| `ESX.UI.ShowCashNotification`   | void    | add, accountData, symbol, money                        |
| `ESX.UI.ShowWeaponItemNotification`   | void    | add, weaponData, count                        |
| `ESX.GetSocietyIntByName`   | number    | society                        |
| `ESX.GetSocietyNameByInt`   | string    | societyId                        |
| `ESX.GetSocietyLabelText`   | string    | societyInt                        |
| `ESX.GetInventoryItemCount`   | number    | itemName                        |
| `ESX.Game.Utils.DrawText3D`   | void    | coords, text, size                        |
| `ESX.Camera.CreateTalkingCamera`   | [Camera]    | entity, camHeightOffset                        |
| `ESX.Camera.DeleteTalkingCamera`   | void    | cam                        |
| `ESX.Admin.GetGroup`   | string    |                         |

# Funções disponíveis no Clientside através de **tick_functions.lua**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX_ShowLoadingPrompt`    | void  | msg, type                        |
| `ESX_HideLoadingPrompt`    | void  |                                  |
| `ESX_RequestNetworkControlOfEntity`  | void  | entity, showHelp, timeoutDuration |
| `ESX_IsCurrentSessionValid`      | bool     |              |
| `ESX_GetNetIdFromEntity`   | number    | entity          |
| `ESX_GetVehicleFromNetId`   | Vehicle    | netId                        |
| `ESX_GetObjectFromNetId`   | Object    | netId                        |
| `ESX_GetPedFromNetId`   | Ped    | netId                        |
| `ESX_IsPedUsingFreemodeSkin`   | bool    | ped                        |
| `ESX_DisplayHelpText`   | void    | str, loop, duration                        |
| `ESX_DisplayLongHelpText`   | void    | str, loop, duration, beep, canBeQueued                        |
| `ESX_DisplayLongHelpTextThisFrame`   | void    | str                        |
| `ESX_DisplayMissionText`   | void    | text, time, drawNow                        |
| `ESX_DisplayLongMissionText`   | void    | text, time, drawNow                        |
| `ESX_ShowNotification`   | void    | msg, data                        |
| `ESX_ShowAdvancedNotification`   | void    | title, subject, msg, icon, iconType, data                        |
| `ESX_GetDistanceBetweenHeadings`   | number    | headingA, headingB                        |
| `ESX_GetHeadingBetweenCoords`   | number    | coordA, coordB, iParam6                        |
| `ESX_IsEntityFacingDirection`   | bool    | entity, heading, distanceAmount                        |
| `ESX_SlideEntityCoordsAndHeadingThisFrame`    | void  | entity, newPos, newHeading, posSpeedAxis, headingSpeed, forceNoOffset                        |
| `ESX_IsEntityAtCoord`    | bool  | entity, x, y, z, xRange, yRange, zRange                        |
| `ESX_GetPedMugshot`   | Handle    | ped, useTransparentBg                        |
| `ESX_Teleport`   | void    | entity, coords, cb, keepPedVeh                        |
| `ESX_TeleportPlayer`   | bool    | playerPed, coords, range, keepPedVeh                        |
| `ESX_StartLoadScene`   | bool    | coords, range, duration, useFocusArea                        |
| `ESX_StartAsyncLoadScene`   | void    | cb, coords, range, duration, useFocusArea                        |
| `ESX_DeleteVehicle`   | void    | vehicle                        |
| `ESX_DeleteObject`   | void    | object                        |
| `ESX_DeletePed`   | void    | ped                        |
| `ESX_DeleteAttachedEntitiesToEntity`    | void  | entity                        |
| `ESX_GetClosestPlayer`   | ID    | coords, canGetLocalPlayerPed                        |
| `ESX_GetPlayersInArea`   | [ID]    | coords, area, returnServerIds                        |
| `ESX_GetClosestVehicle`   | Vehicle    | coords                        |
| `ESX_GetVehicleInDirection`    | Vehicle  | range, checkMapHit, checkObjectHit                        |
| `ESX_GetVehicleInDirectionOfEntity`    | Vehicle  | entity, range, zOffset, checkMapHit, checkObjectHit                        |
| `ESX_CreateVehicleDistControllerThread`    | void  | vehNetId, onEntityLostCb                        |
| `ESX_GetVehicleProperties`    | json  | vehicle, useMinification                        |
| `ESX_SetVehicleProperties`    | void  | vehicle, props                        |
| `ESX_GetVehicleExtraDamageProperties`    | json  | vehicle                        |
| `ESX_SetVehicleExtraDamageProperties`    | void  | vehicle, data                        |
| `ESX_ResetWheelsPairByDecor`   | void    | veh, type, pairId                        |
| `ESX_ResetVehicleSuspensionHeightByDecor`   | void    | veh                        |
| `ESX_ResetVehicleSuspensionBiasByDecor`   | void    | veh                        |
| `ESX_ResetVehicleTractionBiasByDecor`   | void    | veh                        |
| `ESX_IsThisVehicleAPlayerVehicle`    | bool  | vehicle                        |
| `ESX_IsThisVehicleAPersonalVehicleFromThisPlayer`    | bool  | vehicle, accountId                        |
| `ESX_GetPersonalVehicleOwnerAccountId`    | ID  | vehicle                        |
| `ESX_IsSpawnPointClear`   | bool    | coords, radius, noVehsCheck, noObjsCheck, noPedsCheck                        |
| `ESX_GetPlayersInVehicle`    | void  | vehicle, canIncludeLocalPlayer                        |
| `ESX_GetPedsInVehicle`    | [Ped]  | vehicle, pedToExclude                        |
| `ESX_GetPedVehicleSeat`    | Ped  | ped, vehicle                        |
| `ESX_GetDistanceBetweenCoords`    | void  | coordsA, coordsB, useZ                        |
| `ESX_GetValueAdaptedToHigherFramesPerSecond`    | void  | value, currentFPS                        |
| `ESX_SetNUIFocus`   | void    | resourceName, hasFocus, hasCursor                        |
| `ESX_DrawText3D`   | void    | coords, text, size                        |
| `ESX_SetBlipName`    | void  | blip, name                        |
| `ESX_RemoveBlip`    | void  | blip                        |
| `ESX_CreateInstructionalButtonsScaleform`    | void  |                         |
| `ESX_WaitUntilInstructionalButtonsScaleformAreLoaded`    | void  |                         |
| `ESX_ReleaseInstructionalButtonsScaleform`    | void  |                         |
| `ESX_DrawInstructionalButtonsScaleformThisFrame`    | void  |                         |
| `ESX_BeginInstructionalButtonsScaleformDrawerThread`    | void  |                         |
| `ESX_IsInstructionalButtonsScaleformReady`    | bool  |                         |
| `ESX_SetInstructionalButtonsList`    | void  | list, drawNow                        |
| `ESX_ClearInstructionalButtonsList`    | void  | drawNow                        |
| `ESX_RefreshInstructionalButtonsList`    | void  |                         |
| `ESX_RegisterKeyMapping`    | void  | commandName, description, defaultMapper, defaultParameter, onPressCb, onReleaseCb, onDisabledPressCb, onDisabledReleaseCb, similarNativeKeyId                        |
| `ESX_IsAllControlsDisabled`    | bool  |                         |
| `ESX_RegisterCommand`    | void  | commandName, handler, restricted, description, paramsDescs                        |
| `ESX_RegisterCommandSuggestionOnly`    | void  | commandName, description, paramsDescs                        |
| `ESX_StartSynchronisedSceneController`    | void  | netScene, onTickStartFunc, onTickEndFunc, onSceneDestroyedFunc, onSceneLastFrameFunc, overrideLastFramePhase                        |
| `ESX_AdvancedDecorGetValue`    | dynamic  | entity, entryName, entryType                        |
| `ESX_AdvancedDecorSetValue`    | void  | entity, entryName, entryValue, extraData                        |
| `ESX_StateBagExistOn`    | bool  | entity, name                        |
| `ESX_StateBagGetValue`    | dynamic  | entity, name                        |
| `ESX_StateBagSetValue`    | void  | entity, name, value, canReplicate                        |
| `ESX_RefreshVehicleStateBagsFromPropsDecors`    | void  | veh                        |