---
title: Kolmanda osapoole tootmise käivitussüsteemidega integreerimine
description: See teema kirjeldab, kuidas saate Integreerida Microsofti Dynamics 365 Supply Chain Management kolmanda osapoole tootmise käivitamissüsteemiga (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8917c9b265bc3df19517f052e28fb7644057cb46
ms.sourcegitcommit: 19f0e69a131e9e4ff680eac13efa51b04ad55a38
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/22/2022
ms.locfileid: "8330697"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Kolmanda osapoole tootmise käivitussüsteemidega integreerimine

[!include [banner](../includes/banner.md)]

Mõned tootmisorganisatsioonid, mis kasutavad Microsoft-i Dynamics 365 Supply Chain Management, kasutavad Dynamics 365-i omafunktsioone, et juhtida nende tootmistegevust masinate, seadmete ja personali puhul. Kuid teised tootmisorganisatsioonid, eriti need, kellel on täpsemad tootmisnõuded, kasutavad hoopis kolmanda osapoole tootmise käivitamise süsteemi (MES). Organisatsioonid võivad valida kolmanda isiku mes-i lahenduse, sest näiteks on see spetsiifiliselt kohandatud nende vertikaalsele majandusharule.

Integreeritud lahenduses on andmevahetus täielikult automaatne ja toimub reaalaja lähedal. Seetõttu säilitatakse andmeid mõlemas süsteemis ja käsitsi andmesisestus ei ole vajalik. Näiteks kui materjalitarbimine on MES-is registreeritud, tagab integratsioon, et sama tarbimine registreeritakse ka Dynamics 365-s. Seetõttu on ajakuupäevad laokirjed saadaval teistele olulistele protsessidele, nt planeerimisele ja müügile.

Lahendus muudab tarneahela halduse kasutajate jaoks kolmanda osapoole MES-iga integreerumise kiiremaks, lihtsamaks ja odavamaks. See pakub järgmisi funktsioone:

- Ärisündmused ja liidesed, mis toetavad tootmise [käivitamise võtmeprotsesse](#processes-available-for-mes-integration)
- Tsentraliseeritud armatuurlaud, kus saate jälgida sündmuste töötlemise ajalugu ning tõrkeid sooritava protsessi tõrkeotsingut ja parandusprotsesse

Järgmine näide näitab tüüpilist ärisündmuste, protsesside ja teadete kogum, mida vahetatakse integreeritud lahenduses.

![Tüüpiline integratsioonistsenaarium.](media/3p-mes-scenario.png "Tüüpiline integratsioonistsenaarium.")

## <a name="turn-on-the-mes-integration-feature"></a>Lülita MES-i integreerimisfunktsioon sisse

Enne selle funktsiooni kasutamist peab administraator selle teie süsteemis sisse lülitama, nagu kirjeldatud järgmises protseduuris.

1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Veenduge, et kellaaja **ja kohalviibimise** litsentsivõti on lubatud (kuvab märkeruudu). See litsentsivõti on vajalik, kuna see kontrollib tootmise käivitamise süsteemi funktsioone ja andmeid. Kui see ei ole lubatud, järgige järgmisi samme.
    1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. **Litsentsi konfiguratsioonilehel** valige märkeruut **Kellaaeg ja kohalviibimine**.
    1. Lülitage hooldusrežiim välja, nagu on kirjeldatud hooldusrežiimis [.](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Minge süsteemihalduse **tööruumide \> funktsioonihaldusesse \>**.
1. Lülitage sisse järgmisel viisil loetletud funktsioon (vt ka funktsioonihalduse [ülevaadet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Moodul:** *tootmise juhtimine*
    - **Funktsiooni nimi: tootmise** *käivitamissüsteemi integreerimine*

## <a name="processes-available-for-mes-integration"></a>MES-i integreerimiseks saadaolevad protsessid

Saate lubada mis tahes või kõik järgmised integratsiooniprotsessid.

| Protsessi nimi | Kirjeldus |
|---|---|
| Tootmistellimuste ja tootmistellimuse oleku muutmise ärisündmuse väljaminev | See protsess pakub ärisündmuse, mida GIS saab kuulaks, et saada teavet tootmistellimuste kohta, mida tuleb toota. Tootmistellimusega seotud viiteandmed jagatakse eeldatavalt tarneahela haldamisest MES-ile Open Data Protocoli (OData) või andmeüksuste kaudu. |
| Käivita tootmistellimus | See protsess varustab tarneahela haldust teabega tootmistellimuste kohta, mis käivitatakse MES-i kasutades. See tagab, et mõlemas süsteemis on uuendatud kõikide tootmistegevuste vaade. |
| Toodetud või praagitud koguse aruanne | See protsess varustab tarneahela haldust teabega nende heade ja veakoguste kohta, mis on tootmistöös mes-i kasutades teatatud. See tagab, et tööde ülevaatajad peavad tootmisplaani edenemist uuendatud vaates. |
| Teata materjali tarbimisest | See protsess varustab tarneahela haldust MES-i teabega tarbitavate materjalide koguse kohta. See teeb uuendatud laokirjed kättesaadavaks teistele olulistele protsessidele, nt planeerimisele ja müügile. |
| Operatsiooni jaoks tarbitud aja teatamine | See protsess varustab tarneahela haldust teabega konkreetseks operatsiooniks kasutatud aja kohta. |
| Tootmistellimuse lõpetamine | See protsess teavitab tarneahela haldust, et MES on värskendanud tootmistellimuse oma lõplikuks olekuks *Lõpetatud*. See olek näitab, et tootmistellimusega ei toodeta rohkem koguseid. |

## <a name="monitor-incoming-messages"></a>Saate jälgida sissetulevaid teateid.

Süsteemi sissetulevate teadete jälgimiseks avage tootmise käivitamissüsteemide **integreerimise** leht. Seal saate vaadata, töödelda ja tõrkeotsingu probleeme.

## <a name="call-the-api"></a>Helista API-sse

MES-i integratsiooni API kutsumiseks saatke taotlus `POST` järgmise lõpp-punkti URL-ile:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Teie saatmistaotluse keha peaks sarnanema järgmise näitega. Asendage väärtused väärtusega `_companyId``_messageType` ja vastavalt `_messageContent` vajadusele. Teavet erinevate teatetüüpide kohta, mida API toetab ja kuidas nende sisu kujundada, vt järgmisest jaotisest.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API teatetüübid ja sisu

See jaotis kirjeldab igat tüüpi teateid, mida saab MES-i integratsiooni API kaudu vahetada.

### <a name="start-production-order-message"></a>Käivita tootmistellimuse teade

Tootmistellimuse *teate alguseks* on `_messageType` väärtus .`ProdProductionOrderStart` Järgmine tabel näitab välju, mida see teade toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ProductionOrderNumber` | Kohustuslik | String |
| `StartedQuantity` | Valikuline | Tegelik |
| `StartedDate` | Valikuline | Kuupäev |
| `AutomaticBOMConsumptionRule` | Valikuline | Loetelu (FlushingPrincip Alati \| mitte kunagi \|) |

### <a name="report-as-finished-message"></a>Teata lõpetatuna

*Lõpetatuna kinnitatud teate* väärtus `_messageType` on `ProdProductionOrderReportFinished`. Järgmine tabel näitab välju, mida see teade toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ProductionOrderNumber` | Kohustuslik | String |
| `ReportFinishedLines` | Kohustuslik | Ridade loend (vähemalt üks), millest igaüks sisaldab järgmises tabelis kirjeldatud lasti |

Järgnev tabel näitab välju, mida sõnumi jaotise `ReportFinishedLines` iga rida `ProdProductionOrderReportFinished` toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `LineNumber` | Valikuline | Tegelik |
| `ItemNumber` | Valikuline | String|
| `ProductionType` | Valikuline | Enum (MainItem \| valemi \| kooslus \| Co_Product \| By_Product \| Puudub), laiendatav |
| `ReportedErrorQuantity` | Valikuline | Tegelik|
| `ReportedGoodQuantity` | Valikuline | Tegelik|
| `ReportedErrorCatchWeightQuantity` | Valikuline | Tegelik |
| `ReportedGoodCatchWeightQuantity` | Valikuline | Tegelik |
| `AcceptError` | Valikuline |Loogiline |
| `ErrorCause` | Valikuline | Enum (pole \| materjalimasina \|\| operatsioonisüsteemi), laiendatav |
| `ExecutedDateTime` | Valikuline | DateTime |
| `ReportAsFinishedDate` | Valikuline | Kuupäev |
| `AutomaticBOMConsumptionRule` | Valikuline | Loetelu (FlushingPrincip Alati \| mitte kunagi \|) |
| `AutomaticRouteConsumptionRule` | Valikuline |Enum (RouteDependent \| Alati mitte kunagi \|) |
| `RespectFlushingPrincipleDuringOverproduction` | Valikuline | Loogiline |
| `ProductionJournalNameId` | Valikuline | String |
| `PickingListProductionJournalNameId` | Valikuline | String|
| `RouteCardProductionJournalNameId` | Valikuline | String |
| `FromOperationNumber` | Valikuline | Täisarv|
| `ToOperationNumber` | Valikuline | Täisarv|
| `InventoryLotId` | Valikuline | String |
| `BaseValue` | Valikuline | String |
| `EndJob` | Valikuline | Loogiline |
| `EndPickingList` | Valikuline | Loogiline |
| `EndRouteCard` | Valikuline | Loogiline |
| `PostNow` | Valikuline | Loogiline |
| `AutoUpdate` | Valikuline | Loogiline |
| `ProductColorId` | Valikuline | String|
| `ProductConfigurationId` | Valikuline | String |
| `ProductSizeId` | Valikuline | String |
| `ProductStyleId` | Valikuline | String |
| `ProductVersionId` | Valikuline | String |
| `ItemBatchNumber` | Valikuline | String |
| `ProductSerialNumber` | Valikuline | String |
| `LicensePlateNumber` | Valikuline | String |
| `InventoryStatusId` | Valikuline | String |
| `ProductionWarehouseId` | Valikuline | String |
| `ProductionSiteId` | Valikuline | String |
| `ProductionWarehouseLocationId` | Valikuline | String |
| `InventoryDimension1` kuni `InventoryDimension12` | Valikuline | String |

12 laiendatav dimensioon (`InventoryDimension1` kuni `InventoryDimension12`) nõuab kohandamist ja neid ei kasutata alati. Lisateavet nende kohta vt jaotisest Uute [varude dimensioonide lisamine laiendi kaudu](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Materjalitarbimise (komplekteerimisleht) teade

Materjalitarbimise *(komplekteerimislehe)* teate puhul on `_messageType` väärtus `ProdProductionOrderPickingList`. Järgmine tabel näitab välju, mida see teade toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ProductionOrderNumber` | Kohustuslik | String |
| `JournalNameId` | Valikuline | String |
| `PickingListLines` | Kohustuslik | Ridade loend (vähemalt üks), millest igaüks sisaldab järgmises tabelis kirjeldatud lasti |

Järgnev tabel näitab välju, mida sõnumi jaotise `PickingListLines` iga rida `ProdProductionOrderPickingList` toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ItemNumber` | Kohustuslik | String |
| `ConsumptionBOMQuantity` | Valikuline | Tegelik |
| `ProposalBOMQuantity` | Valikuline | Tegelik |
| `ScrapBOMQuantity` | Valikuline | Tegelik |
| `BOMUnitSymbol` | Valikuline | String |
| `ConsumptionInventoryQuantity` | Valikuline | Tegelik |
| `ProposalInventoryQuantity` | Valikuline | Tegelik |
| `ConsumptionCatchWeightQuantity` | Valikuline | Tegelik |
| `ProposalCatchWeightQuantity` | Valikuline | Tegelik |
| `ConsumptionDate` | Valikuline | Kuupäev |
| `OperationNumber` | Valikuline | Täisarv |
| `LineNumber` | Valikuline | Tegelik |
| `PositionNumber` | Valikuline | String |
| `IsConsumptionEnded` | Valikuline | Loogiline |
| `ErrorCause` | Valikuline | Enum (pole \| materjalimasina \|\| operatsioonisüsteemi), laiendatav |
| `InventoryLotId` | Valikuline | String |

### <a name="time-used-for-operation-route-card-message"></a>Operatsiooni (protsessikaardi) teate jaoks kasutatav aeg

*Operatsiooni (protsessikaardi) teates kasutatava aja* väärtus `_messageType` on `ProdProductionOrderRouteCard`. Järgmine tabel näitab välju, mida see teade toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ProductionOrderNumber` | Kohustuslik | String |
| `JournalNameId` | Valikuline | String |
| `RouteCardLines` | Kohustuslik | Ridade loend (vähemalt üks), millest igaüks sisaldab järgmises tabelis kirjeldatud lasti |

Järgnev tabel näitab välju, mida sõnumi jaotise `RouteCardLines` iga rida `ProdProductionOrderRouteCard` toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `OperationNumber` | Kohustuslik | Täisarv |
| `OperationPriority` | Valikuline | Enum (esmane \| teisene 1 \| . sekundaarne2 \| ... \| Teisene 20) |
| `OperationId` | Valikuline | String |
| `OperationsResourceId` | Valikuline | String |
| `Worker` | Valikuline | String |
| `HoursRouteCostCategoryId` | Valikuline | String |
| `QuantityRouteCostCategoryId` | Valikuline | String |
| `HourlyRate` | Valikuline | Tegelik |
| `Hours` | Valikuline | Tegelik |
| `GoodQuantity` | Valikuline | Tegelik |
| `ErrorQuantity` | Valikuline | Tegelik |
| `CatchWeightGoodQuantity` | Valikuline | Tegelik |
| `CatchWeightErrorQuantity` | Valikuline | Tegelik |
| `QuantityPrice` | Valikuline | Tegelik |
| `ProcessingPercentage` | Valikuline | Tegelik |
| `ConsumptionDate` | Valikuline | Kuupäev |
| `TaskType` | Valikuline | Loend (QueueBefore häälestusprotsessi \|\| kattumine \| transpordi \| ootel \| seisakuga \|) |
| `ErrorCause` | Valikuline | Enum (pole \| materjalimasina \|\| operatsioonisüsteemi), laiendatav |
| `OperationCompleted` | Valikuline | Loogiline |
| `BOMConsumption` | Valikuline | Loogiline |
| `ReportAsFinished` | Valikuline | Loogiline |

### <a name="end-production-order-message"></a>Tootmistellimuse lõpetamise teade

Tootmistellimuse *lõppteate* väärtus `_messageType` on `ProdProductionOrderEnd`. Järgmine tabel näitab välju, mida see teade toetab.

| Välja nimi | Olek | Tüüp |
|---|---|---|
| `ProductionOrderNumber` | Kohustuslik | String |
| `ExecutedDateTime` | Valikuline | DateTime |
| `EndedDate` | Valikuline | Kuupäev |
| `UseTimeAndAttendanceCost` | Valikuline | Loogiline |
| `AutoReportAsFinished` | Valikuline | Loogiline |
| `AutoUpdate` | Valikuline | Loogiline |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Võta sõnumi oleku kohta tagasisidet

Pärast seda, kui MES on tarneahela haldusse sõnumi saatnud, võib tarneahela haldamise puhul olla oluline anda sõnumi oleku kohta tagasisidet. Siin on mõned näited juhtumitest, kus see käitumine võib olla asjakohane:

- Ükski isik ei ole vastutav MES-i integratsiooni juhendamise eest.
- Isik, kes vastutab MES-i integratsiooni üle järelvalve eest, soovib saada meili teel teadet, kui teade nurjub, nii et nad teaksid, et peavad midagi ette võtma.
- Et teavitada tööde juhtimise osakonda või it-osakonna operaatoreid, et nad peavad midagi ette võtma, peab meS kuvama veateate.
- Pärast tõrketeate saamist peab MES tellimuse graafiku ümber arvutama (nt tootmistellimuse käivitamine ebaõnnestus).

Sellisel juhul saate kasutada tarneahela halduses standardset teatisefunktsiooni. Lisateavet selle kohta, kuidas standardsed teatised töötavad, vaadake järgmistest ressurssidest:

- Spikriteema teatiste [ülevaade](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [teatisereegli valikud Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Näiteks võite sõnumi oleku kohta tagasiside andmiseks seadistada järgmised teatised:

- Looge ärisündmus ("Väliselt saatmine")., mida kasutatakse teate *nurjumisel*.
- Saate saata teatise ja e-kirja IT-haldus- või tootmisjuhile.
