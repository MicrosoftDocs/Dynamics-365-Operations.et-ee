---
title: Väljade kirjelduste vaatamine ja eksportimine
description: Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks.
author: twheeloc
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.form: FieldDescriptions
ms.openlocfilehash: d2d59796b312d50d69bf7722b605c159a933a283
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292362"
---
# <a name="view-and-export-field-descriptions"></a>Väljade kirjelduste vaatamine ja eksportimine

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Selles artiklis kirjeldatakse, kuidas vaadata väljade kirjeldusi ja kuidas kasutada väljade kirjelduste lehte kirjelduste eksportimiseks.

Mõnedel keerukamatel väljadel on välja kirjeldused. Need kirjeldused kuvatakse, kui liigute välja kohale. Väljade kirjeldusi saab vaadata ja eksportida ka lehel **Väljade kirjeldused**.

Kõigil lehekülgedel ei ole väljade kirjeldusi. Soovime pakkuda kirjeldusi ainult keerukamate väljade jaoks, mitte nende väljade jaoks, mille kasutamine on ilmselge. Seetõttu pole mõnel lehel väljade kirjeldusi, mõnel lehel on mõned kirjeldused ja mõnel keerukamal lehel (nt paljudel parameetrilehtedel) on palju kirjeldusi.

Kui teil on juurdepääs arenduskeskkonnale, saate lisada uusi väljade kirjeldusi ja kohandada olemasolevaid kirjeldusi. Näiteks saate lisada välja kirjeldusele ettevõttepõhist teavet. Lisateavet leiate jaotisest [Välja kirjelduste kohandamine](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Väljakirjelduste vaatamine kasutajaliideses

Välja kirjelduse vaatamiseks liikuge välja kohale. Kui kirjeldus puudub, näete välja kohale liikudes välja nime.

> [!NOTE]
> Dynamics AX-i versioonis 7.0 (veebruar 2016) saab väljakirjeldusi vaadata ainult lehel **Väljade kirjeldused**.

Järgmisel joonisel on näha väljakirjeldus, mis kuvatakse, kui liigute välja **Lukusta kaubad inventuuri ajaks** kohale.

[![Väljakirjelduse näide.](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Kasutage lehte Väljade kirjeldused väljaspikri vaatamiseks ja eksportimiseks

Leht **Väljade kirjeldused** võimaldab väljade kirjeldusi vaadata ja eksportida. Saate korraga vaadata ühe lehe jaoks saadaolevaid kirjeldusi.

### <a name="view-the-descriptions-for-a-page"></a>Vaadake lehe kirjeldusi

Lehe kirjelduste vaatamiseks tehke järgmist.

- Sisestage väljale **Lehe valimine** lehe nimi. Teise võimalusena klõpsake noolt kõigi lehtede loendi avamiseks ja seejärel sirvige või filtreerige loendit.

Saate kasutada kasutajaliideses kuvatavat lehe nime (nt **Kliendid**) või lehe koodnime (AOT-nime), mis on kättesaadav lehele paremklõpsates (nt **CustTable**).

Teavet mitmesuguste võimaluste kohta lehtede loendi filtreerimiseks leiate selle artikli edasisest osast „Lehe otsimine”.

Kui määrate valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**, kuvatakse kõik lehe väljad, olenemata sellest, kas neil on kirjeldus.

### <a name="export-the-descriptions-for-a-page"></a>Ekspordi lehe kirjeldused

Kirjelduste eksportimiseks tehke järgmist.

1. Valige leht väljalt **Lehe valimine**.
2. Klõpsake paremas ülanurgas nuppu **Ava Microsoft Office’is** ja siis klõpsake suvandit **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Lehe otsimine

Lehe otsimiseks väljal **Lehe valimine** on mitu võimalust. Paljudel juhtudel tuleb klõpsata noolt väljal **Lehe valimine**, et avada ripploend ja valida siis filtreeritud lehtede loendist.

- Sisestage nime osa ning avage siis ripploend, et filtreeritud lehtede loendist valida.
- Avage ripploend ja klõpsake siis pealkirja **Lehe nimi** loendi ülaosas või pealkirja **Lehe AOT-nimi**. Avaneb dialoogiboks, kus saate kasutada täpsema filtreerimise valikuid, nt **Lehe nimi algab tähega**.
- Sisestage lehe täisnimi Selle valiku kasutamisel tasub avada ripploend ja vaadata, mida see veel sisaldab, ka siis, kui väljade kirjeldused on nähtavad.

    - Kui nimele on üks täpne vaste, näidatakse selle lehe väljade kirjeldusi.
    - Kui on mitu täpset vastet, ei kuvata ühtegi kirjeldust. Peate ripploendi avama ja valima soovitud lehe.
    - Kui sisestatud lehe nimi on osa teise lehe nimest, näete oma lehe kirjeldusi. Kuid kui avate ripploendi, siis näete veel lehti, mis seda nime sisaldavad.

Näiteks ei kuvata ühtegi kirjeldust, kui sisestate sõna **Inventuur** väljale **Lehe valimine**. Avate ripploendi ja näete, et on olemas kaks lehte nimega **Inventuur** ja mitu lehte, mille nimes on sõna „inventuur”. Kui valite lehe, mille AOT-nimi on **InventJournalCount**, kuvatakse selle lehe väljade kirjeldused. Kui aga ripploendi uuesti avate, näete, et loend sisaldab nüüd kõiki lehti, mille AOT-nime osa on „InventJournalCount”.

## <a name="troubleshooting"></a>Tõrkeotsing

Selles jaotises on teave, mis on abiks veaotsingul probleemide osas, millega võite väljade kirjelduste kasutamisel kokku puutuda.

### <a name="i-cant-find-a-field-description"></a>Ma ei leia välja kirjeldust

Praegu on käimas kirjelduste lisamise toiming keerulisematele väljadele. Kui vajate konkreetse välja kohta spikrit, andke meile teada, lisades kommentaari selle artikli kohta.

### <a name="the-field-description-isnt-helpful"></a>Välja kirjeldusest ei ole abi

Andke meile teada, lisades sellele artiklile kommentaari. Võimaluse korral kirjeldage lisateavet, mida vajate.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Ma ei leia lehelt Väljade kirjeldused välja.

Kõigi väljade kuvamiseks lehel määrake valiku **Kaasa ilma kirjelduseta väljad** väärtuseks **Jah**. Klõpsake välja **Lehe valimine** kontrollimiseks, kas olete õige lehe valinud. Kui sisestatud nimi on osa teise välja nimest, siis valisite võib-olla lehe, millel on pikem nimi.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Ma ei leia lehelt Väljade kirjeldused lehte.

Teavet mitmesuguste võimaluste kohta lehtede otsimiseks leiate selle artikli varasemast osast „Lehtede otsimine”. Kui sisestasite lehe täpse nime, ei pruugi väljade kirjeldusi näha olla, kui sama nimi on mitmel lehel. Klõpsake noolt väljal **Lehe valimine**, et avada saadaolevate lehtede filtreeritud loend.

## <a name="additional-resources"></a>Lisaressursid

[Välja kirjelduste kohandamine](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
