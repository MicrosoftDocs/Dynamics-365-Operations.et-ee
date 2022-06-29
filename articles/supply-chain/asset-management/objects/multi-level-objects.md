---
title: Mitmetasandiline vara
description: See artikkel selgitab, kuidas luua ja kustutada mitmetasemelised varad.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b13db8b8b12aaef2e067f9a55eb8754333eb16b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017141"
---
# <a name="multi-level-assets"></a>Mitmetasandiline vara

[!include [banner](../../includes/banner.md)]

 

See artikkel selgitab, kuidas luua ja kustutada mitmetasemelised varad. Hierarhilises puustruktuuris saate luua varasid ja seotud allvarasid. Sel viisil saate kuvada varade vahelisi suhteid ja sõltuvusi. Hooldustöid saab seostada kõigil puustruktuuri tasemetel. Statistikat saab luua ka üksiku taseme või kõigi alamvarade tasemete summana.

Loendilehel **Kõik** varad (**Asset management** \> **Assets All** \> **assets)** **loetleb põhivarad** hierarhilises järjestuses. **Emaveerg** näitab seostuvat vanemat. Lisaks, kui varad ja allvarad on juba loodud kuvatakse jaotise **Vara puu** paanil **Seotud teave** varad puustruktuuris.

Teabe saamiseks vara loomise kohta vt teemat [Vara loomine](../objects/create-an-object.md). Alamvara loomiseks valige emavara väli **Ema** kiirkaardil **Üldine**.

## <a name="copy-an-asset-or-asset-structure"></a>Vara või vara struktuuri kopeerimine

Kui teie ettevõttel on mitu sarnast varade struktuuri, saate nende kiireks loomiseks kasutada funktsiooni Kopeeri varahalduses.

1. Valige **Varahaldus** \> **Varad Kõik** \> **varad.**
2. Leheloendis **Kõik varad** valige kopeeritav vara. Näiteks kui soovite kopeerida kogu vara struktuuri (sh alamvarasid), valige emavara.
3. Valige **Kopeeri vara**. Jaotises **Kopeeri asukohast** on välja **Vara** väärtuseks sätestatud vara, mille valisite loendilehelt.
4. Jaotise **Kopeeri asukohta** väljale **Vara** sisestage uue vara nimi.
5. Kui loodava vara väärtus peaks olema osa olemasolevast varastruktuurist valige jaotise **Emavara** välja **Vara** jaoks emavara ID.
6. Valige nupp **OK**. Uus varade struktuur kuvatakse loendilehel **Kõik varad**. Kõik kopeeritud varaga seotud vara atribuudid, hooldusplaanid ja hooldusringid kantakse üle uuele varale või vara struktuurile.

Vara struktuuri kopeerimisel on uue struktuuri alamvaradel kopeeritud alamvaradega sama nimi. Kui kopeerimisprotseduur on lõpule viidud, saate hõlpsalt muuta vara nime ja muid sätteid. Valige loendilehel **Kõik varad** ja seejärel valige nupp **Redigeeri**.

> [!NOTE]
> Vara või vara struktuuri kopeerimisel lähtestatakse uue vara elutsükli olek mis tahes olekusse, mille määratlete varade algse elutsükli olekuna. Funktsionaalne asukoht lähtestatakse vaikimisi funktsionaalsele asukohale.

## <a name="delete-an-asset-or-asset-structure"></a>Vara või vara struktuuri kustutamine

Kui varal on seotud alamvara, saate selle kustutada ainult siis, kui ühegi vara kohta pole registreeritud ühtegi hooldustaotlust, töötellimuse tööd, puuduste registreerimist ega seisundi hindamist.

1. Valige loendilehel **Kõik varad** vara, mida soovite kustutada.
2. Valige **Kustuta**.

> [!NOTE]
> Kui te ei saa seda protseduuri kasutades vara kustutada, on teine viis kustutamise käsitlemiseks luua selleks otstarbeks vara elutsükli olek. Näiteks saate seadistada elutsükli olekuks **Mahakantud** või **Kustutatud** lehel **Vara elutsükli olekud**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]