---
title: Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine
description: Selles artiklis kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712104"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.

## <a name="overview"></a>Ülevaade

Commerce'i versioonide 10.0.5 ja 10.0.6 vahel lisati võimalus redigeerida selvehulgimüügikandeid (nt müük ja tagastused) ning kassahalduskandeid (nt sularaha sissemakse ja maksevahendi eemaldamine). Commerce'i versioonis 10.0.7 lisati võimalus redigeerida veebitellimuse kandeid ja asünkroonse klienditellimuse kandeid.

## <a name="edit-and-audit-order-transactions"></a>Tellimuse kannete redigeerimine ja auditeerimine

Commerce'i peakontoris tellimuse kannete redigeerimiseks ja auditeerimiseks toimige järgmiselt.

1. Installige [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Sisestage ootelolekukood lehe **Commerce'i parameetrid** vahekaardi **Klienditellimused** kiirkaardi **Tellimus** lahtrisse **Tellimuse sünkroonimise tõrgete ootelolekukood**.
2. Peatage muud tellimuse sünkroonimise tööd, mis on teie redigeerimise ja auditeerimise ajaga vastuolus.
3. Avage tööruum **Kaupluse finantsandmed**. Paanid **Veebitellimuse sünkroonimise tõrked** ja **Klienditellimuse sünkroonimise tõrked** pakuvad jaemüügikande lehe eelfiltreeritud vaadet. Mõlemal paanil on kuvatud kandekirjed, mille sünkroonimine nurjus asjaomase tellimusetüübi korral.
4. Avage kas leht **Veebitellimuse sünkroonimise tõrked** või leht **Klienditellimuse sünkroonimise tõrked**. Valige kirje sünkroonimistõrke üksikasjade vaatamiseks. Kiirkaardil **Sünkroonimise olek** on järgmised tõrkeüksikasjad.

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
    > [!NOTE]
    > Kui te ei leia redigeerimist vajavat välja, järgige alltoodud toiminguid töölehele puuduva välja lisamiseks.
    >   1. Valige andmekonnektoris **Kujunda**
    >   1. Valige pliiatsiikoon tabeli kõrvalt, millele soovite välja lisada.
    >   1. Valige väli jaotisest **Saadaolevad väljad** ja seejärel valige **Lisa**.
    >   1. Lisage vajaminev väljade hulk ja seejärel valige **Värskenda**.
    >   1. Kui värskendus on lõpule viidud, peate väärtuste värskendamiseks valima **Värskenda**.

3. Muudatuste täieliku kontrolljälje vaatamiseks valige päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes suvand **Kuva kontrolljälg**. Näiteks kuvatakse kõik müügiridadega seotud muudatused lehel **Müügikanded** ja kõik maksetega seotud muudatused lehel **Maksekanded**. Muudatuste korral säilitatakse järgmised auditiüksikasjad.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
