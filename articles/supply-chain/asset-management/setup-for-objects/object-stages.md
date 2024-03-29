---
title: Toote elutsükli olekud
description: See artikkel selgitab vara elutsükli olekuid ja töötsükli mudeleid varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b1ff9438437e6c1ff33bab9a7ba0361029cb6d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901056"
---
# <a name="asset-lifecycle-states"></a>Toote elutsükli olekud

[!include [banner](../../includes/banner.md)]

 

See artikkel selgitab vara elutsükli olekuid ja töötsükli mudeleid varahalduses. Vara elutsükli olekuid kasutatakse määratlemaks, kas vara on aktiivne või passiivne. Näiteks saate seadistada vara elutsükli olekud, näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**.

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

    - Elutsükli oleku lisamiseks lifecycle mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige paremnool ![paremnool.](media/15-setup-for-objects.png) et teisaldada see valitud jaotisesse **Elutsükli valitud olekud**.
    - Et kasutada kõiki mudeli saadaolevaid elutsükli olekuid, valige nupp **Kõik saadaolevad elutsükli olekud** nupp ![Kõik saadaolevad elutsükli olekud.](media/20-setup-for-objects.png). Kõik elutsükli olekud viiakse üle jaotisesse **Valitud elutsükli olekud**.
    - Elutsükli oleku lisamiseks elutsükli mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige vasaknool ![vasaknool.](media/16-setup-for-objects.png) et teisaldada see valitud jaotisesse **Elutsükli järelejäänud olekud**.

6. Valige **Elutsükli oleku värskendused**, et määratleda, millised elutsükli olekud saavad valitud elutsükli olekut järgida.
7. Kasutage kiirkaarti **Vara olek**, kui käsitlete remondiks saadud varasid. Jaotises **Sissetulev/väljaminev** saate valida vara elutsükli olekud, et näidata vara töövoogu, mille olete paranduseks saanud. Kui pakute klientidele või osakondadele laenuvarasid, saate jaotises **Laen** valida laenuvaradele elutsükli olekud.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]