---
title: Kassa rakenduse ja kasutaja keelesätted
description: See artikkel kirjeldab, kuidas muuta keelesätteid Modern POS-s (MPOS) ja Pilve kassas.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288375"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Kassa rakenduse ja kasutaja keelesätted

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas muuta keelesätteid Modern POS-s (MPOS) ja Pilve kassas.

## <a name="overview"></a>Ülevaade
Modern POS (MPOS) ja pilvekassa toetavad keskkondi, kus kaupluse ja kasutaja keelesätted ning tõlked võivad erineda. Näiteks asub kauplus piirkonnas, kus enamik kliente kasutab inglise keelt, kuid mõned töötajad eelistavad prantsuskeelse tõlkega rakendust kasutada.

## <a name="data-language"></a>Andmete keel

Olenemata kasutaja sätetest kasutavad Modern POS ja pilve kassa andmete tõlkimiseks alati kaupluse sätetes määratud keelt. See tagab kõigile kasutajatele ja klientidele sama kogemuse. Andmete näidete hulka kuuluvad:

- Tooted
- atribuudid ja väärtused,
- kategooriate nimed,
- prinditud või meilitsi saadetud kannete sissetulekud,
- makseviiside nimed,
- rea kuvateated.

Kaupluse keelt kasutatakse ka kassa peamises sisselogimisaknas, kuna kasutaja ei ole enne sisselogimist teada. Kui kaupluse keele jaoks pole tõlget saadaval, ennistatakse kassasse ettevõtte keel.

### <a name="configuring-the-stores-language-setting"></a>Kaupluse keelesätte konfigureerimine

Kaupluse keelt saab seadistada lehel **Kauplused** jaotises **Kõik kauplused**, asukohas **Üldine &gt; Regioonisätted &gt; Keel**. Iga kaupluse jaoks keele valimiseks kasutage ripploendit.

## <a name="user-interface-language"></a>Kasutajaliidese keel

Kassa kasutaja keelesäte määrab rakenduse kasutajaliideses kasutatavad tõlked. See hõlmab kõiki silte, menüüsid ja loendeid, mida ei peeta andmeteks. Erandiks on vaid kassa nupupaneelidel kuvatav tekst. Nupupaneelid ei toeta tõlkeid, seega kuvatakse neil alati nupul määratletud tekst. Tõlgitud nuppude toetamiseks tuleb kopeerida ja salvestada eraldi nupupaneelid ning määrata need vastavatele kasutajatele.

### <a name="configuring-the-users-language-setting"></a>Kasutaja keelesätte konfigureerimine

Kassa kasutaja keelt saab seadistada lehel **Töötaja** jaotises **Kõik töötajad"**, valides **Jaemüük ja kaubandus &gt; Keel**. Seda ei seadistata vahekaardil Profiil. Kassa ei kasuta seda sätet. Kui kasutaja keelt ei määrata või määratakse mõni keel, millele ei ole tõlget saadaval, ennistatakse kassas kaupluse keel.

| &nbsp;      | Kasutajaliidese keel                   | Andmete keel (tooted, kviitungi vormingud, rea kuva jne) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Ettevõte** | Vaikimisi                    | Vaikimisi                                                       |
| **Kauplus**   | Tühistab ettevõtte          | Tühistab ettevõtte                                             |
| **Kasutaja**    | Tühistab kaupluse või ettevõtte | Mitte kunagi                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
