---
title: Arvehaldus B2B e-kaubanduse veebisaitide jaoks
description: Selles teemas kirjeldatakse ettevõtete-ettevõtete Microsoft Dynamics 365 Commerce (B2B) e-kaubanduse veebisaitide arvehalduse võimalusi.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c1f0cc6820063a9a87e79fd6df25c7cffc01e228
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312122"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Arvehaldus B2B e-kaubanduse veebisaitide jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse ettevõtete-ettevõtete Microsoft Dynamics 365 Commerce (B2B) e-kaubanduse veebisaitide arvehalduse võimalusi.

B2B-kandeid käitlevad ettevõtted on tavaks aktsepteerida kliendikrediidi tellimusi ja seejärel saata klientidele arve pärast tellimuse täitmist. Maksetingimused on määratud klientidele ja võivad olla mõned allahindlused, et motiveerida kliente maksma õigeaegselt või enne aega. Maksete õigeaegselt laekumise tõenäosuse suurendamiseks lasevad B2B e-äri veebisaidid klientidel vaadata kõiki oma arveid. Klient saab arveid hõlpsasti filtreerida, et vaadata nii makstud, maksmata kui ka osaliselt makstud arveid koos maksetähtaegadega.

![Arvete leht B2B veebisaidil.](../media/ViewInvoices.png)

> [!NOTE]
> Sisse logitud kasutaja saab vaadata ja maksta ainult enda arveid. Kui organisatsioonikonto on **konfigureeritud** arvekonto rippmenüüs rakenduse Commerce Headquarters kliendikirje arve ja tarne kiirkaardil, saab **kasutaja** vaadata ja maksta arveid organisatsiooni konto puhul.

**B2B veebisaidi** arvete lehel saab kasutaja valida maksmata või osaliselt makstud arve ja seejärel valida **maksearve**. Valitud arve lisatakse ostukorvi ja kasutaja saab maksega jätkata. Kasutaja saab seejärel otsustada, kas maksta arve kogusumma või osaline summa. Kasutaja ei saa arvete maksmiseks kasutada ettemaksu makseviisi.

> [!NOTE]
> Arveid saab ostukorvi lisada ainult juhul, kui selles pole praegu kaupu. Vastupidiselt võib kaupu ostukorvi lisada ainult siis, kui selles pole praegu arveid. Microsoft plaanib selle piirangu tulevastes Commerce'i väljalasetes eemaldada.

![Ostukorvi lehekülg B2B veebisaidil.](../media/PayInvoice.png)

**Lehel Arved** saab kasutaja valida ka arve **kõrval** taotluse arve. Sel viisil saab kasutaja taotleda arve üksikasjade saatmist oma registreeritud meiliaadressile.

![Arve taotluse dialoogiboks.](../media/RequestInvoice2.png)

Kui kasutaja on arvet taotlenud, teisaldatakse **taotlus minu konto lehe jaotisse B2B-taotlused** **·**. Seejärel, **kui P-0001** **ja** Sünkrooni tellimused ja kanali taotlused on commerce headquartersis käitatud, käivitatakse arve meiliaadress ja B2B-taotluse olek märgitakse lõpetatuks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
