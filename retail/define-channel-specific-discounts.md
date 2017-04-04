---
title: "Kanalipõhiste allahindluste määratlemine"
description: "Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanalipõhiste allahindluste määratlemine

Jaemüüjad määravad tihti erinevates kanalites erinevad allahindlused. Selles teemas antakse ülevaade mõistetest, mida peate teadma kindlale kanalile allahindluse loomiseks. 

<a name="channel-specific-discounts"></a>Kanalipõhised allahindlused
--------------------------

Jaemüüjad pakuvad tihti erinevaid allahindlusi erinevates kanalites. See on mai aadress kohaliku turu tingimustele või konkureerivate jaemüüjate teha.

Hulgi- ja kaubanduse Microsoft Dynamics 365 operatsioonide kasutab Hooldushinnarühmad kanali konkreetse allahindlusi. Hinnagruppe saab määrata vähemalt ühele järgmisele üksusele: kanalid, kataloogid, alluvused ja püsikliendiprogrammid. See artikkel käsitleb kanaleid, kuid samad mõisted kehtivad kataloogi allahindlustele, alluvuste allahindlustele ja püsikliendiallahindlustele.

## <a name="price-groups"></a>Hinnagrupid
\[caption id = "manuse\_256084" viia = "alignnone" width = "640"\][![hind sõprade](./media/price-groups-1024x608.png)](./media/price-groups.png) hind rühma lingid jaemüük\[/caption\]

Joonis illustreerib seost üksused, mida võib tehingu (kanal, kataloog, liitumine, klient, kliendikaart) ja erinevate hinnaalandite liikide, mida saab konfigureerida. Kõik tehingud toimuvad kanalisse, nii, et kanal on tagatud lõppes tehingu. Ülejäänud üksused on valikulised. Igal koondandmete lehel on link seotud hinnagruppide lehele, kus saate vaadata ja lisada vajalikke hinnagruppe. Hinnagrupp kasutatakse nelja tüüpi üksuste seotud allahindlused, tariifide ja kaubanduskokkulepete. Me soovitame, et teil planeerida oma strateegia näidatakse nime oma hind sõprade hoida neid korraldatud. Üks võimalus oleks kasutada tähe või numbri eesliide või sufiks eristada erinevaid. Näiteks 1-xxxxx hind kanalipaketi ja 2-xxxxx kataloogi hind gruppidele. Neli päringulehte keskenduvad igale jaemüügiüksusele, millega on seotud allahindlused.

-   **Jaemüügikanali hinnagrupid **– sellel lehel on loend kanalitest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Kataloogi hinnagrupid **– sellel lehel on loend kataloogidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Püsikliendi hinnagrupid **– sellel lehel on loend püsikliendiprogrammidest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.
-   **Sidusettevõtete hinnagrupid **– sellel lehel on loend sidusettevõtetest ja allahindlustest, mis on iga hinnagrupi puhul seostatud.

## <a name="example-channel-discount-set-up"></a>Kanali allahindluse seadistuse näide
Järgmine näide illustreerib kanali allahindluse seadistamiseks vajalikke toiminguid.

1.  Selles näites on kanal nimega **Houston** ja loote uue allahindluse nimega **Tagasi-kooli.**
2.  Kuna hinnakujunduse ja allahindluste strateegia hõlmab kanali allahindluste võimalust, luuakse kanali loomisel alati kanalipõhine hinnagrupp.
3.  Teil on hinnagrupp **Houston-PG** ja see on määratud kanalile **Houston**.
4.  Pärast uue allahindluse **Tagasi-kooli** loomist tuleb klõpsata valikut **Hinnagrupid** lehe **Allahindlus** ülemises osas. Avaneb leht **Allahindluse hinnagrupid**. Seejärel klõpsake nuppu **Uus** ja valige hinnagrupp **Houston-PG**.
5.  Nüüd saate allahindluse lubada ja kanalisse suunata.

 

<a name="see-also"></a>Vt ka
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


