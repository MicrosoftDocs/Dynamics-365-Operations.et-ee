---
title: Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine
description: Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is selvehulgimüügi- ja kassahalduskandeid redigeerida ning auditeerida.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a9086da036712fc8c63498d95dc9f71f32f75c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792725"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is selvehulgimüügi- ja kassahalduskandeid redigeerida ning auditeerida.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce'i kliendid kasutavad nii esimese osapoole kassarakendust kui ka kolmanda osapoole kassarakendusi. Esimese osapoole kassarakenduse korral lisatakse kaupluse kanded pakktöötluse kaudu kanalitest Commerce'i peakontorisse. Kolmanda osapoole rakenduste korral lisatakse kanded Commerce'i peakontorisse integratsiooni kaudu. Mõlemal juhul tuleb pärast kannete Commerce'i peakorterisse lisamist läbi teha süsteemsuskontrolli protsess. Selle protsessi käigus kinnitatakse kandeid mitmel viisil ning väljavõttesse lisatakse ainult kinnitamise edukalt läbinud kanded, et neid saaks Commerce'i peakorterisse sisestada.

Commerce'i kannete kinnitamine võib nurjuda eri põhjustel. Integratsioonikoodi või kassarakenduse viga võib põhjustada vastuolulisi andmeid. Lisaks võib vastuolulisi andmeid põhjustada kasutaja viga. Näiteks kui kasutaja kustutab toote pärast seda, kui see on kanaliga sünkroonitud, või kui kasutaja sulgeb rahandusperioodi ilma selle perioodi kandeid sisestamata. Kuigi need kanded märgitakse ära ja jäetakse väljavõtetest välja, võivad need häirida kasutaja igapäevast protsessi, mille käigus sisestatakse müügiteavet finantssüsteemi. Commerce'is saate redigeerida kinnitamist mitteläbinud kandeid ning samal ajal jätta alles kõigi muudatuste auditi.

## <a name="edit-transactions"></a>Kannete redigeerimine

Commerce'i versioonis 10.0.5 on selvehulgimüügikanded (nt müük ja tagastused) ainsad kanded, mida saab redigeerida. Kliendi- ja veebitellimusi ei saa redigeerida. Commerce'i versioonis 10.0.6 ja uuemates saab ka kassahalduskandeid redigeerida.

Commerce'i peakontoris kannete redigeerimiseks toimige järgmiselt.

