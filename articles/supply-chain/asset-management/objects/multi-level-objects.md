---
title: Mitmetasandiline vara
description: Selles teemas selgitatakse, kuidas luua ja kustutada mitmetasandilist vara.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f38253317ed8f06318fc501511ca5263a614e20
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783205"
---
# <a name="multi-level-assets"></a>Mitmetasandiline vara

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas luua ja kustutada mitmetasandilist vara. Hierarhilises puustruktuuris saate luua varasid ja seotud allvarasid. Sel viisil saate kuvada varade vahelisi suhteid ja sõltuvusi. Hooldustöid saab seostada kõigil puustruktuuri tasemetel. Statistikat saab luua ka üksiku taseme või kõigi alamvarade tasemete summana.

Loendilehel **Kõik varad** (**Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**), loendab veerg **Vara** varad hierarhilises järjestuses. **Emaveerg** näitab seostuvat vanemat. Lisaks, kui varad ja allvarad on juba loodud kuvatakse jaotise **Vara puu** paanil **Seotud teave** varad puustruktuuris.

Teabe saamiseks vara loomise kohta vt teemat [Vara loomine](../objects/create-an-object.md). Alamvara loomiseks valige emavara väli **Ema** kiirkaardil **Üldine**.

## <a name="copy-an-asset-or-asset-structure"></a>Vara või vara struktuuri kopeerimine

Kui teie ettevõttel on mitu sarnast varade struktuuri, saate nende kiireks loomiseks kasutada funktsiooni Kopeeri varahalduses.

1. Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.
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