--- 
title: Hankekataloogi loomine
description: "Selles juhendis näidatakse, kuidas hankekataloogi luua."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 19d053a0bdbdcc764b3361fe5a326e8c68cdc682
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-procurement-catalog"></a>Hankekataloogi loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selles juhendis näidatakse, kuidas hankekataloogi luua. Seda ülesannet täidab tavaliselt hankespetsialist. Samuti saate teada, kuidas töötajad saavad kataloogi ostutellimuse loomisel kasutada. Enne kataloogi loomist peab teie süsteemis olema hankekategooria hierarhia. Uus kataloog pärib hierarhia koos kõigi hierarhias olevate toodetega. Saate kasutada seda juhendit demoandmete ettevõttes USMF, kus on saadaval hankekategooria hierarhia ja näited, mida protseduuri toimingutes kasutatakse.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Veenduge, et hankekategooria hierarhia on olemas
1. Tehke valik Hanked > Hankekategooriad.
    * Demoandmete ettevõttes USMF on saadaval hanke kategooriahierarhia ja tooted on lisatud kategooriasse Kontoriseadmed/arvutid. Kui käitate seda protseduuri ülesandejuhendina, tuleb juhend lukust avada, kui soovite kategoorias sirvida. Kui hierarhiat polnud saadaval, tuleb see luua, klõpsates valikut Uus. Seda saab teha ainult ühe korra.  
2. Sulgege leht.

## <a name="create-a-catalog"></a>Kataloogi loomine
1. Valige Hanked > Kataloogid > Hankekataloogid.
2. Rippdialoogi avamiseks klõpsake valikut Uus hankekataloog.
3. Sisestage väärtus väljale Nimi.
4. Klõpsake nuppu OK.
5. Laiendage puul valikut ETTEV. HANKEKATEGOORIAD.
6. Laiendage puul valikut KONTORSEADMED.
7. Valige puult Arvutid.
    * Hankekategooria tooted kuvatakse loendis. Kui soovite lisada toote kategooriasse, tuleb seda teha lehel Hankekategooria hierarhia või lehel Kauba üksikasjad.  
    * Vaikimisi värskendamise tüüp määrab, kas uued tooted, mis on hankekategooria hierarhiasse lisatud, on kataloogis kohe näha. Kui värskenduse tüübiks on määratud Dünaamiline, on muudatused kohe näha. Kui värskenduse tüüp on Staatiline, on uued tooted kataloogi kasutavatele inimestele nähtavad alles pärast kataloogi uuesti avaldamist. Toiming Avalda on saadaval tegumiribal lehe ülaosas. Kui tooteid hankekategooria hierarhiast eemaldatakse, on muudatus kohe näha, olenemata väärtusest väljal Vaikimisi värskendamise tüüp.  
8. Otsige loendist ja valige soovitud kirje.
9. Klõpsake käsku Peida.
10. Klõpsake toimingupaanil valikut Kategooria navigeerimine.
11. Klõpsake käsku Keela.
12. Klõpsake toimingupaanil valikut Kategooria navigeerimine.
13. Klõpsake käsku Luba.
14. Klõpsake käsku Aktiveeri kataloog.
15. Sulgege leht.

## <a name="make-the-catalog-visible"></a>Tehke kataloog nähtavaks
1. Valige Hanked > Seadistus > Poliitikad > Ostupoliitikad.
2. Valige Hankepoliitika USMF.
    * Peate valima ostupoliitika sellele juriidilisele isikule, milles teie kasutajaprofiiliga seotud töötajal on lubatud tooteid tellida. Demoandmete USMF puhul on kasutaja Administraator seotud töötajaga nimega Julia Funderburk ja viimane tellib USMF-is vaikimisi tooteid.  
3. Klõpsake loendis valitud real olevat linki.
4. Valige äsja loodud kataloog.
5. Klõpsake nuppu OK.
6. Sulgege leht.
7. Sulgege leht.

## <a name="use-the-catalog"></a>Kasutage kataloogi
1. Valige Hanked > Ostutaotlused > Kõik ostutaotlused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Klõpsake nuppu OK.
5. Klõpsake suvandit Lisa tooteid.
6. Otsige loendist ja valige soovitud kirje.
    * Saate kasutada toodete filtreerimiseks vasakul olevat kategooriahierarhiat või ülal olevat filtrit.  
7. Klõpsake suvandit Lisam ridadele.
8. Otsige loendist ja valige soovitud kirje.
9. Klõpsake suvandit Lisam ridadele.
10. Klõpsake nuppu OK.

