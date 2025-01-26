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

# Funções disponíveis no Serverside através da "classe" **xPlayer**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `getIsBeingDropped`    | bool  |                         |
| `setAsBeingDropped`    | void  |                        |
| `getCanDropItemsOnDisconnection`    | bool  |                        |
| `setDropItemsOnDisconnection`    | void  | state, index, periodDuration                       |
| `setVolatilData`    | void  | entryName, value, avoidDatabaseUpdate, avoidClientsideUpdate                       |
| `getVolatilData`    | dynamic  | entryName                       |
| `canGroupTarget`    | bool  | groupName                       |
| `setMoney`    | void  | money                       |
| `getMoney`    | number  |                        |
| `getBank`    | number  |                        |
| `getCoords`    | vector3  |                        |
| `getRealCoords`    | vector3  |                        |
| `isNearToCoords`    | bool  | coords, range, useZ                       |
| `kick`    | void  | reasonLabel                       |
| `addMoney`    | void  | money, noSFX                       |
| `removeMoney`    | void  | money, noSFX                       |
| `getPermissions`    | dynamic  |                        |
| `setPermissions`    | void  | permissionName, replicateToDatabase                       |
| `getIdentifier`    | string  |                        |
| `setGroup`    | void  | groupName, replicateToDatabase                       |
| `getGroup`    | string  |                        |
| `getRoles`    | [string]  |                        |
| `giveRole`    | void  | role, daysDuration                       |
| `removeRole`    | void  | role                       |
| `removeAllRoles`    | void  |                        |
| `hasRole`    | bool  | role                       |
| `set`    | void  | key, value                       |
| `get`    | dynamic  | key                       |
| `getPlayer`    | dynamic  |                        |
| `getRealAccounts`    | [dynamic]  |                        |
| `getAccount`    | dynamic  | accountName                       |
| `getAccountWithIndex`    | number, dynamic  | accountName                       |
| `getAccountByIndex`    | dynamic  | index, accountName                       |
| `getInventory`    | [dynamic]  |                        |
| `getBags`    | [dynamic]  |                        |
| `getJob`    | dynamic  |                        |
| `getLoadout`    | [dynamic]  |                        |
| `getName`    | string  |                        |
| `getLastPosition`    | dynamic  |                        |
| `getCharacterName`    | string  | canCallFallback                       |
| `createAccount`    | dynamic  | accountName, money                       |
| `setAccountMoney`    | void  | accountName, money, noSFX                       |
| `setAccountMoneyByIndex`    | void  | index, accountName, money, noSFX                       |
| `addAccountMoney`    | void  | accountName, money, noSFX                       |
| `addAccountMoneyByIndex`    | void  | index, accountName, money, noSFX                       |
| `removeAccountMoney`    | void  | accountName, money, noSFX                       |
| `removeAccountMoneyByIndex`    | void  | index, accountName, money, noSFX                       |
| `getInventoryItem`    | dynamic  | name                       |
| `getInventoryItemById`    | dynamic  | uid                       |
| `getInventoryItemHavingExtraData`    | dynamic  | name, extraData                       |
| `getInventoryItemByIndex`    | dynamic  | index, name                       |
| `getInventoryItemWithIndex`    | number, dynamic  | name                       |
| `getInventoryItemHavingExtraDataWithIndex`    | number,dynamic  | name, extraData                       |
| `getInventoryItemWithIndexById`    | number, dynamic  | objId                       |
| `createInventoryItem`    | void  | name, count, extraData, jumpWeightRefresh                       |
| `addInventoryItem`    | dynamic  | name, count, extraData, jumpWeightRefresh                       |
| `removeInventoryItem`    | void  | name, count, jumpWeightRefresh                       |
| `removeInventoryItemByIndex`    | void  | index, name, count, jumpWeightRefresh                       |
| `setInventoryItemByIndex`    | void  | index, name, count, jumpWeightRefresh                       |
| `setInventoryItemExtraDataByIndex`    | void  | index, name, extraData, canReplicate                       |
| `getBagItemByIndex`    | dynamic  | index, name                       |
| `getBagItem`    | dynamic  | name                       |
| `createBagItem`    | dynamic  | name                       |
| `addBagItem`    | dynamic  | name                       |
| `removeBagItemByIndex`    | void  | bagIndex, name                       |
| `removeBagItem`    | void  | name                       |
| `refreshBagWeight`    | void  | withoutClientEvent                       |
| `getWeight`    | number  |                        |
| `refreshWeight`    | void  |                        |
| `canCarryItem`    | bool  | name, count, extraData, itemsToIgnoreWeightCalc                       |
| `setMaxWeight`    | void  | newWeight                       |
| `setJob`    | void  | name, grade, extraData                       |
| `setJobExtraData`    | void  | extraData                       |
| `addWeapon`    | dynamic  | weaponName, ammo, tint, components, creationTime                       |
| `removeWeapon`    | void  | weaponName                       |
| `removeWeaponByIndex`    | void  | weaponIndex, weaponName                       |
| `removeWeaponsConditioned`    | void  | conditionFunc                       |
| `removeWeaponAmmoAsItem`    | void  | weaponName                       |
| `removeAllWeapons`    | void  |                        |
| `getWeapon`    | dynamic  | weaponName                       |
| `getWeaponWithIndex`    | number, dynamic  | weaponName                       |
| `setWeaponTint`    | void  | weaponName, tintIndex                       |
| `addWeaponComponent`    | dynamic  | weaponName, componentHash                       |
| `addWeaponComponentFromModelData`    | dynamic  | weaponName, modelData                       |
| `getWeaponComponent`    | dynamic  | weaponName, componentHash                       |
| `getWeaponComponentIndexFromHash`    | dynamic  | weaponData, componentHash                       |
| `removeWeaponComponent`    | void  | weaponName, componentHash                       |
| `addTempWeapon`    | dynamic  | weaponName, ammo, tint, components                       |
| `removeTempWeapon`    | void  | weaponName                       |
| `removeTempWeaponByIndex`    | void  | weaponIndex, weaponName                       |
| `getTempWeapon`    | dynamic  | weaponName                       |
| `getTempWeaponWithIndex`    | number, dynamic  | weaponName                       |
| `giveAchievement`    | void  | achievementName, count                       |
| `getRankLevel`    | number  | rankName                       |
| `giveRankXP`    | void  | rankName, xpCount                       |
| `triggerEvent`    | void  | eventName, ...                       |
| `showNotification`    | void  | msg, data                       |
| `showAdvancedNotification`    | void  | title, subtitle, msg, photo, icon, extraData                       |
| `showNUINotification`    | void  | msg, data                       |
| `showHelpText`    | void  | msg, duration, beep, canBeQueued                       |
| `showBankNotification`    | void  | subtitle, msg, icon                       |
| `showPhoneNotification`    | void  | appName, subtitle, message, supressSFX, suppressOnPrecaryPhones                       |
| `createProgressbar`    | Handle  | text, duration, color                       |
| `cancelProgressbar`    | void  | id                       |
| `getAssignedBankData`    | string, string  |                        |