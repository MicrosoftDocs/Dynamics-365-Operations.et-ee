---
title: Hankekataloogi loomine
description: See artikkel selgitab, kuidas luua hankekataloogi.
author: GalynaFedorova
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e35e8c5b5c93fa9aac914f04e7ea658748cb052
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869542"
---
# <a name="create-a-procurement-catalog"></a>Hankekataloogi loomine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas luua hankekataloogi. Seda ülesannet täidab tavaliselt hankespetsialist. Samuti saate teada, kuidas töötajad saavad kataloogi ostutellimuse loomisel kasutada. Enne kataloogi loomist peab teie süsteemis olema hankekategooria hierarhia. Uus kataloog pärib hierarhia koos kõigi hierarhias olevate toodetega. Saate kasutada seda juhendit demoandmete ettevõttes USMF, kus on saadaval hankekategooria hierarhia ja näited, mida protseduuri toimingutes kasutatakse.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Veenduge, et hankekategooria hierarhia on olemas
1. Avage **Navigeerimispaan > Moodulid > Hanked > Hanke kategooriad**. Demoandmete ettevõttes USMF on saadaval hanke kategooriahierarhia ja tooted on lisatud kategooriasse **Kontoriseadmed/arvutid**. Kui käitate seda protseduuri ülesandejuhendina, tuleb juhend lukust avada, kui soovite kategoorias sirvida. Kui hierarhiat polnud saadaval, tuleb see luua, klõpsates valikut **Uus**. Seda saab teha ainult ühe korra.  
2. Sulgege leht.

## <a name="create-a-catalog"></a>Kataloogi loomine
1. Avage **Navigeerimispaan > Moodulid > Hanked > Kataloogid > Hankekataloogid**.
2. Rippdialoogi avamiseks klõpsake valikut **Uus hankekataloog**.
3. Sisestage väärtus väljale **Nimi**.
4. Valige nupp **OK**.
5. Laiendage puul valikut **ETTEVÕTTE HANKEKATEGOORIAD**.
6. Laiendage puul valikut **KONTORSEADMED**.
7. Valige puult **Arvutid**.

  - Hankekategooria tooted kuvatakse loendis. Kui soovite lisada toote kategooriasse, tuleb seda teha lehel **Hankekategooria hierarhia** või lehel **Kauba üksikasjad**.  
  - **Vaikimisi** värskendamise tüüp määrab, kas uued tooted, mis on hankekategooria hierarhiasse lisatud, on kataloogis kohe näha. Kui värskenduse tüübiks on määratud **Dünaamiline**, on muudatused kohe näha. Kui värskenduse tüüp on **Staatiline**, on uued tooted kataloogi kasutavatele inimestele nähtavad alles pärast kataloogi uuesti avaldamist. Toiming **Avalda** on saadaval tegumiribal lehe ülaosas. Kui tooteid hankekategooria hierarhiast eemaldatakse, on muudatus kohe näha, olenemata väärtusest väljal **Vaikimisi** värskendamise tüüp.  

8. Valige toimingupaanil **Kategooria navigeerimine** ja veenduge, et suvand **Luba** oleks valitud.
9. Valige **Aktiveeri kataloog**.
10. Sulgege leht.

## <a name="make-the-catalog-visible"></a>Tehke kataloog nähtavaks
1. Avage navigeerimispaanil **Moodulid > Hange > Häälestus > Poliitika > Ostupoliitika**.
2. Valige **Hankepoliitika USMF**. Peate valima ostupoliitika sellele juriidilisele isikule, milles teie kasutajaprofiiliga seotud töötajal on lubatud tooteid tellida. Demoandmete USMF puhul on kasutaja Administraator seotud töötajaga nimega **Julia Funderburk** ja viimane tellib USMF-is vaikimisi tooteid.  
3. Valige äsja loodud kataloog.
4. Valige nupp **OK**.

## <a name="use-the-catalog"></a>Kasutage kataloogi
1. Avage **Navigeerimispaan > Moodulid > Hanked > Ostutaotlused > Kõik ostutaotlused**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. Valige nupp **OK**.
5. Valige **Lisa tooteid**.
6. Otsige loendist ja valige soovitud kirje. Saate kasutada toodete filtreerimiseks vasakul olevat kategooriahierarhiat või ülal olevat filtrit.  
7. Valige **Lisa ridadele**.
8. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]