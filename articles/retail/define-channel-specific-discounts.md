---
title: "Kanalipõhiste allahindluste määratlemine"
description: "Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f68400bf10b6235decc7ac5cb82e58b369c7c0c7
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="define-channel-specific-discounts"></a>Kanalipõhiste allahindluste määratlemine

[!include[banner](includes/banner.md)]


Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks. 

<a name="channel-specific-discounts"></a>Kanalipõhised allahindlused
--------------------------

Jaemüüjad pakuvad sageli erinevates kanalites erinevaid allahindlusi. Seda saab teha kohalike turutingimuste arvestamiseks või konkureerivate jaemüüjatega toime tulemiseks.

Microsoft Dynamics 365 for Retail kasutab kanalipõhiste allahindluste määratlemiseks hinnagruppe. Hinnagruppe saab määrata vähemalt ühele järgmisele üksusele: kanalid, kataloogid, alluvused ja püsikliendiprogrammid. See artikkel käsitleb kanaleid, kuid samad mõisted kehtivad kataloogi allahindlustele, alluvuste allahindlustele ja püsikliendiallahindlustele.

## <a name="price-groups"></a>Hinnagrupid

[![Hinnagrupid](./media/price-groups-1024x608.png)](./media/price-groups.png)

Ülalolev joonis illustreerib seost kande võimalike üksuste vahel (kanal, kataloog, alluvus, klient, püsikliendikaart) ja mitmesuguseid allahindluse tüüpe, mida saab konfigureerida. Kõik kanded tehakse kanalis, seega on kanal kindlasti kandel olemas. Ülejäänud üksused on valikulised. Igal koondandmete lehel on link seotud hinnagruppide lehele, kus saate vaadata ja lisada vajalikke hinnagruppe. Hinnagruppi kasutatakse nelja tüüpi üksuste seostamiseks allahindluste, hinna korrigeerimiste ja kaubanduslepetega. Soovitame plaanida strateegia, kuidas hinnagruppe nimetada, et neid korras hoida. Üks võimalus on kasutada ees või järel tähte või numbrit, et erinevaid tüüpe eristada. Näiteks 1-xxxxx kanali hinnagruppide puhul ja 2-xxxxx kataloogi hinnagruppide puhul. Neli päringulehte keskenduvad igale jaemüügiüksusele, millega on seotud allahindlused.

-   **Jaemüügikanali hinnagrupid**– sellel lehel on loend kanalitest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Kataloogi hinnagrupid**– sellel lehel on loend kataloogidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Püsikliendi hinnagrupid**– sellel lehel on loend püsikliendiprogrammidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Sidusettevõtete hinnagrupid**– sellel lehel on loend sidusettevõtetest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.

## <a name="example-channel-discount-set-up"></a>Kanali allahindluse seadistuse näide
Järgmine näide illustreerib kanali allahindluse seadistamiseks vajalikke toiminguid.

1.  Selles näites on kanal nimega **Houston** ja loote uue allahindluse nimega **Tagasi-kooli.**
2.  Kuna hinnakujunduse ja allahindluste strateegia hõlmab kanali allahindluste võimalust, luuakse kanali loomisel alati kanalipõhine hinnagrupp.
3.  Teil on hinnagrupp **Houston-PG** ja see on määratud kanalile **Houston**.
4.  Pärast uue allahindluse **Tagasi-kooli** loomist tuleb klõpsata valikut **Hinnagrupid** lehe **Allahindlus** ülemises osas. Avaneb leht **Allahindluse hinnagrupid**. Seejärel klõpsake nuppu **Uus** ja valige hinnagrupp **Houston-PG**.
5.  Nüüd saate allahindluse lubada ja kanalisse suunata.

 

<a name="see-also"></a>Vt ka
--------

[Hinnakorrigeerimised ja allahindlused](price-adjustments-discounts.md)




