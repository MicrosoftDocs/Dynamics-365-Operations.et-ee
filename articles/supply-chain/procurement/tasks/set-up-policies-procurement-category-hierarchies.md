---
title: Hankekategooria hierarhiate poliitikate seadistamine
description: Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 415262fa5e68544ea2a4ae2b6818b83c7efb2fad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243987"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Hankekategooria hierarhiate poliitikate seadistamine

[!include [banner](../../includes/banner.md)]

Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks. Reeglid määratletakse konkreetsele ostupoliitikale. Kategooria juurdepääsureegel juhib seda, millistele hankekategooriatele on töötajatel juurdepääs, kui nad taotluse loovad. Taotluse loomise ajal määratakse rakendatav ostupoliitika ja kategooria juurdepääsureegel juriidilise isiku ja tootmisüksuse põhjal, kuhu töötaja kuulub. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Seda ülesannet täidab tavaliselt ostujuht.


## <a name="find-the-procurement-policy"></a>Hankepoliitika otsimine
1. Avage navigeerimispaanil **Moodulid > Jange > Häälestus > Poliitika > Ostupoliitika**.
2. Klõpsake „Hankepoliitika USMF“ poliitika linki. See on poliitika, millele reegli lisate. See peab olema aktiivne poliitika.  

## <a name="create-a-category-access-rule"></a>Kategooria juurdepääsureegli loomine
1. Laiendage kiirkaarti **Poliitika reeglid**.
2. Valige loendist **Poliitika reegli tüüp** suvand **Kategooria juurdepääsupoliitika reegel**. Kui nupp **Poliitika reegli loomine** on tuhm, tähendab see seda, et aktiivne poliitika reegel on kategooria juurdepääsuks juba olemas. Kontrollige välju **Tõhus** ja **Aegumine**, et tuvastada, kumb see on, ning seejärel valige see ja klõpsake **Poliitika reegli kustutamine**. Kui nupp **Poliitika reegli loomine** on saadaval, ei pea te midagi tegema.  
3. Klõpsake nuppu **Poliitika reegli loomine**.
4. Sisestage kuupäev ja kellaaeg väljale **Jõustumiskuupäev**. Aeg ei tohi kattuda teise juba aktiivse reegliga.  
5. Valige kategooria, millele reegel rakendub. Märkige üles, milline kategooria see on – seda on hiljem vaja. Kategooria valimisel lisatakse loendisse Valitud kategooriad selle põhikategooria või -kategooriad. Kui soovite, et reegel rakenduks kõigile valitud kategooria alamkategooriatele, valige märkeruut **Kaasa alamkategooriad**.
6. Klõpsake paremnoolt, et lisada loend **Valitud kategooriad**.  
4. Klõpsake valikut **OK**. Kui seadistate suvandi **Kaasa ema reegel** olekusse Jah, määratakse emakategooriale määratud poliitika reegel ka selle alamkategooriatele, kui alamkategooriatele ei ole poliitika reeglit määratud.

## <a name="create-a-category-policy-rule"></a>Kategooria poliitikareegli loomine
1. Valige loendist **Poliitika reegli tüüp** suvand **Kategooria poliitika reegel**. Kui nupp **Poliitika reegli loomine** on tuhm, valige aktiivne poliitika reegel ja seejärel klõpsake **Kustuta poliitika reegel**.  
2. Klõpsake nuppu **Poliitika reegli loomine**.
3. Sisestage kuupäev ja kellaaeg väljale **Jõustumiskuupäev**.
4. Klõpsake käsku **Lisa**.
5. Valige väljal **Kategooria** sama kategooria, mida kasutasite **Kategooria juurdepääsu reegli** korral.
6. Valige suvand väljal **Hankia valik**. Valige reegel, et juhtida, milliseid hankijaid võib taotluste loomisel kategooriale valida.  
7. Klõpsake valikut **Sule**. Teie määratletud poliitikareeglid on olnud taotlustele tüübiga Tarbimine. Kui soovite määratleda poliitikad taotlustele tüübiga Täiendamine, tuleb luua reegel poliitikareegli tüübile nimega „Täiendamise kategooria juurdepääsupoliitika reegel”.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]