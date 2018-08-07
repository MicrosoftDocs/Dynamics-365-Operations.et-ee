--- 
title: Hankekategooria hierarhiate poliitikate seadistamine
description: Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks.
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Hankekategooria hierarhiate poliitikate seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks. Reeglid määratletakse konkreetsele ostupoliitikale. Kategooria juurdepääsureegel juhib seda, millistele hankekategooriatele on töötajatel juurdepääs, kui nad taotluse loovad. Taotluse loomise ajal määratakse rakendatav ostupoliitika ja kategooria juurdepääsureegel juriidilise isiku ja tootmisüksuse põhjal, kuhu töötaja kuulub. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Seda ülesannet täidab tavaliselt ostujuht.


## <a name="find-the-procurement-policy"></a>Hankepoliitika otsimine
1. Valige Hanked > Seadistus > Poliitikad > Ostupoliitikad.
2. Klõpsake poliitika Hankepoliitika USMF linki.
    * See on poliitika, millele reegli lisate. See peab olema aktiivne poliitika.  

## <a name="create-a-category-access-rule"></a>Kategooria juurdepääsureegli loomine
1. Valige kategooria juurdepääsupoliitika reegel.
    * Kui nupp Loo poliitikareegel on tuhm, siis on kategooria juurdepääsul juba aktiivne poliitikareegel olemas. Kontrollige jõustumis- ja aegumiskuupäeva välju, et määrata, mis see on, ning seejärel valige see ja klõpsake valikut Määra poliitikareegel aegunuks. Kui nupp Loo poliitikareegel on saadaval, pole midagi vaja teha.  
2. Klõpsake valikut Loo poliitika reegel.
3. Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.
    * Aeg ei tohi kattuda teise juba aktiivse reegliga.  
    * Valige kategooria, millele reegel rakendub. Märkige üles, milline kategooria see on – seda on hiljem vaja. Kategooria valimisel lisatakse loendisse Valitud kategooriad selle põhikategooria või -kategooriad.  
    * Kui soovite, et reegel kehtiks kõigile valitud kategooria alamkategooriatele, märkige ruut Kaasa alamkategooriad.  
4. Klõpsake vahekaarti Lisa.
    * Kui määrate valiku Kaasa põhireegel väärtuseks Jah, määratakse põhireeglile määratletud poliitikareegel ka selle alamkategooriatele, kui alamkategooriatele on poliitikareegel määratletud.  
5. Klõpsake nuppu OK.

## <a name="create-a-category-policy-rule"></a>Kategooria poliitikareegli loomine
1. Valige kategooria poliitikareegel
    * Kui nupp Loo poliitikareegel on tuhm, valige aktiivne poliitikareegel ja klõpsake valikut Määra poliitikareegel aegunuks.  
2. Klõpsake valikut Loo poliitika reegel.
3. Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.
4. Klõpsake vahekaarti Lisa.
5. Valige sama kategooria, mida kasutasite kategooria juurdepääsureegli puhul.
6. Tehke valik väljal Hankija olek.
    * Valige reegel, et juhtida, milliseid hankijaid võib taotluste loomisel kategooriale valida.  
7. Klõpsake valikut Sule.
    * Teie määratletud poliitikareeglid on olnud taotlustele tüübiga Tarbimine. Kui soovite määratleda poliitikad taotlustele tüübiga Täiendamine, tuleb luua reegel poliitikareegli tüübile nimega Täiendamise kategooria juurdepääsupoliitika reegel.  


