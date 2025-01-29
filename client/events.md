# Eventos disponíveis no Clientside através de **AddEventHandler** ou **RegisterNetEvent**

| Função     | Parâmetros                                     | NetEvent  | Descrição                                     |
|------------|------------------------------------------------|-----------|------------------------------------------------
| `esx:onNUINotificationDisplay`       | type, duration               | false | É disparado quando uma notificação NUI é criada pela framework.
| `esx:onTalkingCamerasStateChange`    | state                        | false | É disparado quando uma Talking Camera é criada ou desativada.
| `esx:drawBasicBlips`                 |                              | false | É disparado uma vez quando a framework está pronta para criar Blips.
| `esx:onPlayerDeath`                  | killerId                     | false | É disparado quando o jogador morre.
| `esx:onWaypointTeleport`             | position                     | false | É disparado quando o jogador utiliza o comando de teleport por waypoint.
| `esx:hasPauseMenuToggled`            | state                        | false | É disparado quando o jogador abre o menu de pause.
| `esx:onJobActionsControlPressed`     | state                        | false | É disparado quando o jogador pressiona a tecla pra abrir o menu do emprego atual.
| `esx:onGameZoneEnter`                | zoneName, gridId, camGridId  | false |
| `esx:isRankupHudComponentActive`     | state                        | false | É disparado quando a HUD de progredir de rank está ativa.
| `esx:onPrintDisplay`                 | message, time, drawNow       | false | É disparado quando uma notificação Print é criada pela framework.
| `esx:onShowNotification`             | message                      | false | É disparado quando uma notificação do GTA:Online é criada pela framework.
| `esx:onInstructionButtonsScaleformDrawThreadToggle` | state         | false | É disparado quando a interface de dicas de teclas pressionáveis for ativada/desativada.
| `esx:openInventoryCategory` | isKeyPressRequired         | false |
| `esx:spawnPed`              | model         | true | Spawn um Ped através do nome do modelo, ou da numeração do modelo.
| `esx:deleteVehicle`         |          | true | Deleta o Vehicle que estiver na frente do jogador.
| `esx:deleteVehicle2`        |          | true | Identifica o Vehicle em frente ao jogador, e solicita ao servidor para que delete-o utilizando OneSync.
| `esx:setWantedLevelControlByAnotherScript`        | state          | false | Informa a framework que outro script precisa controlar o Nível de Procurado.
| `esx:toogleCopsChase`          | state          | true | É disparado quando o /pmnabota é ativado ou desativado pelo servidor.
| `esx:peacefulToogle`           | state          | false | Inform a framework que outro script quer que a framework ative/desative o modo pacífico.
| `es:disablePvpTemp`            | state          | false |
| `esx:getMyAchievements`        | cb         | false | Retorna uma lista com todas as conquistas do jogador.
| `esx:getPlayerJobRankLevel`        | cb, rankName         | false | Retorna o nível do jogador em um rank específico.