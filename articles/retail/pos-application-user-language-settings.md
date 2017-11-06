---
title: "Kassa rakenduse ja kasutaja keelesätted"
description: "Selles teemas kirjeldatakse Retail Modern POS-i (MPOS) ja pilve kassa keelesätete muutmist."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

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

Kassa kasutaja keelt saab seadistada lehel **Töötaja** jaotises **Kõik töötajad**, valides **Jaemüük &gt; Keel**.  Seda ei seadistata vahekaardil Profiil. Kassa ei kasuta seda sätet. Kui kasutaja keelt ei määrata või määratakse mõni keel, millele ei ole tõlget saadaval, ennistatakse kassas kaupluse keel.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Kasutajaliidese keel** ** **      | **Andmete keel (tooted, kviitungi vormingud, rea kuva jne)** |
| **Ettevõte** | Vaikimisi                    | Vaikimisi                                                           |
| **Kauplus**   | Tühistab ettevõtte          | Tühistab ettevõtte                                                 |
| **Kasutaja**    | Tühistab kaupluse või ettevõtte | Mitte kunagi                                                             |





