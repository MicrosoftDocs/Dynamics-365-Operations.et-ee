--- 
title: Hankekategooria hierarhia seadistamine
description: "See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: et-ee
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Hankekategooria hierarhia seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat. Neid ülesandeid täidab üldjuhul ostujuht. Enne, kui saate selle protseduuri käivitada, peab teil olema kategooriahierarhia, mille tüüp on Hange. Demoettevõtte kasutamisel saate seda protseduuri käitada ettevõttes USMF.


## <a name="add-a-new-procurement-category"></a>Uue hankekategooria lisamine
1. Tehke valik Hanked > Hankekategooriad.
2. Klõpsake suvandit Kategooriahierarhia redigeerimine.
    * Lehe vasakus servas kuvatakse praegune hankekategooria hierarhia. Hakkate seda hierarhiat muutma.  
3. Klõpsake suvandit Uus kategooriasõlm.
    * Süsteem valib vaikimisi ülemise sõlme. Kui käitate seda protseduuri ülesandejuhendina, saate klõpsata nuppu Ava ja valida teise ülataseme sõlme, millesse oma uus sõlm lisada. Kui see on tehtud, lukustage uuesti ülesandejuhend ja klõpsake sõlme Uus kategooria.  
4. Sisestage väärtus väljale Nimi.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Sisestage väärtus väljale Hüüdnimi.
    * Hüüdnimi on valikuline. See kuvatakse kategooriaotsingutes koos kategooria nimega.  
7. Klõpsake nuppu Salvesta.

## <a name="add-products-to-your-new-procurement-category"></a>Toodete lisamine uude hankekategooriasse
1. Tehke valik Hanked > Hankekategooriad.
    * Valige äsjalisatud sõlm. Kui käitate seda protseduuri ülesandejuhendina, peate sõlme valimiseks võib-olla ülesandejuhendi avama.  
2. Laiendage jaotist Tooted.
3. Klõpsake suvandit Lisa, et seostada tooted hankekategooriaga.
4. Valige toode, mille soovite lisada hankekategooriasse.
5. Klõpsake toote valimiseks noolt.
6. Valige teine toode, mille soovite lisada hankekategooriasse.
7. Klõpsake toote valimiseks noolt.
8. Klõpsake nuppu OK.

## <a name="add-approved-and-preferred-vendors"></a>Kinnitatud ja eelistatud hankijate lisamine
1. Lülitage jaotise Hankijad laiendamist.
2. Klõpsake vahekaarti Lisa.
    * Saate lisada hankekategooriasse hankija ja määrata, kas hankija on eelistatud või kategooria jaoks lihtsalt kinnitatud. Kui kustutate hankija kategooriast, ei kustutata kategooriast hankija ajaloolisi kandeid.   
3. Leidke hankija, kelle soovite lisada hankekategooriasse.
4. Klõpsake hankija valimiseks noolt.
5. Klõpsake nuppu OK.
6. Valige selle hankija rida, keda soovite muuta.
7. Valige suvand väljal Hankija olek.
    * Hankija valimise säte suvandis Kategooria poliitika reegel määrab, kas ostutaotlusel on saadaval eelistatud hankija, kinnitatud hankija või kõik hankijad.   

## <a name="add-additional-information-to-the-category"></a>Kategooriale lisateabe lisamine
1. Laiendage jaotist Hankija hindamiskriteeriumigrupid.
    * Sellel vahekaardil saate määratleda, millise kriteeriumi järgi tuleks hankekategoorias olevaid hankijaid hinnata. Selleks klõpsake suvandit Lisa ja seejärel valige soovitud kriteeriumit sisaldav hankija hindamise grupp.  
2. Laiendage jaotist Küsimustikud.
    * Sellel vahekaardil saate lisada küsimustikke, mis kuvatakse tellimusel, kui määrate suvandi Tegevuse tüüp sätteks Tellimus. Sel juhul peab tellija enne hankekategooriasse kuuluva kindla toote või toodete tellimuse esitamist täitma küsimustiku.  
3. Laiendage jaotist Kauba käibemaksugrupid.
4. Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.
5. Saate valida käibemaksugrupi.
6. Laiendage jaotist Kategooria leht.
    * Kategooria lehed luuakse lehel Kategooria hierarhia. Need sisaldavad teavet hankekategooria kohta, näiteks kategoorias olevate toodete tüüp, kategoorias olevate toodete pildid või teated, näiteks kategoorias saadaolevad allahindlused. Kategooria lehel olev teave kuvatakse ostutaotlustel.  
7. Sulgege leht.