1. Installige [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Avage Commerce'i peakontoris tööruum **Kaupluse finantsandmed**. Paanil **Kande kinnitamise tõrked** kuvatakse eelfiltreeritud vaade sellise kande lehest, mis ei täitnud üht või rohkemat kinnitusreeglit.
1. Avage kande leht, valige kirje, mille kinnitamine nurjus, valige **Office'i lisandmoodul** ja seejärel **Redigeeri valitud kannet**. Avatakse Exceli fail, milles on valitud kande üksikasjad. See fail sisaldab järgmisi töölehti.

    - **Read** – sellel töölehel on kande päise- ja tooteread ning seotud andmed.
    - **Maksed** – sellel töölehel on kande makseridade üksikasjad.
    - **Allahindlused** – sellel töölehel on kande allahindlusega seotud üksikasjad.
    - **Maksud** – sellel töölehel on kande maksudega seotud üksikasjad.
    - **Tasud** – sellel töölehel on kande tasudega seotud andmed.

1. Muutke Exceli failis asjakohaseid välju ja seejärel laadige andmed uuesti üles Commerce'i peakontorisse, kasutades Dynamics Exceli lisandmooduli avaldamisfunktsiooni. Pärast andmete avaldamist kajastatakse muudatused süsteemis. Avaldamise ajal ei üritata ühtegi kasutajate tehtud muudatust kinnitada.
1. Muudatuste täieliku kontrolljälje vaatamiseks valige päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes suvand **Kuva kontrolljälg**. Näiteks kuvatakse kõik müügiridadega seotud muudatused lehel **Müügikanded** ja kõik maksetega seotud muudatused lehel **Maksekanded**. Muudatuste korral säilitatakse järgmised auditiüksikasjad.

    - Muutmise kuupäev ja kellaaeg
    - Väli
    - Varasem väärtus
    - Uus väärtus
    - Muutja

1. Pärast muudatuste tegemist ja avaldamist käivitage protsess **Kaupluse kannete kinnitamine**, et kontrollida, kas tehtud muudatused on süsteemsed ja kehtivad.

> [!NOTE]
> Saate redigeerida ainult kinnitamist mitteläbinud kandeid. Kui soovite redigeerida kinnitamise läbinud kandeid, määrake kande kinnitamise olekuks **Tõrge** või **Pole** ja seejärel avaldage muudatus. Seejärel saate redigeerida andmeid kande päises või mis tahes muus tütarkirjes ning avaldada päise või kirjed.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Väljavõttega seotud kannete hulgiredigeerimine

Commerce'i versioonis 10.0.6 ja uuemates toetatakse kannete hulgiredigeerimist väljavõtte tasemel.

Commerce'i peakontori väljavõttega seotud kannete hulgiredigeerimiseks toimige järgmiselt.

1. Avage leht **Väljavõtted** ja valige väljavõte, mis sisaldab redigeeritavaid kandeid.
1. Valige nupp **Ava Microsoft Office'is**.
1. Sõltuvalt sellest, mida tuleb redigeerida, valige üks järgmistest suvanditest.

    - **Redigeeri selvehulgimüügikandeid** – see suvand võimaldab redigeerida kõiki väljavõttes sisalduvaid selvehulgimüügikandeid. Saadaval on järgmised Exceli töölehed.

        - **Kanne** – sellel töölehel on kogu müügikannete päisetaseme teave.
        - **Müügikanne** – sellel töölehel on kogu müügikannete reataseme teave.
        - **Maksekanded** – sellel töölehel on kogu müügikannete maksereateave.
        - **Allahindluskanded** – sellel töölehel on kogu müügikannete allahindlusreateave.
        - **Maksukanded** – sellel töölehel on kogu müügikannete maksureateave.
        - **Tasukanded** – sellel töölehel on kogu müügikannete tasureateave.

    - **Redigeeri kassahalduskandeid** – see suvand võimaldab redigeerida kõiki väljavõttes sisalduvaid kassahalduskandeid. Saadaval on järgmised Exceli töölehed.

        - **Kanne** – sellel töölehel on kogu kassahalduskannete päisetaseme teave.
        - **Panka hoiustatud maksevahendi kanded** – sellel töölehel on kõik panka hoiustamise kande üksikasjad.
        - **Seifi maksevahendi kanded** – sellel töölehel on kõik seifi hoiustamise kande üksikasjad.
        - **Päevakassa** – sellel töölehel on kõik päevakassa kande üksikasjad.
        - **Tulu-/kulukanne** – sellel töölehel on kõik tulu-/kulukande rea üksikasjad.
        - **Maksekanded** – sellel töölehel on kogu toimingu **Arve tasumine** ja samuti tulu-/kulukande maksega seotud teave.

1. Redigeerige vajalikke kandeid.

    > [!NOTE]
    > Kui avaldate hulgiredigeeritud kandeid, siis kinnitamisi ei tehta. Peate veenduma, et kõik teie muudatused oleksid täpsed ja andmete kvaliteet kõigil töölehtedel tagatud. Kui soovite näiteks muuta kande kuupäeva, et tulla toime olukordades, kus avatud kannete rahandus- või varude periood on suletud, peate muutma kuupäeva kõigil Exceli töölehtedel, millel on veerg **Ärikuupäev**. Kannete kinnitamiseks pärast nende redigeerimist saate lehel **Väljavõtted** valida suvandi **Kinnita kanded uuesti**. Enne väljavõtte sisestamist oodake, kuni kinnitamistöö on lõpule viidud.

1. Kui kogum on juba loodud, avage leht **Koondatud kanded** ja valige suvand **Loo müügitellimuse XML uuesti**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Väljavõttega mitteseotud kannete hulgiredigeerimine

Commerce'i versioonis 10.0.10 ja uuemates toetatakse võimalust hulgiredigeerida kandeid, mille kinnitamine nurjus, aga mis pole väljavõttega seotud.

Commerce'i peakontori väljavõttega mitteseotud kannete hulgiredigeerimiseks toimige järgmiselt.

1. Avage leht **Kõik kauplused** ja valige kauplus, mille kandeid tuleb redigeerida.
1. Valige nupp **Ava Microsoft Office'is** ja seejärel valige **Redigeeri selvehulgimüügikandeid**.
1. Redigeerige vajalikke kandeid ja seejärel avaldage need.

## <a name="additional-resources"></a>Lisaressursid

[Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine](edit-order-trans.md)

[Jaemüügikannete finantsdimensioonide redigeerimine](edit-financial-dim.md)

[Exceli töövihiku loomine jaemüügikannete redigeerimiseks](create-excel-edit.md)

[Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]