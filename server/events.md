# Funções disponíveis no Serverside através de **AddEventHandler** ou **RegisterNetEvent**

| Função     | Parâmetros                                     | NetEvent  | Descrição                                     |
|------------|------------------------------------------------|-----------|------------------------------------------------
| `es:addGroup`                 | group, inherit, aceGroup       | false |
| `es:canGroupTarget`           | group, targetGroup, cb         | false |
| `es:getAllGroups`             | cb                             | false |
| `es:addCommand`               | command, callback, suggestion, arguments                     | false |
| `es:addGroupCommand`          | command, group, callback, callbackfailed, suggestion, arguments       | false |
| `es:addAdvancedCommand`       | commandData, callback, callbackfailed, suggestion, arguments          | false |
| `esx:playerLoaded`            | source, xPlayer, isNewAccount  | false |
| `esx:playerDropped`           | source, xPlayer                | false |
| `esx:netEntityRemoved`        | netId                          | false |
| `esx:setCleanupState`         | name, state                    | false |
| `esx:randomizeEventBoosters`  |                      | false |
| `esx:deleteAllEventBoosters`  |                      | false |
| `esx:reloadAllEventBoosters`  |                      | false |
| `esx:onAddInventoryItem`      | source, itemData, itemCount                        | false |
| `esx:onRemoveInventoryItem`   | source, itemIndex, itemData, itemCount             | false |
| `esx:onAddBagItem`            | source, bagData                                    | false |
| `esx:onRemoveBagItem`         | source, bagData                                    | false |
| `esx:setJob`                  | source, jobData, lastJobData                       | false |
| `esx:createQuestion`          | source, target, title, sendMsg, duration, acceptCb, rejectCb, failCb, canSendMultipleQuestions  | false |
| `esx:giveRankXPToPlayer`      | source, jobName, xpCount                        | false |
| `esx:giveAchievementToPlayer` | source, achievementName, count                  | false |
| `esx:givePlayerDonateBonuses` | xPlayer, donationId, days, canOverrideActiveDonations     | false |
| `esx:incomingShopDonation`    | cb, accountId, idDonates, overrideMaxDaysDuration         | false |
| `esx:incomingHouseDonation`   | model                 | false |
| `esx:incomingYachtDonation`   | cb, accountId         | false |
| `esx:incomingRoleDonation`    | cb, accountId         | false |
| `esx:incomingVehPlateChangeVoucher`   | cb, accountId         | false |
| `esx:incomingPhoneNumberChangeVoucher`   | cb, accountId         | false |
| `esx:incomingWarehouseEquipsUpgradeVoucher`   | cb, accountId         | false |
| `esx:incomingWarehouseLocationChangeVoucher`  | cb, accountId         | false |
| `esx:incomingCarDonation`     | cb, accountId, vehModelName, overrideMaxDaysDuration         | false |
| `esx:incomingHouseDonation`   | cb, accountId, propertyName, overrideMaxDaysDuration         | false |
| `esx:incomingBoatDonation`    | cb, accountId, vehModelName         | false |
| `esx:incomingTwitterAccountVerifyDonation`   | cb, accountId         | false |
| `esx:incomingInstagramAccountVerifyDonation` | cb, accountId         | false |
| `esx:incomingTinderAccountVerifyDonation`    | cb, accountId         | false |
| `esx:incomingOnlyFansAccountVerifyDonation`  | cb, accountId         | false |