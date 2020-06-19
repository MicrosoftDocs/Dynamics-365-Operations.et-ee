---
title: Tootesoovituste lisamine kassas
description: See teema kirjeldab toote soovituste kasutamist müügikohas (POS) seadmel.
author: bebeale
manager: AnnBe
ms.date: 05/26/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a1dc1e8934bcd6a8cb94b780bbfe247f64067912
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404252"
---
# <a name="add-product-recommendations-on-pos"></a>Tootesoovituste lisamine kassas

[!include [banner](includes/banner.md)]

Oma sisult on tootesoovitused ümberkujundamise ärirakendus, mis ulatub üle kõik kaubanduse ruumide, et luua rikkaid, kaasavaid ja kohandatud toote avastamise kogemusi. Selle funktsiooni juurutamiseks POS-is järgige juhiseid [soovituste lisamiseks oma POS-seadmetesse.](add-recommendations-control-pos-screen.md) 

Lisateavet toote soovituste funktsioonide kohta leiate [toote soovituste ülevaatest.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Stsenaariumid

Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul. Need on saadaval pilvekassas või Modern POS-is (MPOS).

1. Lehel **Toote üksikasjad** toimub järgmine.

    - Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.

    [![Soovitused lehel Toote üksikasjad](./media/proddetails.png)](./media/proddetails.png)

2. Lehel **Kanne** toimub järgmine.

    - Soovituse mootor pakub kaupu kogu ostukorvis olevate kaupade loendi alusel, mis on sageli koos ostetud.

    > [!NOTE]
    > Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 Commerceis ekraanipaigutust. Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.

    [![Soovitused lehel Kanne](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce’i konfigureerimine kassasoovituste kuvamiseks

Tootesoovituste seadistamiseks läbige need etapid.

1. Veenduge, **et teie teenus on uuendatud 10.0.6 järgule.**
2. Järgige juhiseid, kuidas [lubada toote soovitusi](../commerce/enable-product-recommendations.md) oma ettevõttele.
3. Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus**, valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja** ja paigutage siis **soovituste juhtelement** vajalikku kohta.
4. Avage **Kaubanduse parameetrid**, valige **Masinõpe** ja valige **Jah** jaotises **Luba kassasoovitused**.
5. Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**. Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Tõrkeotsing, kui tootesoovitused on juba lubatud

- Liikuge kohta **Commerce’o parameetrid** \> **Soovituste loendid** \> **Keela tootesoovitused** ja käivitage **Globaalne konfigureerimistöö \[9999\]**. 
- Kui olete oma kandekuvale lisanud **soovituste juhtelemendi**, kasutades **ekraanipaigutuse kujundajat**, eemaldage ka see.
- Kui teil on lisaküsimusi, vaadake teemat [Tootesoovituste KKK](../commerce/faq-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)
