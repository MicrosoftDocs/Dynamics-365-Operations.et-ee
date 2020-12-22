---
title: Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine
description: Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458884"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.

## <a name="overview"></a>Ülevaade

Commerce'i versioonide 10.0.5 ja 10.0.6 vahel lisati võimalus redigeerida selvehulgimüügikandeid (nt müük ja tagastused) ning kassahalduskandeid (nt sularaha sissemakse ja maksevahendi eemaldamine). Commerce'i versioonis 10.0.7 lisati võimalus redigeerida veebitellimuse kandeid ja asünkroonse klienditellimuse kandeid.

## <a name="edit-and-audit-order-transactions"></a>Tellimuse kannete redigeerimine ja auditeerimine

Commerce'i peakontoris tellimuse kannete redigeerimiseks ja auditeerimiseks toimige järgmiselt.

1. Installige [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Sisestage ootelolekukood lehe **Jaemüügi parameetrid** vahekaardi **Klienditellimused** kiirkaardi **Tellimus** lahtrisse **Tellimuse sünkroonimise tõrgete ootelolekukood**.
1. Avage tööruum **Kaupluse finantsandmed**. Paanid **Veebitellimuse sünkroonimise tõrked** ja **Klienditellimuse sünkroonimise tõrked** pakuvad jaemüügikande lehe eelfiltreeritud vaadet. Mõlemal paanil on kuvatud kandekirjed, mille sünkroonimine nurjus asjaomase tellimusetüübi korral.
1. Avage kas leht **Veebitellimuse sünkroonimise tõrked** või leht **Klienditellimuse sünkroonimise tõrked**. Valige kirje sünkroonimistõrke üksikasjade vaatamiseks. Kiirkaardil **Sünkroonimise olek** on järgmised tõrkeüksikasjad.

    - Ootel tellimuse olek
    - Tellimuse tõrke üksikasjad
    - Muutmise kuupäev ja kellaaeg
    - Uuesti proovimiste arv

1. Kui tõrkeüksikasjade järgi tuleb kirje parandada, valige **Office'i lisandmoodul** ja seejärel **Redigeeri valitud kannet**. Avatakse Exceli fail, milles on valitud kande üksikasjad.

    - Kui redigeeritav kanne on veebitellimuse kanne, sisaldab Exceli fail järgmisi töölehti.

        - **Kanne** – sellel töölehel on kande päiseüksikasjad.
        - **Müügikanne** – sellel töölehel on kande reaüksikasjad.
        - **Maksekanded** – sellel töölehel on kande makseridade üksikasjad.
        - **Allahindluse kanded** – sellel töölehel on kande allahindlusega seotud üksikasjad.
        - **Maksukanded** – sellel töölehel on kande maksudega seotud üksikasjad.
        - **Tasukanded** – sellel töölehel on kande tasudega seotud andmed.

    - Kui redigeeritav kanne on asünkroonne klienditellimuse kanne, sisaldab Exceli fail järgmisi töölehti.

        - **Read** – sellel töölehel on kande päise- ja reaüksikasjad.
        - **Maksed** – sellel töölehel on kande makseridade üksikasjad.
        - **Allahindlused** – sellel töölehel on kande allahindlusega seotud üksikasjad.
        - **Maksud** – sellel töölehel on kande maksudega seotud üksikasjad.
        - **Tasud** – sellel töölehel on kande tasudega seotud andmed.

1. Sisestage Exceli failis väljale **Ootel tellimuse olek** tekst **Redigeerimine** ja seejärel avaldage muudatus. Sel viisil ei jäta pakktöötlusrežiimi käigus käitatav töö **Tellimuse sünkroonimine** seda kirjet töötluse ajal vahele.
1. Muutke Exceli failis asjakohaseid välju ja seejärel laadige andmed uuesti üles Commerce'i peakontorisse, kasutades Dynamics Exceli lisandmooduli avaldamisfunktsiooni. Pärast andmete avaldamist kajastatakse muudatused süsteemis. Avaldamise ajal ei üritata ühtegi kasutajate tehtud muudatust kinnitada.
1. Muudatuste täieliku kontrolljälje vaatamiseks valige päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes suvand **Kuva kontrolljälg**. Näiteks kuvatakse kõik müügiridadega seotud muudatused lehel **Müügikanded** ja kõik maksetega seotud muudatused lehel **Maksekanded**. Muudatuste korral säilitatakse järgmised auditiüksikasjad.

    - Muutmise kuupäev ja kellaaeg
    - Väli
    - Varasem väärtus
    - Uus väärtus
    - Muutja

1. Pärast muudatuste tegemist ja avaldamist valige **Sünkrooni tellimus**, et sünkroonimisprotsess kohe käivitada. Teise võimalusena võite lasta pakktöötlusrežiimis käitataval sünkroonimisprotsessil kannet töödelda.

Vaikimisi pannakse tellimused pärast nende edukat sünkroonimist ootele ootelolekukoodi põhjal, mis on määratletud Commerce'i parameetrites. Tellimuste ootelolek tuleb eemaldada, enne kui tellimusi saab täitmise või muude toimingute jaoks edasi töödelda.

## <a name="additional-resources"></a>Lisaressursid

[Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine](edit-cash-trans.md)

[Jaemüügikannete finantsdimensioonide redigeerimine](edit-financial-dim.md)

[Exceli töövihiku loomine jaemüügikannete redigeerimiseks](create-excel-edit.md)

[Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks](add-fields-excel.md)
