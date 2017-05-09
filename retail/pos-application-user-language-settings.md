---
title: "Kassa rakenduse ja kasutaja keelesätted"
description: "Selles teemas kirjeldatakse Retail Modern POS-i (MPOS) ja pilve kassa keelesätete muutmist."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Kassa rakenduse ja kasutaja keelesätted

[!include[banner](includes/banner.md)]


Selles teemas kirjeldatakse Retail Modern POS-i (MPOS) ja pilve kassa keelesätete muutmist.

<a name="overview"></a>Ülevaade
========

Retail Modern POS (MPOS) ja pilve kassa toetavad keskkondi, kus kaupluse ja kasutaja keelesätted ja tõlked võivad erineda. Näiteks asub kauplus piirkonnas, kus enamik kliente kasutab inglise keelt, kuid mõned töötajad eelistavad prantsuskeelse tõlkega rakendust kasutada.

## <a name="data-language"></a>Andmete keel
Olenemata kasutaja sätetest kasutavad Retail Modern POS ja pilve kassa andmete tõlkimiseks kaupluse sätetes määratud keelt. See tagab kõigile kasutajatele ja klientidele sama kogemuse.  Andmete näidete hulka kuuluvad:

-   Tooted
-   atribuudid ja väärtused,
-   kategooriate nimed,
-   prinditud või meilitsi saadetud kannete sissetulekud,
-   makseviiside nimed,
-   rea kuvateated.

Kaupluse keelt kasutatakse ka kassa peamises sisselogimisaknas, kuna kasutaja ei ole enne sisselogimist teada. Kui kaupluse keele jaoks pole tõlget saadaval, ennistatakse kassasse ettevõtte keel.

### <a name="configuring-the-stores-language-setting"></a>Kaupluse keelesätte konfigureerimine

Kaupluse keelt saab seadistada lehel **Jaekauplus** jaotises **Kõik jaekauplused**, valides **Üldine &gt; Regioonisätted &gt; Keel. **Iga kaupluste jaoks keele valimiseks kasutage rippmenüüd.

## <a name="user-interface-language"></a>Kasutajaliidese keel
Kassa kasutaja keelesäte määrab rakenduse kasutajaliideses kasutatavad tõlked. See hõlmab kõiki silte, menüüsid ja loendeid, mida ei peeta andmeteks. Erandiks on vaid kassa nupupaneelidel kuvatav tekst. Nupupaneelid ei toeta tõlkeid, seega kuvatakse neil alati nupul määratletud tekst. Tõlgitud nuppude toetamiseks tuleb kopeerida ja salvestada eraldi nupupaneelid ning määrata need vastavatele kasutajatele.

### <a name="configuring-the-users-language-setting"></a>Kasutaja keelesätte konfigureerimine

Kassa kasutaja keelt saab seadistada lehel **Töötaja** jaotises **Kõik töötajad**, valides **Jaemüük &gt; Keel**.  Seda ei seadistata peamisel vahekaardil Profiil.  Kassa ei kasuta seda sätet. Kui kasutaja keelt ei määrata või määratakse mõni keel, millele ei ole tõlget saadaval, ennistatakse kassas kaupluse keel.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Kasutajaliidese keel** ** **      | **Andmete keel (tooted, kviitungi vormingud, rea kuva jne)** |
| **Ettevõte** | Vaikimisi                    | Vaikimisi                                                           |
| **Kauplus**   | Tühistab ettevõtte          | Tühistab ettevõtte                                                 |
| **Kasutaja**    | Tühistab kaupluse või ettevõtte | Mitte kunagi                                                             |





