---
title: Varude saadavus topeltkirjutuses
description: Selles teemas saate teada, kuidas kontrollida varude saadavust topeltkirjutuses.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: f967f832fc716938c544aad266d2c14a9ea19dd0ca8ee11fe228ce47145f3e78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762422"
---
# <a name="inventory-availability-in-dual-write"></a>Varude saadavus topeltkirjutuses

[!include [banner](../../includes/banner.md)]

Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate toote rakenduses Microsoft Dynamics 365 Sales lehtedele **Pakkumised**, **Tellimused** või **Arved**. Näiteks kontrollite te protsessi [potentsiaalne klient sularahaks](dual-write-prospect-to-cash.md) käigus ühe olulise ülesandena varusid ja määrate täitmiskuupäeva.

Kui teil puuduvad piisavad varud, siis saate eeldatava varude vastuvõtu ja väljastamise alusel tarneaega prognoosida. Samuti saate kontrollida lubamiseks saadaval (ATP) toote teavet, kust leiate lubamiseks saadaval koguse eelmääratletud ajavahemiku raames.

## <a name="on-hand-inventory"></a>Vaba kaubavaru

Rakenduses Dynamics 365 Sales on lehtede **Pakkumised**, **Tellimused** ja **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**. Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte ja toote, mille puhul soovite kontrollida vaba kaubavaru. Selles dialoogiboksis kuvatav teave ühtib teemas [Vaba kaubavaru](../../../../supply-chain/inventory/tasks/check-availability-stock.md) kirjeldatud teabega.

Dialoogiboksis kuvatakse Dynamics 365 Supply Chain Managementist pärit teavet varude kohta. See teave sisaldab järgmiseid koguseid.

- Laos olev kogus
- Reserveeritud laos olev kogus
- Saadaolev laos olev kogus
- Tellitud kogus
- Tellimisel kogus
- Reserveeritud tellitud kogus
- Saadaolev kogus kokku

## <a name="atp-information"></a>ATP teave

Rakenduses Sales on lisatud lehtede **Pakkumised**, **Tellimused** ja **Arved** reakaupadele uus nupp **ATP teave**. Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte, toote, varude saidi, varude lao ja tellimuse koguse. Selle dialoogiboksi sätted ühtivad teemas [Tellimuse lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatutega.

Dialoogiboksis kuvatakse Supply Chain Managementist pärit ATP teave. See teave sisaldab järgmiseid koguseid.

- ATP kogus
- Sissetuleku kogus
- Väljamineku kogus
- Laos olev kogus

## <a name="how-it-works"></a>Toimimisviis

Kui valite **Pakkumised**, **Tellimused** või **Arved** nupu **Vaba kaubavaru**, tehakse **vaba kaubavaru** API-le reaalajas topeltkirjutuse kutse. API arvutab selle toote vaba kaubavaru. Tulemus talletatakse tabelites **InventCDSInventoryOnHandRequestEntity** ja **InventCDSInventoryOnHandEntryEntity** ning seejärel kirjutatakse see topeltkirjutuse abil Dataverse’i. Selle funktsiooni kasutamiseks peate käivitama järgmised topeltkirjutuse kaardid. Jätke kaartide käivitamisel esialgne sünkroonimine vahele.

- CDS-i vaba kaubavaru kirjed (msdyn_inventoryonhandentries)
- CDS-i vaba kaubavaru taotlused (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Mallid

Vaba kaubavaru andmete näitamiseks on saadaval järgmised mallid.

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
---|---|---
[CDS-i vaba kaubavaru kirjed](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS-i vaba kaubavaru kirjete taotlused](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
