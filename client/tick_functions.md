# Funções disponíveis no Clientside através de **tick_functions.lua**
O arquivo pode ser utilizado importando no fxmanifest.lua: `@es_extended/client/tick_functions.lua`

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `ESX_ShowLoadingPrompt`    | void  | msg, type                        | Habilita o indicador de carregamento do GTA com uma mensagem.
| `ESX_HideLoadingPrompt`    | void  |                                  | Esconde o indicador de carregamento do GTA.
| `ESX_RequestNetworkControlOfEntity`  | void  | entity, showHelp, timeoutDuration |
| `ESX_IsCurrentSessionValid`      | bool     |              | OBSOLETO: Retorna se a sessão atual é válida.
| `ESX_GetNetIdFromEntity`   | number    | entity          | Retorna o NetId atribuído a uma Entity.
| `ESX_GetVehicleFromNetId`   | Vehicle    | netId                        | Retorna o Vehicle atribuído ao NetId.
| `ESX_GetObjectFromNetId`   | Object    | netId                        | Retorna o Object atribuído ao NetId.
| `ESX_GetPedFromNetId`   | Ped    | netId                        | Retorna o Ped atribuído ao NetId.
| `ESX_IsPedUsingFreemodeSkin`   | bool    | ped                        | Retorna se o Ped está utilizando um modelo de personagem do GTA:Online (`mp_m_freemode_01` e `mp_f_freemode_01`).
| `ESX_DisplayHelpText`   | void    | str, loop, duration                        |
| `ESX_DisplayLongHelpText`   | void    | str, loop, duration, beep, canBeQueued                        |
| `ESX_DisplayLongHelpTextThisFrame`   | void    | str                        |
| `ESX_DisplayMissionText`   | void    | text, time, drawNow                        |
| `ESX_DisplayLongMissionText`   | void    | text, time, drawNow                        |
| `ESX_ShowNotification`   | void    | msg, data                        | Emite uma notificação no jogo utilizando a interface do GTA.
| `ESX_ShowAdvancedNotification`   | void    | title, subject, msg, icon, iconType, data                        | Emite uma notificação no jogo utilizando a interface do GTA.
| `ESX_GetDistanceBetweenHeadings`   | number    | headingA, headingB                        |
| `ESX_GetHeadingBetweenCoords`   | number    | coordA, coordB, iParam6                        |
| `ESX_IsEntityFacingDirection`   | bool    | entity, heading, distanceAmount                        |
| `ESX_IsEntityAtCoord`    | bool  | entity, x, y, z, xRange, yRange, zRange                        |
| `ESX_SlideEntityCoordsAndHeadingThisFrame`    | void  | entity, newPos, newHeading, posSpeedAxis, headingSpeed, forceNoOffset                        |
| `ESX_GetPedMugshot`   | Handle    | ped, useTransparentBg                        |
| `ESX_Teleport`   | void    | entity, coords, cb, keepPedVeh                        |
| `ESX_TeleportPlayer`   | bool    | playerPed, coords, range, keepPedVeh                        |
| `ESX_StartLoadScene`   | bool    | coords, range, duration, useFocusArea                        |
| `ESX_StartAsyncLoadScene`   | void    | cb, coords, range, duration, useFocusArea                        |
| `ESX_DeleteVehicle`   | void    | vehicle                        | Deleta um Vehicle.
| `ESX_DeleteObject`   | void    | object                        | Deleta um Object.
| `ESX_DeletePed`   | void    | ped                        | Deleta um Ped.
| `ESX_DeleteAttachedEntitiesToEntity`    | void  | entity                        |
| `ESX_GetClosestPlayer`   | Player, number    | coords, canGetLocalPlayerPed                        | Retorna o Player mais próximo e a distância dele. Retornará -1 caso nenhum jogador seja encontrado.
| `ESX_GetPlayersInArea`   | [Player]    | coords, area, returnServerIds                        |
| `ESX_GetClosestVehicle`   | Vehicle    | coords                        |
| `ESX_GetVehicleInDirection`    | Vehicle  | range, checkMapHit, checkObjectHit                        |
| `ESX_GetVehicleInDirectionOfEntity`    | Vehicle  | entity, range, zOffset, checkMapHit, checkObjectHit                        |
| `ESX_CreateVehicleDistControllerThread`    | void  | vehNetId, onEntityLostCb                        |
| `ESX_GetVehicleProperties`    | json  | vehicle, useMinification                        | Retorna as propriedades de personalização de um veículo.
| `ESX_SetVehicleProperties`    | void  | vehicle, props                        | Define as propriedades de personalização de um veículo.
| `ESX_GetVehicleExtraDamageProperties`    | json  | vehicle                        | Retorna as propriedades de danos físicos de um veículo.
| `ESX_SetVehicleExtraDamageProperties`    | void  | vehicle, data                        | Define as propriedades de danos físicos de um veículo.
| `ESX_ResetVehicleWheelsPairByDecor`   | void    | veh, type, pairId                        | Reseta as informações customizadas por Decorator de WheelsPair do veículo.
| `ESX_ResetVehicleSuspensionHeightByDecor`   | void    | veh                        | Reseta as informações customizadas por Decorator de SuspensionHeight do veículo.
| `ESX_ResetVehicleSuspensionBiasByDecor`   | void    | veh                        | Reseta as informações customizadas por Decorator de SuspensionBias do veículo.
| `ESX_ResetVehicleTractionBiasByDecor`   | void    | veh                        | Reseta as informações customizadas por Decorator de TractionBias do veículo.
| `ESX_IsThisVehicleAPlayerVehicle`    | bool  | vehicle                        | Retorna se o Vehicle pertence a um jogador.
| `ESX_IsThisVehicleAPersonalVehicleFromThisPlayer`    | bool  | vehicle, accountId                        | Retorna se o Vehicle possui como dono `accountId` (ID da conta do jogador).
| `ESX_GetPersonalVehicleOwnerAccountId`    | ACCOUNT_ID  | vehicle                        | Retorna o ID da conta do dono de um Vehicle.
| `ESX_RefreshVehicleStateBagsFromPropsDecors`    | void  | veh                        | Replica todos os Decorators de um Vehicle utilizando StateBags.
| `ESX_IsSpawnPointClear`   | bool    | coords, radius, noVehsCheck, noObjsCheck, noPedsCheck                        | Retorna se uma coordenada está disponível para ser usada como Ponto de Spawn.
| `ESX_GetPlayersInVehicle`    | [Player]  | vehicle, canIncludeLocalPlayer                        | Retorna uma lista de ID de jogadores que estão dentro de um Vehicle.
| `ESX_GetPedsInVehicle`    | [Ped]  | vehicle, pedToExclude                        | Retorna uma lista de Peds que estão dentro de um Vehicle.
| `ESX_GetPedVehicleSeat`    | number  | ped, vehicle                        | Retorna o assento atual que um Ped está ocupando em um Vehicle. Retornará -2 caso o Ped não esteja ocupando um assento no veículo.
| `ESX_GetDistanceBetweenCoords`    | number  | coordsA, coordsB, useZ                        | Calcula e retorna a distância entre 2 coordenadas.
| `ESX_GetValueAdaptedToHigherFramesPerSecond`    | number  | value, currentFPS                        | Retorna o valor informado, porém reajustado baseado na taxa de FPS informado.
| `ESX_SetNUIFocus`   | void    | resourceName, hasFocus, hasCursor                        |
| `ESX_DrawText3D`   | void    | coords, text, size                        |
| `ESX_CalculateBestTickPacingByDistance`     | number | distance          |
| `ESX_SetBlipName`    | void  | blip, name                        | Define o nome de um Blip.
| `ESX_RemoveBlip`    | void  | blip                        | Deleta um Blip.
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
| `ESX_IsAllControlsDisabled`    | bool  |                         | Retorna se todos os controles estão desabilitados.
| `ESX_RegisterCommand`    | void  | commandName, handler, restricted, description, paramsDescs                        |
| `ESX_RegisterCommandSuggestionOnly`    | void  | commandName, description, paramsDescs                        |
| `ESX_StartSynchronisedSceneController`    | void  | netScene, onTickStartFunc, onTickEndFunc, onSceneDestroyedFunc, onSceneLastFrameFunc, overrideLastFramePhase                        |
| `ESX_AdvancedDecorGetValue`    | dynamic  | entity, entryName, entryType                        |
| `ESX_AdvancedDecorSetValue`    | void  | entity, entryName, entryValue, extraData                        | Define um valor para Decorator e StateBag também.
| `ESX_StateBagExistOn`    | bool  | entity, name                        |
| `ESX_StateBagGetValue`    | dynamic  | entity, name                        |
| `ESX_StateBagSetValue`    | void  | entity, name, value, canReplicate                        |