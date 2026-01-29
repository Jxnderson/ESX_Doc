# Funções disponíveis no Serverside através da "classe" **xPlayer**

| Função     | Retorno | Parâmetros                                     | Descrição                                     |
|------------|---------|------------------------------------------------|------------------------------------------------
| `getIsBeingDropped`    | bool  |                         | Retorna se o jogador está em processo de saída do jogo.
| `setAsBeingDropped`    | void  |                        | Seta o estado do jogador como `em processo de saída do jogo`.
| `getCanDropItemsOnDisconnection`    | bool  |                        | Retorna se o jogador deve dropar itens numa sacola ao desconectar do jogo.
| `setDropItemsOnDisconnection`    | void  | state, index, periodDuration                       | Define se o jogador deverá dropar seus itens numa sacola ao desconectar do jogo.
| `setVolatilData`    | void  | entryName, value, avoidDatabaseUpdate, avoidClientsideUpdate                       |
| `getVolatilData`    | dynamic  | entryName                       |
| `canGroupTarget`    | bool  | groupName                       |
| `canExecuteCommand` | bool  | commandName                     | Retorna se o jogador tem permissões para executar determinado comando (só funciona com comandos criados pelos eventos da framework).
| `setMoney`    | void  | money                       | Define a quantia atual de dinheiro em mãos.
| `getMoney`    | number  |                        | Retorna a quantia atual de dinheiro em mãos.
| `getBank`    | number  |                        | Retorna a quantia atual de dinheiro no banco.
| `getPedCoords`    | vector3  |                        | Retorna a coordenada atual baseada no OneSync.
| `getLastPosition`    | dynamic  |                        | Retorna a última coordenada setada no Banco de dados.
| `isNearToCoords`    | bool  | coords, range, useZ                       | Retorna se está próximo de uma coordenada.
| `kick`    | void  | reasonLabel                       |
| `addMoney`    | void  | money, noSFX                       | Adiciona uma quantia de dinheiro em mãos.
| `removeMoney`    | void  | money, noSFX                       | Remove uma quantia de dinheiro em mãos.
| `getPermissions`    | dynamic  |                        |
| `setPermissions`    | void  | permissionName, replicateToDatabase                       |
| `setGroup`    | void  | groupName, replicateToDatabase                       | Define o grupo atual do jogador.
| `getGroup`    | string  |                        | Retorna o grupo atual do jogador.
| `getRoles`    | [dynamic]  |                        | Retorna uma lista de objetos {name, endAt} de todas as roles ativas do jogador.
| `giveRole`    | void  | role, daysDuration                       | Garante uma permissão específica pro jogador por um período determinado. Caso seja uma permissão permanente, use daysDuration = -1.
| `removeRole`    | void  | role                       | Remove uma permissão específica do jogador.
| `removeAllRoles`    | void  |                        | Remove todas as permissões do jogador.
| `hasRole`    | bool  | role                       | Retorna se o jogador tem uma determinada permissão em vigor.
| `set`    | void  | key, value                       |
| `get`    | dynamic  | key                       |
| `getAccountsData`   | [dynamic]  |                        | Retorna uma lista de objetos {id, name, label, money} de todas as contas de dinheiro do jogador. Use esta função caso pretenda enviar a lista para o cliente.
| `getAccounts`       | [dynamic]  |                        | Retorna uma lista de objetos complexos de todas as contas de dinheiro do jogador.
| `getInventory`    | [dynamic]  |                        |
| `getBags`    | [dynamic]  |                        |
| `getJob`    | dynamic  |                        |
| `getLoadout`    | [dynamic]  |                        |
| `getName`    | string  |                        | Retorna o nome do perfil da Steam/EGS/R* ou do PC do jogador.
| `getCharacterName`    | string  | canCallFallback                       | Retorna o nome do personagem atual em uso. Caso não seja encontrado e o parâmetro `canCallFallback` seja true, o nome do perfil do jogador será usado.
| `getAccount`    | dynamic  | accountName                       | Retorna uma conta de dinheiro pelo nome dela.
| `getAccountWithIndex`    | number, dynamic  | accountName                       | Retorna o índice e o objeto de uma conta de dinheiro pelo nome dela.
| `getAccountByIndex`    | dynamic  | index, accountName                       | Retorna uma conta de dinheiro pelo nome dela e pelo índice também.
| `createAccount`    | dynamic  | accountName, money                       | Tenta criar uma conta de dinheiro. Caso não consiga, retornará um objeto NULO.
| `getAccountMoney`    | number  | accountName                             | Retorna o tanto de dinheiro existente em uma conta de dinheiro. Retornará 0 se não encontrar a conta.
| `getAccountMoneyByIndex`    | number  | index, accountName               | Retorna o índice e o tanto de dinheiro existente em uma conta de dinheiro. Retornará -1 e 0 se não encontrar a conta.
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
| `refreshBagWeight`    | void  | withoutClientEvent        | Recalcula e atualiza o peso máximo atual do inventário do jogador.
| `getWeight`    | number  |                        | Retorna o peso atual do inventário.
| `refreshWeight`    | void  |                        | Recalcula e atualiza o peso atual do inventário do jogador.
| `canCarryItem`    | bool  | name, count, extraData, itemsToIgnoreWeightCalc                       | Retorna se o jogador tem espaço suficiente no inventário para carregar determinado item.
| `setMaxWeight`    | void  | newWeight                       |
| `setJob`    | void  | name, grade, extraData                       |
| `setJobExtraData`    | void  | extraData                       |
| `addWeapon`       | dynamic  | weaponName, ammo, tint, components, creationTime                       |
| `removeWeapon`    | void  | weaponName                       |
| `removeWeaponByIndex`    | void  | weaponIndex, weaponName                       |
| `removeWeaponsConditioned`    | void  | conditionFunc                       |
| `removeWeaponAmmoAsItem`    | void  | weaponName                       |
| `removeAllWeapons`    | void  |                        |
| `getWeapon`    | dynamic  | weaponName                       |
| `getWeaponWithIndex`    | number, dynamic  | weaponName                       |
| `setWeaponTint`    | void  | weaponName, tintIndex                       |
| `addWeaponComponent`    | void  | weaponName, componentHash                       |
| `addWeaponComponentFromModelData`    | void  | weaponName, componentModelData               |
| `getWeaponComponentIndex`            | number  | weaponName, componentHash                     |
| `getWeaponComponentIndexByData`      | number  | weaponData, componentHash                     |
| `removeWeaponComponent`              | bool  | weaponName, componentHash                       |
| `removeWeaponComponentByIndex`       | bool  | weaponData, componentIndex, componentHash       |
| `removeAllTintComponentsFromWeapon`  | void  | weaponData                                      |
| `addTempWeapon`    | dynamic  | weaponName, ammo, tint, components                       |
| `removeTempWeapon`    | void  | weaponName                       |
| `removeTempWeaponByIndex`    | void  | weaponIndex, weaponName                       |
| `getTempWeapon`    | dynamic  | weaponName                       |
| `getTempWeaponWithIndex`    | number, dynamic  | weaponName                       |
| `hasAchievement`    | bool  | achievementName                       | Retorna se o jogador possui uma conquista.
| `giveAchievement`   | void  | achievementName, progressCount        | Adiciona progresso a uma conquista.
| `getRankLevel`    | number  | rankName                            | Retorna o nível atual em um rank.
| `giveRankXP`    | void  | rankName, xpCount                       | Adiciona XP a um rank.
| `getAccountBonuses`                | {string: dynamic}  | | Retorna a lista de bonificações de conta que estão salvas em cache. A lista é indexada pelo tipo das bonificações.
| `getActiveAccountBonuses`          | {string: dynamic}  | Retorna somente a lista de bonificações de conta que estão ATIVAS. A lista é indexada pelo tipo das bonificações.
| `getActiveAccountBonusesByType`    |  [dynamic]  | targetBonusType | Retorna somente a lista de bonificações de conta que estão ATIVAS de determinado tipo.
| `giveAccountBonus`    | void  | bonusType, label, value, durationInDays, originatedFromName | Dá ao jogador uma bonificação de conta de determinado tipo, com um período específico definido e outros detalhes.
| `triggerEvent`    | void  | eventName, ...                        | Dispara um evento (igual `TriggerClientEvent`)
| `showNotification`    | void  | msg, data                         | Envia uma notificação simples do GTA:Online ao jogador.
| `showAdvancedNotification`    | void  | title, subtitle, msg, photo, icon, extraData                       | Envia uma notificação complexa do GTA:Online ao jogador.
| `showNUINotification`    | void  | msg, data                       | Envia uma notificação usando a interface da framework ao jogador.
| `showHelpText`    | void  | msg, duration, beep, canBeQueued       | Envia uma dica simples do GTA:Online ao jogador.
| `showBankNotification`    | void  | subtitle, msg, icon                       | Envia uma notificação simples do GTA:Online como sendo o remetente o Banco ao jogador.
| `showPhoneNotification`    | void  | appName, subtitle, message, supressSFX, suppressOnPrecaryPhones      | Envia uma notificação de um aplicativo ao telefone do jogador.
| `createProgressbar`    | Handle  | text, duration, color                       | Cria uma barra de progresso.
| `cancelProgressbar`    | void  | id                       | Cancela uma barra de progresso pelo ID.
| `getAssignedBankData`    | string, string  |                        | Retorna o nome do banco e o nome do ícone de notificação do banco do jogador.
| `isInThisPublicInstance`    | bool         | name | Retorna se o jogador está dentro de uma instância pública específica.
| `isPlayerInSameWorldOrInstance` | bool     | xTarget | Retorna se os jogadores estão na mesma instância. Retornará TRUE caso ambos não estejam instanciados.
| `isPlayerInSameInstance`    | bool         | xTarget | Retorna se o jogador está na mesma instância que outro jogador (xTarget). Retornará FALSO caso algum deles não esteja instanciado.