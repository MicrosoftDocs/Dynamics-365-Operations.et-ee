---
title: Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine
description: See teema kirjeldab, kuidas määrata Warehouse Management mobiilirakenduses uute või kohandatud ülesandevoogude etapiikoonid ja pealkirjad.
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b8d663fa9743fae83654ed9938b4131e0fa08b9
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902168"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas määrata Warehouse Management mobiilirakenduses uute või kohandatud ülesandevoogude etapiikoonid ja pealkirjad.

Järgmised illustratsioonid näitavad, kuidas etapiikoonid ja pealkirjad kuvatakse Warehouse Management mobiilirakenduses.

![Warehouse Management mobiilirakenduse astmeikooni ja etapi pealkirja näide.](media/step-icon-example.png "Warehouse Management mobiilirakenduse astmeikooni ja etapi pealkirja näide")

## <a name="turn-on-this-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *uue laorakenduse kasutajasätted, ikoonid ja etapi pealkirjad*

## <a name="standard-step-ids-classes-and-icons"></a>Standardsammude ID-d, klassid ja ikoonid

Iga samm ülesande voos tuvastatakse etapi ID järgi ja igal sammu ID-l on vastav astmeklass. Sammu ikoon ja pealkiri määratakse igas astmeklassis.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Sammu ID-d ja etapiklassid

Järgmises tabelis loetletakse kõik praegu saadaolevad etapi ID-d ja see on vastav astmeklass. Peamise sisendvälja juhtelemendi nime kasutatakse astme ID-s.

