---
title: "Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine"
description: "Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kuluarvestuse analüüsi Power BI sisu jaoks turbe seadistamine

[!INCLUDE [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas saate kuluarvestuses juurdepääsutaseme turbe Microsoft Power BI-s reatasemel turbeks muuta. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, millele neil on juurdepääs.

<a name="overview"></a>Ülevaade
--------

**Kuluarvestuse analüüsi** Microsoft Power BI sisu kasutab Power BI reatasemel turvet kasutaja juurdepääsu piiramiseks. Turve põhineb juurdepääsutaseme organisatsioonihierarhial, mis seadistatakse kuluarvestuse parameetrites. **Kuluarvestuse analüüsi** Power BI sisu kohta lisateabe saamiseks vaadake teemat [Kuluarvestuse analüüs Power BI sisu](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Häälestus
Power BI-le juurdepääsutaseme turbe levitamiseks peab Power BI sisu omanik järgima neid juhiseid. **Märkus.** **Kuluarvestuse analüüsi** Power BI sisu avaldav kasutaja muutub automaatselt omanikuks. Ainult omanik saab Power BI-s turvet seadistada. Lisaks ei saa mitte keegi peale omaniku näha **Kuluarvestuse analüüsi** Power BI sisus olevaid andmeid, kuni omanik lisab veebisaidile PowerBI.com teised kasutajad.

1.  Definitsioonifaili avaldamine Power BI-sse.
2.  Logige saidile PowerBI.com sisse.
3.  Leidke **kuluarvestuse analüüsi** Power BI sisu jaoks andmekogum.
4.  Avage turbe leht. 

    ![Turbelehe avamine](./media/CA-picture-1.png)

5.  Roll **Kuluobjekti kontroller** on juba loodud. Lisage teisi liikmeid, kes kuuluvad kuluarvestuse juurdepääsutaseme organisatsioonihierarhiasse. 

    ![Liikmete lisamine](./media/CA-picture-2.png)

Kasutajad, kes lisatakse rollile **Kuluobjekti kontroller**, näevad ainult neid andmeid, mida neil on kuluarvestuse juurdepääsutaseme organisatsioonihierarhia määratluse järgi lubatud näha. **Märkus** Reatasemel turve kehtib rakenduses Microsoft Dynamics 365 for Finance and Operations olevatele paanidele ja aruannetele, mis manustatakse Power BI kaudu.

## <a name="updating-security"></a>Turbe värskendamine
Kui värskendused tehakse kuluarvestuses juurdepääsutasemel turbele ja soovite, et Power BI kajastaks neid värskendusi, peate värskendama kogu kauplust **kuluarvestuse analüüsi** Power BI sisu jaoks. Pärast rakenduse Finance and Operations kaudu üksuse kaupluse uuenduse lõpuleviimist peate uuendama artefaktid saidil PowerBI.com. Üksuse kaupluse värskenduse kohta lisateabe saamiseks vaadake teemat [Üksuse kaupluse värskendamine](power-bi-integration-entity-store.md#update-entity-store). Kui uutele kasutajatele antakse juurdepääs organisatsioonihierarhiale, peab **kuluarvestuse analüüsi** Power BI sisu omanik tegema ka üksuse kaupluse värskenduse. Lisaks peab omanik saidil PowerBI.com lisama rollile **Kuluobjekti kontroller** uusi kasutajaid, et neile rakendataks reatasemel turvet.

## <a name="disabling-security"></a>Turbe keelamine
Eeldame, et teie organisatsioon soovib andmetele juurdepääsu piirata. Kui turbeparameetrid mingil põhjusel kuluaruandluse käitamisel keelatakse, peab omanik Power BI-s rollile **Kuluarvestaja** kasutajaid lisama. Kui muudate turbe lubatud olekust keelatud olekusse, on mõttekas eemaldada kasutajad rollist **Kuluobjekti kontroller**. Ja vastupidi, kui turbe uuesti lubate. Kasutajad saavad mõlemasse rolli kuuluda. Ühine juurdepääs on mõlema rolli liit. **Kuluarvestuse analüüsi** Power BI sisu korral on ühise juurdepääsuga kasutajatel piiramatu andmetele juurdepääs. Kui teie eesmärk on rakendada piiratud juurdepääsu, tuleb kasutajad määrata ainult rollile **Kuluobjekti kontroller**. Need reatasemel turbevärskendused jõustuvad koheselt. Asjassepuutuvad kasutajad peaksid värskendama oma brausereid.

## <a name="additional-resources"></a>Lisaressursid
Power BI reatasemel turbe kohta lisateabe saamiseks vaadake teemat [Turbe haldamine teie Power BI mudelis](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




