---
title: Täiendamine tagastamiskanbanitega
description: Selles teemas kirjeldatakse, kuidas väljavõtmise kanbani kasutatakse tootmistegevuste puhul materjali täiendamiseks.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0caa0020083138f702e4a1fda457b7075a9c87e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426574"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Täiendamine tagastamiskanbanitega

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas väljavõtmise kanbani kasutatakse tootmistegevuste puhul materjali täiendamiseks.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Väljavõtmise kanbani kasutav materjali täiendamise töövoog
-------------------------------------------------------------------

Väljavõtmise kanbani saab kasutada üksiku kauba kanbani liigutamiseks ladude ja tootmiskohtade vahel, kus materjali tarbitakse. Väljavõtmise kanban toetab materjali täiendamise tõmbepõhist lahendust, kus konkreetse nõudluse jaoks pakkumise käivitamiseks on vaja tõmbesignaali. 

Järgmine stsenaarium näitab tõmbepõhist täiendamissüsteemi, kus tõmbesignaal käivitab kanban-töö loomise tootmisprotsessi jaoks materjali täiendamiseks. 

[![Tõmbesignaal käivitab kanbani loomise tootmisprotsessi jaoks materjali täiendamiseks](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Kanbani väljaminek
2.  Kanbani lähtekoht ja asetamise koht laotöö jaoks
3.  Kanbani sihtkoht ja toodangu sisestuskoht
4.  Tootmisprotsess
5.  Laotöö kanbani komplekteerimiseks
6.  Toormaterjali laoasukohad
7.  Materjaliladu
8.  Tootmisladu

Selles stsenaariumis tarbib tootmisprotsess (4) materjali toodangu sisestuskohast (3) tootmislaos (8). Kui materjali käsitlemisühik (kanban) on ära tarbitud, registreeritakse see tühjana. Kauba lähtekohale luuakse täiendamise signaal ja luuakse uus kanban (1). Sellisel juhul koosneb kauba lähtekoht asukohtadest materjalilaos (7). Kambani materjal komplekteeritakse ja asetatakse asukohta (2) samas laos. Kui materjal on komplekteeritud, on see valmis edastamiseks asukohast 2 toodangu sisestuskohta (3) tootmislaos (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Laotöö konfigureerimine kanbani komplekteerimiseks väljavõtmise kanbani jaoks

Väljavõtmise kanbani jaoks toormaterjali komplekteerimise lubamiseks tuleb konfigureerida voomallid, töömallid ja asukohakorraldused töötellimuse tüübiga **Kanbani komplekteerimine**. See töötellimuse tüüp ei toeta ainult väljavõtmise kanbani komplekteerimisprotsessi. See toetab ka tootmise kanbani komplekteerimisprotsessi. Kuid iga kanbani tüübi jaoks saab konfigureerida eraldi komplekteerimisprotsessi, eraldades voomallid, töömallid ja asukohadirektiivid. Voomallide, töömallide ja asukohadirektiivide eraldamiseks määrake nende üksuste päringutes kriteeriumid tegevuse tüübile (**Töötlemine** või **Üleviimine**).

## <a name="configure-the-withdrawal-kanban"></a>Väljavõtmise kanbani konfigureerimine

Väljavõtmise kanbani puhul kasutatav üleviimistegevus konfigureeritakse aktiveeritud tegevusplaani osana säästlikus tootmisvoos. Üleviimistegevuse konfiguratsiooni osana tuleb määrata üleviimise lähte- ja sihtkoht. Pärast üleviimistegevuse konfigureerimist võite määrata selle kanban-reeglile tüübiga **Väljavõtmine**. Kanban-reegel määrab väljavõtmise kanbani poliitikad ja konfiguratsioonid. Kanbani kogus määrab, mitut käsitlemisühikut kanban üleviimisprotsessi ajal kannab. Fikseeritud täiendusstrateegia valimisel kasutatakse fikseeritud kanbani kogust. See kogus määratleb, kui palju kanbane on vaja, et vältida varude lõppemist nõudluse allika suhtes. Fikseeritud koguse saab arvutada tegeliku nõudluse, varasema nõudluse ja teenindustasemete põhjal. Järgmised kaks stsenaariumi kirjeldavad, kuidas on võimalik täiendada materjali, kui kasutatakse väljavõtmise kanbani.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>1. stsenaarium: toodangu sisestuskoha täiendamine fikseeritud väljavõtmise kanbani kasutades

Tootmisprotsess tarbib ostetud toorainet toodangu sisestuskohast, mis asub tootmislaos. Kui toormaterjal hankijalt saadakse, ladustatakse see materjalilao asukohtades. Kuna nõudlust materjali järele peetakse teatud perioodil stabiilseks, on see seadistatud varustama tootmist fikseeritud koguses kanban-vooga. Kui kanban on toodangu sisestuskohas tarbitud, registreeritakse tühi signaal ja voole lisatakse uus sama tüüpi kanban. 

Tühja signaali saab seadistada kanbani lõpetamisel automaatselt vallanduma. Teise võimalusena saab tühja signaali seadistada käsitsi toiminguna, mis tehakse Kanbani ülekandmise tahvlilt või pihuseadme menüüst. Kanbani ülekandmise tahvel on tööruum, kus hallatakse kõik kanbani töötsükli toiminguid. 

Kanbani loomisel materjalilao kanban-voole toormaterjali voo rida. Kanbani ülekandmise tahvli komplekteerimisloendi jaotises saab jälgida materjali ja seotud laoprotsesside olekut alates voo loomisest kuni töö loomiseni, kuni materjal on üleviimise lähtekohas vaba ja valmis toodangu sisestuskohtadesse ülekandmiseks. Kanbani saab lõpetada Kanbani ülekandmise tahvlile või pihuseadme menüüst. 

Selles stsenaariumis töödeldakse materjalilaos toimuvat komplekteerimistööd ühe tegevusena. Ülekandmistegevust materjalilao ja tootmislau vahel töödeldakse eraldi tegevusena. See lähenemisviis võib olla abiks juhul, kui kahe lao vahel on näiteks suur füüsiline vahemaa. Sellisel juhul võib kanbani ülekandmistegevus kajastada veost. 

Kui laoasukohtade ja toodangu sisestuskoha vahemaa on väike, võib olla tõhusam ülekandmistegevuse lisamine komplekteerimisprotsessi. Seejärel, kui materjal on komplekteeritud, saab selle asetada otse toodangu sisestuskohta. Selle protsessi toetamiseks konfigureeritakse ülekandmistegevus nii, et see lõpetatakse automaatselt, kui väljavõtmise kanbani komplekteerimistöö on töödeldud.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>2. stsenaarium: ülekandmistegevuse automaatne lõpetamine, kui kanbani komplekteerimistöö on töödeldud

Järgmises stsenaariumis on väljavõtmise kanbani ülekandmistegevus konfigureeritud liikuma kahe asukoha vahel samas laos. Väljavõtmise kanbani ülekandmistegevus on seadistatud nii, et see viiakse lõpule automaatselt. 

[![Ülekandmistegevus viiakse automaatselt lõpule, kui kanbani komplekteerimistöö on töödeldud](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Toormaterjali ja tootmise ühine ladu
2.  Toormaterjalide laoasukohad
3.  Kanbani lähtekoht ja asetamise koht laotöö jaoks
4.  Kanbani väljaminek
5.  Toodangu sisendasukoht
6.  Tootmisprotsess

Kui kanban on toodangu sisestuskohas tarbitud, registreeritakse kanban tühjaks ja voole lisatakse uus kanban. Kanbani loomisel lisatakse kanban-voole voorida. Kui kanban-voog on töödeldud, luuakse laotöö kanbani komplekteerimiseks. Laotöötaja töötleb kanbani komplekteerimise tööd ja töö suunab teda laoasukohta kanbani materjali komplekteerima. Kui see laotöötaja komplekteerimise kinnitab, viiakse kanban automaatselt lõpule ja laotöötaja suunatakse asetama materjali toodangu sisestuskohta.

