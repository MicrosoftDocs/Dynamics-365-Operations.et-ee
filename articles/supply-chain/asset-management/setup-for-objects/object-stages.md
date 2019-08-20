---
title: Toote elutsükli olekud
description: Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses.
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
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783199"
---
# <a name="asset-lifecycle-states"></a>Toote elutsükli olekud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses. Vara elutsükli olekuid kasutatakse määratlemaks, kas vara on aktiivne või passiivne. Näiteks saate seadistada vara elutsükli olekud, näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**.

> [!NOTE]
> - Taotluse elutsükli olekud on seotud vara elutsükli olekuga. Seega, kui taotlus on muudetud uue taotluse elutsükli olekusse, muudetakse taotlusele lisatud vara uue vara elutsükli olekusse. Näiteks kui taotluse elutsükli olek muudetakse **Sissetulevaks**, muudetakse manustatud vara elutsükli olekut elutsükli olekusse, mis valitakse väljal **Sissetulev elutsükli olek** kiirkaardil **Vara elutsüklo olek** lehel **Vara elutsükli oleku mudelid**. 


Vara elutsükli olekuid saab seadistada vara elutsükli mudelites, kus saate määratleda nõutavad elutsükli olekud eri liiki varade jaoks. Esmalt seadistage elutsükli olekud. Seejärel looge elutsükli mudel ja valige selle jaoks elutsükli olekud.

1. Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli olekud**.
2. Valige uue vara elutsükli oleku loomiseks **Uus**.
3. Sisestage väljale **Elutsükli olek** elutsükli oleku ID.
4. Väljale **Nimi** sisestage kirjeldus.

    Väljal **Elutsükli mudelid** kuvatakse vara elutsükli olekut kasutavate varade elutsükli mudelite arv.

5. Määrake suvandi **Aktiivne** väärtuseks **Jah**, kui see elutsükli olek peaks olema aktiivne elutsükli olek (teisisõnu, kui töökäske saab luua selle elutsükli olekus olevate varade puhul).
6. Seadke suvandi **Kustuta avatud kalendriread** väärtuseks **Jah**, kui avatud vara kalendriread, millel on vara elutsükli olek **Loodud**, tuleks kustutada, kui need on selles elutsükli olekus. See säte on kasulik, kui soovite puhastada kõik avatud hooldusajakavad, mis pole vara puhul enam asjakohased (näiteks kui vara pole enam aktiivne).

> [!NOTE]
> Vara elutsükli olekud, vara elutsükli mudelid ja vara tüübid on seotud. Neid kasutatakse samamoodi nagu töökäsu elutsükli olekuid, töökäsu elutsükli mudeleid ja töökäsu tüüpe. 


Pärast nõutavate vara elutsükli mudelite loomist saate seadistada elutsükli olekud vara elutsükli mudelites.

1. Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli mudelid**.
2. Valige uue vara elutsükli mudeli loomiseks **Uus**.
3. Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.
4. Väljale **Nimi** sisestage kirjeldus.

    Väljal **Elutsükli olekud** kuvatakse vara elutsükli mudelit kasutavate varade elutsükli olekut arv. Väljal **Vara tüübid** kuvatakse elutsükli mudelit kasutavate vara tüüpide arv.

5. Kiirkaardil **Elutsükli olekud**, valige need vara elutsükli olekud, mis peaksid olema kaasatud vara elutsükli mudelis.

    - Mudeli elutsükli oleku kasutamiseks valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige nupp ![paremnool,](media/15-setup-for-objects.png) et teisaldada see jaotisesse **Valitud elutsükli olekud**.
    - Et kasutada kõiki mudeli saadaolevaid elutsükli olekuid, valige nupp **Kõik saadaolevad elutsükli olekud** ![Kõik saadaolevad elutsükli olekud](media/20-setup-for-objects.png). Kõik elutsükli olekud viiakse üle jaotisesse **Valitud elutsükli olekud**.
    - Elutsükli oleku eemaldamiseks mudelist, valige see jaotises **Valitud elutsükli mudelid** ja seejärel valige nupp ![vasaknool,](media/16-setup-for-objects.png) et teisaldada see jaotisesse **Järelejäänud elutsükli olekud**.

6. Valige **Elutsükli oleku värskendused**, et määratleda, millised elutsükli olekud saavad valitud elutsükli olekut järgida.
7. Kasutage kiirkaarti **Vara olek**, kui käsitlete remondiks saadud varasid. Jaotises **Sissetulev/väljaminev** saate valida vara elutsükli olekud, et näidata vara töövoogu, mille olete paranduseks saanud. Kui pakute klientidele või osakondadele laenuvarasid, saate jaotises **Laen** valida laenuvaradele elutsükli olekud.
