---
title: Kirjet TaxTrans ei loodud
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui Kirjet TaxTrans ei looda.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 284fd4047347386b3893684f077a5980f98a6788
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349996"
---
# <a name="taxtrans-record-isnt-generated"></a>Kirjet TaxTrans ei loodud

[!include [banner](../includes/banner.md)]

Kui valite kandele **Sisestatud käibemaks**, kuid **Sisestatud käibemaks** lehel pole maksuridu või puudub maksurida, ei pruugi kirje **TaxTrans** olla loodud.

[![Sisestatud käibemaksuleht, kus pole reaüksusi.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Kontrollige käibemaksu enne kande sisestamist

1. Enne kande sisestamist valige arvutuse kontrollimiseks **Arve sisestamise** lehel **Käibemaks**.

    [![Käibemaksu nupp lehel Arve sisestamine.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Vaadake **Ajutise käibemaksu kannete** lehel arvutuse tulemus üle. Kui maksu ei arvutata, vt [Maksu ei arvutata või maksusumma on null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Leia kirje TaxTrans kõigis sisestatud käibemaksudes

1. Avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksupäringud** > **Sisestatud käibemaks**.
2. Veerupäises **Kviitung** valige filtri sümbol, et leida kirje **TaxTrans**.
3. Kui leiate otsitava käibemaksukirje, kontrollige kuupäeva. Kui kuupäev erineb päevaraamatu päise kuupäevast, looge lisatoe saamiseks Microsofti teenusetaotlus.

    [![Sisestatud käibemaksu leht.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Vigade parandamine üksikasjade kontrolliks

1. Teabe saamiseks selle kohta, kuidas vigasid parandada ja otsustada, kas **TmpTaxWorkTrans** ja **TaxUncommitted** on õigesti loodud, vaadake [TaxTransi välja väärtus on vale](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Kui **TaxTmpWorkTrans** või **TaxUncommitted** on õigesti loodud, lisage katkestuspunkt **TaxPost::SaveAndPost()** ja **Tax::SaveAndPost**, et parandada viga põhjusel, miks **TaxTrans** ei sisestatud.

    [![Koodi lisatud katkestuspunktid.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Lisatud katkestuspunktide tulemused.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine

Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
