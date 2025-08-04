# Funções disponíveis no Serverside através de **AddEventHandler** ou **RegisterNetEvent**

| Função     | Parâmetros                                     | NetEvent  | Descrição                                     |
|------------|------------------------------------------------|-----------|------------------------------------------------
| `es:addGroup`                 | group, inherit, aceGroup       | false |
| `es:canGroupTarget`           | group, targetGroup, cb         | false |
| `es:getAllGroups`             | cb                             | false |
| `es:addCommand`               | command, callback, suggestion, arguments                     | false | Cria um comando sem qualquer restrição para acessá-lo.
| `es:addGroupCommand`          | command, group, callback, callbackfailed, suggestion, arguments       | false | Cria um comando que possui a restrição onde o jogador deve possuir ao menos determinado grupo de permissões.
| `es:addAdvancedCommand`       | commandData, callback, callbackfailed, suggestion, arguments          | false | Cria um comando que pode ter restrições avançadas. `commandData` aceita um JSON no formato: {name = 'comando', group = 'grupo', role = 'role'}. É possível permitir aos jogadores para terem acesso ao comando através de grupos e também de roles, ou somente de um dos 2, ou até mesmo não indicar restrição alguma e só informar o nome do comando.
| `esx:playerLoaded`            | source, xPlayer, isNewAccount  | false | É disparado pela framework quando o jogador seleciona ou cria o personagem na tela de seleção de identidades após o carregamento do jogo.
| `esx:playerDropped`           | source, xPlayer                | false | É disparado quando um jogador que já havia sido reconhecido pela framework desconecta.
| `esx:netEntityRemoved`        | netId                          | false | É disparado quando uma Entity reconhecida pelo servidor é deletada do jogo.
| `esx:setCleanupState`         | name, state                    | false |
| `esx:randomizeEventBoosters`  |                      | false |
| `esx:deleteAllEventBoosters`  |                      | false |
| `esx:reloadAllEventBoosters`  |                      | false |
| `esx:onAddInventoryItem`      | source, itemData, itemCount                        | false | É disparado quando um jogador recebe um item no inventário.
| `esx:onRemoveInventoryItem`   | source, itemIndex, itemData, itemCount             | false | É disparado quando um jogador remove ou perde um item do inventário.
| `esx:onAddBagItem`            | source, bagData                                    | false | É disparado quando um jogador recebe uma mochila.
| `esx:onRemoveBagItem`         | source, bagData                                    | false | É disparado quando um jogador remove ou perde uma mochila.
| `esx:setJob`                  | source, jobData, lastJobData                       | false |
| `esx:createQuestion`          | source, target, title, sendMsg, duration, acceptCb, rejectCb, failCb, canSendMultipleQuestions  | false | Cria uma interface de pergunta (F5/F6) para o jogador, possibilitando agirmos conforme a resposta dele (seja ele aceitando, recusando ou não respondendo).
| `esx:giveRankXPToPlayer`      | source, jobName, xpCount                        | false |
| `esx:giveAchievementToPlayer` | source, achievementName, count                  | false |
| `esx:givePlayerDonateBonuses` | xPlayer, donationId, days, canOverrideActiveDonations     | false |
| `esx:incomingShopDonation`    | cb, accountId, idDonates, overrideMaxDaysDuration         | false |
| `esx:incomingRoleDonation`    | cb, accountId, roleName, overrideMaxDaysDuration         | false |
| `esx:incomingYachtVoucher`                    | cb, accountId         | false |
| `esx:incomingVehPlateChangeVoucher`           | cb, accountId         | false |
| `esx:incomingPhoneNumberChangeVoucher`        | cb, accountId         | false |
| `esx:incomingWarehouseEquipsUpgradeVoucher`   | cb, accountId         | false |
| `esx:incomingWarehouseLocationChangeVoucher`  | cb, accountId         | false |
| `esx:incomingCarDonation`     | cb, accountId, vehModelName, overrideMaxDaysDuration         | false |
| `esx:incomingHouseDonation`   | cb, accountId, propertyName, overrideMaxDaysDuration         | false |
| `esx:incomingBoatDonation`    | cb, accountId, vehModelName         | false |
| `esx:incomingTwitterAccountVerifyDonation`   | cb, accountId         | false |
| `esx:incomingInstagramAccountVerifyDonation` | cb, accountId         | false |
| `esx:incomingTinderAccountVerifyDonation`    | cb, accountId         | false |
| `esx:incomingOnlyFansAccountVerifyDonation`  | cb, accountId         | false |
| `esx:incomingMoneyDonationGift`              | cb, accountId, accountName, moneyAmount         | false |