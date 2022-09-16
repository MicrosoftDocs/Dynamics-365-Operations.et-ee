---
title: Tootesoovituste lisamine kassas
description: See artikkel kirjeldab tootesoovituste kasutamist müügikoha (POS) seadmes.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460052"
---
# <a name="add-product-recommendations-on-pos"></a>Tootesoovituste lisamine kassas

[!include [banner](includes/banner.md)]

Oma sisult on tootesoovitused ümberkujundamise ärirakendus, mis ulatub üle kõik kaubanduse ruumide, et luua rikkaid, kaasavaid ja kohandatud toote avastamise kogemusi. Selle funktsiooni juurutamiseks POS-is järgige juhiseid [soovituste lisamiseks oma POS-seadmetesse.](add-recommendations-control-pos-screen.md) 

Lisateavet toote soovituste funktsioonide kohta leiate [toote soovituste ülevaatest.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Stsenaariumid

Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul. Need on saadaval pilvekassas või Modern POS-is (MPOS).

1. Lehel **Toote üksikasjad** toimub järgmine.

    - Kui kaupluse seostamine külastab **toote** üksikasjade lehte, kui ta otsib erinevaid kanaleid eelmistest kannetest, soovitab soovituste teenus lisaüksusi, mida tõenäoliselt koos ostetakse. Sõltuvalt teenuse lisandmoodulitest saavad jaemüüjad kuvada oste sarnase välja näeb ja osta toodete kohta sarnaseid kirjelduse soovitusi, lisaks isikupärastatud soovitustele kasutajatele, kellel **on** **eelmine** ostuajalugu.

    [![Soovitused lehel Toote üksikasjad.](./media/proddetails.png)](./media/proddetails.png)

2. Lehel **Kanne** toimub järgmine.

    - Soovituse mootor pakub kaupu kogu ostukorvis olevate kaupade loendi alusel, mis on sageli koos ostetud.

    > [!NOTE]
    > Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 Commerceis ekraanipaigutust. Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.

    [![Soovitused lehel Kande lehel.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce’i konfigureerimine kassasoovituste kuvamiseks 

Tootesoovituste häälestamiseks kinnitage, et olete commerce’i tootesoovituste jaoks lõpule viinud, järgides jaotises Luba tootesoovitused [toodud etappe](../commerce/enable-product-recommendations.md). Vaikimisi ilmuvad soovitused nii toote **üksikasjade** **lehel kui ka kliendi üksikasjade lehel pärast seda, kui olete läbinud sätted ja andmed on** edukalt läbinud. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Soovituste lisamine kandeekraanile

1. Soovituste lisamiseks kande kuvale järgige kande ekraanile [soovituste lisamise samme](add-recommendations-control-pos-screen.md).
1. Kassa ekraani paigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfiguratsioonitöö **1070 rakenduses** Commerce Headquarters.

> [!NOTE] 
> Kui soovite lubada müügikoha soovitused, kasutades RecoM csv-faili, peate enne paigutusehalduri konfigureerimist juurutama CSV-faili Microsoft Dynamics elutsükli teenuste (LCS) varateeki. Kui kasutate RecoM csv-faili, ei pea te soovitusi lubama. CSV-fail on saadaval ainult demo eesmärgil. See on soovitatav klientidele või lahenduse arhitektidele, kes soovivad soovitamisloendite ilmet demo eesmärgil kasutada ilma lisa varudearvestusühikut (SKU) ostmata.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
