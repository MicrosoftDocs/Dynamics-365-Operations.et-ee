---
title: Tootesoovitused müügikohas
description: See teema kirjeldab toote soovituste kasutamist müügikohas (POS) seadmel.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: af0273ca1553d5fb371a20b8c96fd9a101f34815
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022303"
---
# <a name="product-recommendations-on-pos"></a>Tootesoovitused kassas

[!include [banner](includes/banner.md)]

Oma sisult on tootesoovitused ümberkujundamise ärirakendus, mis ulatub üle kõik jaemüügi ruumide, et luua rikkaid, kaasavaid ja kohandatud toote avastamise kogemusi. Selle funktsiooni juurutamiseks POS-is järgige juhiseid [soovituste lisamiseks oma POS-seadmetesse.](add-recommendations-control-pos-screen.md) 

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

[Soovituste juhtelemendi lisamine kassaseadmete kandekuvale](add-recommendations-control-pos-screen.md)

[Tootesoovituste ülevaade](../commerce/product-recommendations.md)

[Tootesoovituste lubamine](../commerce/enable-product-recommendations.md) 
