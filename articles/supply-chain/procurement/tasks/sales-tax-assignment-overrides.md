---
title: Käibemaksu määramine ja tühistamised
description: See protseduur näitab, kuidas kaubanduse kanalitele käibemaksugruppe määrata.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc987ba7f0026f011a04a27d00bd3833453514b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675061"
---
# <a name="sales-tax-assignment-and-overrides"></a>Käibemaksu määramine ja tühistamised

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas kaubanduse kanalitele käibemaksugruppe määrata. Samuti näitab see uue käibemaksu tühistamise loomise protsessi ja selle määramist olemasolevale käibemaksu tühistamise grupile. Protseduur kasutab demoettevõtte USRT andmeid.

1. Minge jaotisse Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused.
2. Klõpsake loendis kanali ID linki „Houston”.
3. Klõpsake nuppu Redigeeri.
    * Väljal Käibemaksugrupp on praeguse ettevõtte käibemaksugruppide loend. Praegu määratud grupp on üldine käibemaksugrupp Texas. On ka käibemaksugrupid "Washington" ja "Washington, Kingi maakond." Käibemaksugruppidesse saate kaasata mitme omavalitsuse asjakohased maksud.  
    * Väljal Käibemaksu tühistamine saab käibemaksu tühistamise gruppe kanaliga vastendada. Käibemaksu tühistamise gruppe saab kasutada mitme kaupluse puhul toimivate käibemaksu tühistamiste grupeerimiseks. Selle asemel, et määrata käibemaksu tühistamisi ükshaaval, saab luua grupi ja määrata selle aja säästmiseks otse kanalitele.  
4. Klõpsake nuppu Salvesta.
5. Sulgege leht.
6. Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamised.
7. Klõpsake valikut Uus.
8. Sisestage väljale Käibemaksu tühistamine oma uue tühistamise nimi.
9. Sisestage tühistamise kirjeldus väljale Kirjeldus.
10. Määrake olekuks Luba.
11. Laiendage või ahendage jaotist Tühistamine.
12. Valige suvand väljalt Tüüp.
    * Kauba käibemaksugruppe saab kasutada konkreetsete gruppi kuuluvate kaupade maksude alistamiseks. Näiteks toidukaupu maksustatakse tavaliselt tarbekaupadest erinevalt ja neil on tõenäoliselt oma käibemaksugrupp. Käibemaksugrupid on konkreetsele kanalile rakendatavad maksude grupid. Näiteks kui kanal teeb nii jaemüüki kui ka ettevõtetevahelist müüki, võidakse kasutada erinevaid kaupade käibemaksugruppe. Kõik kohaldatavad maksud vastendatakse käibemaksugrupiga.  
    * Nüüd saate teha käibemaksu tühistamise loomiseks maksude kohta valikuid Algväärtus ja Sihtväärtus või Maksugrupist ja Maksugrupiks. Väli Algväärtus tähistab tühistatavat maksu või maksugruppi. Kauba käibemaksugrupi järgi tühistamine annab teistsuguseid valikuid kui käibemaksugrupi järgi tühistamine. Käibemaksu tühistamised saab seadistada nii, et maksud tühistatakse kõigil kannetel või konkreetsetel kande ridadel.  
13. Klõpsake nuppu Salvesta.
14. Sulgege leht.
15. Avage Jaemüük ja kaubandus > Kanali seadistus > Käibemaksud > Käibemaksu tühistamise grupid.
    * Selles etapis määrate äsja loodud käibemaksu alistamise Houstoni kanalile määratud käibemaksu alistamise grupile.  
16. Klõpsake nuppu Redigeeri.
17. Laiendage või ahendage jaotist Häälestus.
18. Klõpsake vahekaarti Lisa.
19. Klõpsake väljal Käibemaksu tühistamine otsingu avamiseks ripploendi nuppu.
20. Valige loendist eelnevalt loodud käibemaksu tühistamine.
21. Klõpsake loendis valitud real olevat linki.
22. Klõpsake nuppu Salvesta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]