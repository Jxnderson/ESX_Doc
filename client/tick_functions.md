# Funções disponíveis no Clientside através de **tick_functions.lua**
O arquivo pode ser utilizado importando no fxmanifest.lua: `@es_extended/client/tick_functions.lua`

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