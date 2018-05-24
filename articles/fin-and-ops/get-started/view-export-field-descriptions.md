---
title: "Väljade kirjelduste vaatamine ja eksportimine"
description: "Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1ee87dbe9dab089a893d9c69d2573a4c4b11b58
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="view-and-export-field-descriptions"></a>Väljade kirjelduste vaatamine ja eksportimine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks.

Microsoft Dynamics 365 for Finance and Operationsis on antud mõne keerukama välja kirjeldused. Need kirjeldused kuvatakse, kui liigute välja kohale. Väljade kirjeldusi saab vaadata ja eksportida ka lehel **Väljade kirjeldused**. 

Kõigil lehekülgedel ei ole väljade kirjeldusi. Soovime pakkuda kirjeldusi ainult keerukamate väljade jaoks, mitte nende väljade jaoks, mille kasutamine on ilmselge. Seetõttu pole mõnel lehel väljade kirjeldusi, mõnel lehel on mõned kirjeldused ja mõnel keerukamal lehel (nt paljudel parameetrilehtedel) on palju kirjeldusi. 

Kui teil on juurdepääs Finance and Operationsi arenduskeskkonnale, saate lisada uusi väljade kirjeldusi ja kohandada olemasolevaid kirjeldusi. Näiteks saate lisada välja kirjeldusele ettevõttepõhist teavet. Lisateavet leiate jaotisest [Välja spikri kohandamine](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Väljakirjelduste vaatamine kasutajaliideses
Välja kirjelduse vaatamiseks liikuge välja kohale. Kui kirjeldus puudub, näete välja kohale liikudes välja nime. (Märkus. Dynamics AX-i versioonis 7.0 (veebruar 2016) saab välja kirjeldusi vaadata ainult lehel **Välja kirjeldused**.) Järgmine joonis näitab välja kirjeldust, mis ilmub, kui liigutate kursori välja **Lukusta kaubad inventuuri ajaks** kohale. 

[![Väljakirjelduse näide](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Kasutage lehte Väljade kirjeldused väljaspikri vaatamiseks ja eksportimiseks
Leht **Väljade kirjeldused** võimaldab väljade kirjeldusi vaadata ja eksportida. Saate korraga vaadata ühe lehe jaoks saadaolevaid kirjeldusi.

### <a name="view-the-descriptions-for-a-page"></a>Vaadake lehe kirjeldusi

Lehe kirjelduste vaatamiseks tehke järgmist.

-   Sisestage väljale **Lehe valimine** lehe nimi. Teise võimalusena klõpsake noolt kõigi lehtede loendi avamiseks ja seejärel sirvige või filtreerige loendit.

Saate kasutada kasutajaliideses kuvatavat lehe nime (nt **Kliendid**) või lehe koodnime (AOT-nime), mis on kättesaadav lehele paremklõpsates (nt **CustTable**). 

Teavet mitmesuguste võimaluste kohta lehtede loendi filtreerimiseks leiate selle artikli edasisest osast „Lehe otsimine”. 

Kui määrate valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**, kuvatakse kõik lehe väljad, olenemata sellest, kas neil on kirjeldus.

### <a name="export-the-descriptions-for-a-page"></a>Ekspordi lehe kirjeldused

Kirjelduste eksportimiseks tehke järgmist.

1.  Valige leht väljalt **Lehe valimine**.
2.  Klõpsake nuppu **Ava Microsoft Office’is** ülemises parempoolses nurgas ja klõpsake siis valikut **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Lehe otsimine

Lehe otsimiseks väljal **Lehe valimine** on mitu võimalust. Paljudel juhtudel tuleb klõpsata noolt väljal **Lehe valimine**, et avada ripploend ja valida siis filtreeritud lehtede loendist.

-   Sisestage nime osa ning avage siis ripploend, et filtreeritud lehtede loendist valida.
-   Avage ripploend ja klõpsake siis pealkirja **Lehe nimi** loendi ülaosas või pealkirja **Lehe AOT-nimi**. Avaneb dialoogiboks, kus saate kasutada täpsema filtreerimise valikuid, nt **Lehe nimi algab tähega**.
-   Sisestage lehe täisnimi Selle valiku kasutamisel tasub avada ripploend ja vaadata, mida see veel sisaldab, ka siis, kui väljade kirjeldused on nähtavad.
    -   Kui nimele on üks täpne vaste, näidatakse selle lehe väljade kirjeldusi.
    -   Kui on mitu täpset vastet, ei kuvata ühtegi kirjeldust. Peate ripploendi avama ja valima soovitud lehe.
    -   Kui sisestatud lehe nimi on osa teise lehe nimest, näete oma lehe kirjeldusi. Kuid kui avate ripploendi, siis näete veel lehti, mis seda nime sisaldavad.

Näiteks ei kuvata ühtegi kirjeldust, kui sisestate sõna <strong>Inventuur</strong> väljale *<strong><em>Lehe valimine</em></strong>*. Avate ripploendi ja näete, et on olemas kaks lehte nimega <strong>Inventuur</strong> ja mitu lehte, mille nimes on sõna „inventuur”. Kui valite lehe, mille AOT-nimi on <strong>InventJournalCount</strong>, kuvatakse selle lehe väljade kirjeldused. Kui aga ripploendi uuesti avate, näete, et loend sisaldab nüüd kõiki lehti, mille AOT-nime osa on „InventJournalCount”.

## <a name="troubleshooting"></a>Tõrkeotsing
Selles jaotises on teave, mis on abiks veaotsingul probleemide osas, millega võite väljade kirjelduste kasutamisel kokku puutuda.

### <a name="i-cant-find-a-field-description"></a>Ma ei leia välja kirjeldust

Praegu on käimas kirjelduste lisamise toiming keerulisematele väljadele. Kui vajate konkreetse välja puhul abi, andke meile sellest teada, lisades sellele teemale kommentaari.

### <a name="the-field-description-isnt-helpful"></a>Välja kirjeldusest ei ole abi

Andke meile sellest teada, lisades sellele teemale kommentaari. Võimaluse korral kirjeldage lisateavet, mida vajate.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Ma ei leia lehelt Väljade kirjeldused välja.

Kõigi väljade kuvamiseks lehel määrake valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**. Klõpsake välja **Lehe valimine** kontrollimiseks, kas olete õige lehe valinud. Kui sisestatud nimi on osa teise välja nimest, siis valisite võib-olla lehe, millel on pikem nimi.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Ma ei leia lehelt Väljade kirjeldused lehte.

Teavet mitmesuguste võimaluste kohta lehtede otsimiseks leiate selle artikli varasemast osast „Lehtede otsimine”. Kui sisestasite lehe täpse nime, ei pruugi väljade kirjeldusi näha olla, kui sama nimi on mitmel lehel. Klõpsake noolt väljal **Lehe valimine**, et avada saadaolevate lehtede filtreeritud loend.

<a name="additional-resources"></a>Lisaressursid
--------

[Väljaspikri kohandamine](../../dev-itpro/user-interface/customize-field-help.md)