Näide, mis näitab, kuidas nende sammude ID-sid ja klasse kasutatakse `WHSMobileAppStepInfoBuilder.stepId()` meetodi rakendamist [näites: määrake selles teemas hiljem etapiikoonid ja pealkirjad kohandatud voo](#example) selgitatakse selles teemas hiljem.

| Sammu ID | Samm klass |
|-|-|
| PartiiPositsioon | WhSMobileAppStepBatchDisposition |
| Vedaja | WhSMobileAppStepCarrier |
| Tegelikkaal | WhSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WhSMobileAppStepCatchWeight |
| Tegelikukaalusilt | WhSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WhSMobileAppStepCatchWeightTagWeight |
| ChangeWarekodaSuccess | WHSMobileAppStepChangeWarekodaSuccess |
| Kontrollnumber | WhSMobileAppStepCheckDigit |
| KlastedId | WhSMobileAppStepClusterId |
| ClusterPickQtyVerification | WhSMobileAppStepQtyVerification |
| Klastripositsioon | WHSMobileAppStepClusterPosition |
| KonfiguratsiooniId | WHSMobileAppStepConfigId |
| Kinnitus | WHSMobileAppStepConfirmation |
| KonsolideerimineLitsentseeritudPlaat | WhSMobileAppStepConsolidateFromLicensePlateId |
| KonsolideeritudLPCKinnitus | WHSMobileAppStepConsolidateLPConfirmation |
| KonsolideerimineLitsentseeritudPlaat | WhSMobileAppStepConsolidateToLicensePlateId |
| Konteineritüüp | WHSMobileAppStepContainerType |
| ArvestusePõhjusKood | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WhSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WhSMobileAppStepCycleCountQty |
| CycleCountQty2 | WhSMobileAppStepCycleCountQty |
| CycleCountQty3 | WhSMobileAppStepCycleCountQty |
| CycleCountQty4 | WhSMobileAppStepCycleCountQty |
| Likvideerimine | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| SõitjaVäljaregamiseId | WHSMobileAppStepDriverCheckOutId |
| Aegumiskuupäev | WhSMobileAppStepExpDate |
| PartiiLikvideerimine | WHSMobileAppStepFromBatchDisposition |
| VarudeOlek | WhSMobileAppStepInventoryStatusFrom |
| TäisKogus | WhSMobileAppStepFullQty |
| SissetuleOsa | WhSMobileAppStepInboundPut |
| InventariPartiiId | WhSMobileAppStepBatch |
| InventuuriVärviId | WhSMobileAppStepInventColorId |
| VarudeAsukoht | WHSMobileAppStepInventLocation |
| VarudeAsukohtId | WHSMobileAppStepWarehouse |
| InventSeeriaId | WHSMobileAppStepInventSerialId |
| VaruSuuruseId | WHSMobileAppStepInventSizeId |
| VaruSeisId | WHSMobileAppStepInventStatus |
| VaruStiilId | WHSMobileAppStepInventStyleId |
| VaruVersioonId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMSisuID | ITMMobileAppStepContainerId |
| ITMSaatmisID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanVõiKaardiId | WHSMobileAppStepKanbanCard |
| LitsentsPlateId | WhSMobileAppStepLicensePlate |
| KoormaId | WHSMobileAppStepLoadId |
| AsukohaLitsentsiPlaadiPaigutus | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPcheck | WHSMobileAppStepLocOrLPCheck |
| KohalikKinnitus | WHSMobileAppStepLocVerification |
| LPAdjustIn | WhSMobileAppStepLPAdjustIn |
| LPLapseKindelLP | WhSMobileAppStepLPBreakChildLP |
| LPVanemaKindelLP | WHSMobileAppStepLPBreakParentLP |
| LPEhitaLapsLP | WHSMobileAppStepLPBuildChildLP |
| LPEhitaVanemLP | WHSMobileAppStepLPBuildParentLP |
| LPKinnitus | WHSMobileAppStepLPVerification |
| ÜhendatudKontainerId | WHSMobileAppStepMergeContainerId |
| SeagtudJoonNum | WHSMobileAppStepMixedLPLineNum |
| MobiiliSeadePäringSõnumKogumisIdentId | WhSMobileAppStepSelectOrder |
| LiikumineKinnitusestLoobumine | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WhSMobileAppStepCatchWeight |
| UusPäring | WHSMobileAppStepNewQty |
| VäljaminevKaaluKontrolliSilt | WhSMobileAppStepCatchWeightTag |
| VäljaminevVäljund | WHSMobileAppStepOutboundPut |
| VäljaminevKaal | WhSMobileAppStepCatchWeight |
| KirjutaÜleUusAsukoht | WhSMobileAppStepOverridePutNewLocation |
| TükiPõhjalKinnitus | WhSMobileAppStepQtyVerification |
| PoReaNumber | WHSMobileAppStepPOLineNum |
| PONum | WHSMobileAppStepPONum |
| AmetikohtTäis | WHSMobileAppStepPositionFull |
| AmetikohtTäisPäring | WHSMobileAppStepPositionFullQty |
| Sisaldus | WHSMobileAppStepPotency |
| PrinteriNimi | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdViimanePlaatKinnitus | WhSMobileAppStepProdLastPalletConfirmation |
| TooteKinnitus | WHSMobileAppStepProductConfirmation |
| TootmisScrapKinnitus | WHSMobileAppStepProductionScrapConfirmation |
| Pane | WHSMobileAppStepPut |
| KogumiteKlaster | WHSMobileAppStepPutawayClusterId |
| Kogus | WHSMobileAppStepQty |
| KogusTäiendus | WHSMobileAppStepQtyAdjust |
| KogusLühike | WHSMobileAppStepQtyShort |
| KogusTarbima | WhSMobileAppStepQtyToConsume |
| KogusÜlesKorjama | WHSMobileAppStepQtyToPick |
| KogusVäljaMinev | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| KogusKinnitus | WhSMobileAppStepQtyVerification |
| KogusValgeSkänningPiir | WHSMobileAppStepQtyAdjust |
| Põhjusestring | WhSMobileAppStepReasonString |
| RecvAsukohaId | WHSMobileAppStepRecvLocationId |
| EemaldaContainerId | WHSMobileAppStepRemoveContainerId |
| UuestiprindiSildiKinnitus | WhSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| LühikeKorjePõhjus | WhSMobileAppStepShortPickReason |
| LühikeKinnitusVõiLP | WhSMobileAppStepSortConOrLP |
| LühikeLitsentsPlateId | WHSMobileAppStepSortLicensePlateId |
| LühikeAmetId | WHSMobileAppStepSortPositionId |
| SorteeriKinnitus | WHSMobileAppStepSortVerification |
| StartAsukohtId | WHSMobileAppStepStartLocationId |
| StartTooteTellimuseKinnitus | WhSMobileAppStepStartProdOrderConfirmation |
| EesmärkLitsentsPlateId | WHSMobileAppStepTargetLicensePlateId |
| ReaNumber | WHSMobileAppStepTOLineNum |
| Asukohta | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| Lattu | WHSMobileAppStepWarehouseTo |
| TranspordiVaruId | WhSMobileAppStepTransportLoadId |
| VooSildiId | WhSMobileAppStepWaveLabelId |
| LaineLblQty | WHSMobileAppStepWaveLblQty |
| Kaal | WHSMobileAppStepWeight |
| KaalToConsume | WHSMobileAppStepWeightToConsume |
| WhSAdjustmentType | WhSMobileAppStepWHSAdjustmentType |
| WhSReceivingException | WhSMobileAppStepWHSReceivingException |
| WhSWorkException | WHSMobileAppStepWHSWorkException |
| WhSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobiiliAppSammuAsukoht |
| Töö ID | WHSMobileAppStepWorkId |
| TööstIdLoobumine | WHSMobileAppStepWorkIdToCancel |
| TööLPIdPaneäraKlaster | WHSMobileAppStepWorkLPIdPutawayCluster |
| TööpoolId | WHSMobileAppStepWorkPoolId |
| TsooniId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Saadaolevad astmeikoonid

Süsteem hõlmab standardsete astmeikoonide kogumeid, mida saate kasutada ka kohandatud sammude puhul. Kohandatud astme ikoone ei saa praegu üles laadida. Seetõttu peate alati valima ühe standardsammikoonidest.

Järgmine tabel näitab kõiki praegu saadaolevaid standardseid astme ikoone ja selle nime.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Sammu ikoonist"><br>Teave</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Litsentsiplaadi või kaubasammide ikooni lisamine"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Partii likvideerimissamm"><br>PartiiPositsioon</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Vedaja astme ikoon"><br>Vedaja</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Tegeliku kaalu sildi etapi ikoon"><br>Tegelikukaalusilt</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Tegeliku kaalu sildi etapi ikoon"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Kontrollnumbri astme ikoon"><br>Kontrollnumber</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Sisse- või väljaregistreerimise ID-etapi ikoon"><br>Väljaregistreerimine (CheckInOutId)</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alamlitsentsiplaadi etapi ikoon"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klastri ID etapi ikoon"><br>KlastedId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klastri ID etapi ikoon"><br>Klastripositsioon</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigureeri ID etapi ikoon"><br>KonfiguratsiooniId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Konfigureeritud välja etapi ikoon"><br>Konfigureeritud väli</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con või LP etapi ikoon"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolideeri litsentsiplaadi ID etapi ikoonilt"><br>KonsolideerimineLitsentseeritudPlaatID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolideeri litsentsiplaadi ID etapi ikoon"><br>KonsolideerimineLitsentseeritudPlaatId</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteineri tüübi etapi ikoon"><br>Konteineritüüp</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Arveldus etapi ikoon"><br>Inventuur</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventuuri põhjusekoodi etapi ikoon"><br>ArvestusePõhjusKood</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Päritoluriiki koodi juhise ikoon"><br>Päritoluriik</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Partii likvideerimissammu ikoon"><br>Likvideerimine</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Valmisastme ikoon"><br>Valmis</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Juhi sisseregistreerimise kinnitussamm"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Sisseregistreerimise ID-etapi ikoon"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Väljaregistreerimise ID-etapi ikoon"><br>SõitjaVäljaregamiseId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Aegumiskuupäeva etapi ikoon"><br>Aegumiskuupäev</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Välja sammu ikoon"><br>Field</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Partii likvideerimissammu ikoon"><br>PartiiLikvideerimine</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Varude olekusammide ikoonilt"><br>VarudeOlekult</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Klastri ID etapi ikoon"><br>AtribuudiId</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Varude partii ID etapi ikoon"><br>InventariPartiiId</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Varude värvi ID etapi ikoon"><br>InventuuriVärviId</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Varude asukoha etapi ikoon"><br>VarudeAsukoht</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Varude seeria ID etapi ikoon"><br>InventSeeriaId</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Varude suuruse ID etapi ikoon"><br>VaruSuuruseId</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Varude oleku ID sammu ikoon"><br>VaruSeisId</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Varude stiili ID etapi ikoon"><br>VaruStiilId</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Varude versiooni ID sammu ikoon"><br>VaruVersioonId</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Ühiku ID etapi ikoon"><br>ÜhikuId</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteineri ID etapi ikoon"><br>ITMKonteinerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM-saadetise ID etapi ikoon"><br>ITMSaatmisID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-kaardi ID etapi ikoon"><br>KanbanKaardiId</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban või kaardi ID etapi ikoon"><br>KanbanVõiKaardiId</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Alamlitsentsiplaadi ID etapi ikoon"><br>LitsentsPlateId</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Koorma ID etapi ikoon"><br>KoormaId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Asukoha litsentsiplaadi paigutuse sammu ikoon"><br>AsukohaLitsentsiPlaadiPaigutus</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Asukoha või litsentsiplaadi sammu ikoon"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Asukoha või litsentsiplaadi sammu ikoon"><br>LocOrLPcheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Asukoha või litsentsiplaadi sammu ikoonilt"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Asukohalt või litsentsiplaadilt sammu ikoonile"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Pika protsessi lõpetatud etapi ikoon"><br>PikkprotsessLõpetatud</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-pausi ema LP etapi ikoon"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Ühendatud konteineri ID etapi ikoon"><br>ÜhendatudKontainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Litsentsiplaadi rea numbri segaikoon"><br>SeagtudJoonNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Väljamineva kaalu astme ikoon"><br>VäljaminevKaal</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Omaniku astme ikoon"><br>Omanik</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Ülemlitsentsiplaadi etapi ikoon"><br>Ülem-LP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Kinnitage sammu ikoon"><br>Palun kinnitage</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ostutellimuse rea numbri sammu ikoon"><br>PoReaNumber</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ostutellimuse rea numbri sammu ikoon"><br>PONum</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Ametikoha täis sammu ikoon"><br>AmetikohtTäis</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Potentsiaalse sammu ikoon"><br>Sisaldus</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Printeri nimeastme ikoon"><br>PrinteriNimi</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Koorma ID etapi ikoon"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Toote kinnitussammu ikoon"><br>TooteKinnitus</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Pane sammu ikoon"><br>Pane</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Pane klastri ID etapi ikoon"><br>PaneäraKlastriId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Koguse astme ikoon"><br>Kogus</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Koguse korrigeerimine astme ikoonil"><br>KogusTäiendusIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Koguse lühike astme ikoon"><br>KogusLühike</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Astme ikooni tarbitav kogus"><br>KogusTarbima</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Astme ikooni tarbitav kogus"><br>KogusVäljaMinev</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Koguse eemaldamise sammu ikoon"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Koguse kinnitussammu ikoon"><br>KogusKinnitus</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Lõpetatuna kinnitatud tööastme ikoon"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Asukoha ID etapi ikooni vastu võtta"><br>RecvAsukohaId</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Konteineri eemaldamise ID etapi ikoon"><br>EemaldaContainerId</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numbriastme ikoon"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Valige tellimuse etapi ikoon"><br>ValiTellimus</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Lühike noppimise põhjuseastme ikoon"><br>LühikeKorjePõhjus</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Sordi positsiooni ID etapi ikoon"><br>LühikeAmetId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Alamlitsentsiplaadi ID etapi ikoon"><br>EesmärkLitsentsPlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Reanumbri etapi ikooniks"><br>ReaNumbriks</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Varude asukoha etapi ikoonile"><br>Asukohta</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numbri astme ikoonile"><br>Numbrile</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Varude asukoha etapi ikoonile"><br>Lattu</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Transpordikoorma ID etapi ikoon"><br>TranspordiVaruId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Hankija partii ID etapi ikoon"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Voo sildi-ID etapi ikoon"><br>VooSildiId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Voo sildi-ID kvaliteedi etapi ikoon"><br>LaineLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Kaalu astme ikoon"><br>Kaal</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Kaalu tarbitava sammu ikoon"><br>KaalToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS kohandamistüübi etapi ikoon"><br>WhSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS-i vastuvõtmise erandisammu ikoon"><br>WhSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS asukoha ID etapi ikoon"><br>WMSAsukohtId</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Töö ID etapi ikoon"><br>Töö ID</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Töö ID etapi ikooni tühistamiseks"><br>TööstIdLoobumine</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Töö litsentsiplaadi ID etapi ikoon"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Töö litsentsiplaadi ID ärapanemise klastri etapi ikoon"><br>TööLPIdPaneäraKlaster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Töö ID etapi ikoon"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Tsooni ID etapi ikoon"><br>TsooniId</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Näide: kohandatud voo etapiikoonide ja pealkirjade määramine

See näide selgitab, kuidas seadistada kohandatud ülesandevoo astme ikoone ja pealkirjasid. Stsenaarium on üles ehitatud kohandatud ülesandevoo näitele, mida esitatakse ja analüüsitakse üksikasjalikumalt järgmises postituses": ladustamise [mobiilirakenduse kohandamine](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Ülesande voog töötab järgmiselt:

1. Rakendus kuvab lehekülje, mis palub töötajal sisestada konteineri ID (nt vöötkoodi skannides).
1. Kui konteineri ID on kehtiv, avab rakendus uue lehe, mis palub töötajal kaalu võtta. (Kui konteineri ID ei kehti, tagastatakse töötaja esimesele leheküljele.)
1. Kui töötaja sisestab kehtiva kaalu, talletab süsteem kaalu ja tagastab töötaja esimesele leheküljele.

Järgmisel illustratsioonil on toodud see töövoog.

![Ülesande voo diagramm.](media/step-icons-example-task-flow.png "Ülesande voo diagramm")

### <a name="create-a-step-class-for-the-container-input-page"></a>Konteineri sisestuslehe etapiklassi loomine

Konteineri sisestusleht võimaldab töötajal skannida või sisestada konteineri ID.

![Konteineri sisestusleht.](media/step-icons-example-container-input.png "Konteineri sisestusleht")

Konteineri sisestuslehel on sisendvälja juhtelemendi nimi `ContainerId`. Kuna see juhtelemendi nimi ei ole [ID-de loendis](#step-ids-classes), te ei leia sellel põhinevat olemasolevat sammu. Seetõttu peate looma astmeklassi, mis sammu esindab. Siin on näide.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Astme ikooni identifikaator salvestatakse klassi liikmele ja astme `defaultStepIcon` pealkiri talletatakse `defaultStepTitle` klassi liikmele.

Astme ikooni määramiseks määrake üks ikooni ID-dest, mis on loetletud `defaultStepIcon` varasemas jaotises [Saadaolevad astme ikoonid](#step-icons) selles teemas.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Kasuta kaalusisendi jaoks standardset või kohandatud etapi ikooni ja pealkirja

Kaalu sisestusleht võimaldab töötajal sisestada kaalu.

![Kaalu sisestusleht.](media/step-icons-example-weight-input.png "Kaalu sisestusleht")

Kaalu sisestuslehel on sisendvälja juhtelemendi nimi `Weight`, mis on [astmete ID-de loendis](#step-ids-classes). Seega, kui klassis määratletud astme ikoon ja pealkiri on teile vastuvõetavad, ei pea te selle `WHSMobileAppStepWeight` sammu jaoks midagi muutma.

Kuid kui eelistate selle sammu jaoks kasutada erinevat ikooni või pealkirja, saate alistada kas `stepId()` meetodi või `stepInfo()` meetodi koosteklassis. Igal ülesandevool on oma etapi teabekonstruktur.

#### <a name="override-the-stepid-method"></a>Meetodi stepId() alistamine

Järgmine näide näitab ühte viisi, kuidas saate muuta koostaja klassi, alistades `stepId()` meetodi.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Seejärel loote sammule `NewWeight` astmeklassi. Kood peaks sarnanema koodiga, `ContainerId` mida selles teemas varem kuvati.

#### <a name="override-the-stepinfo-method"></a>Meetodi stepId() ülekirjutamine

Järgmine näide näitab ühte viisi, kuidas saate muuta koostaja klassi, alistades `stepInfo()` meetodi.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Seejärel saate luua `WHSMobileAppStepInfo` objekti ja seadistada ikooni ja/või pealkirja otse.

## <a name="additional-resources"></a>Lisaressursid

- [Laohalduse mobiilirakenduse installimine ja ühendamine](install-configure-warehouse-management-app.md)
- [Mobiilse seadme kasutaja sätted](mobile-device-user-settings.md)
