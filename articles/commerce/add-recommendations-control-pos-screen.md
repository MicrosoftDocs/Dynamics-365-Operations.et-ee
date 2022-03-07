---
title: Soovituste lisamine kandeekraanile
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 Commercei ekraanipaigutuse kujundajat.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af76169455cef16467b1faa9eda92a969aa923e85750cf245b0a6bd071a092e8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731003"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Soovituste lisamine kandeekraanile

[!include [banner](includes/banner.md)]


See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 Commercei ekraanipaigutuse kujundajat. Lisateavet tootesoovituste kohta lugege teemast [Tootesoovitused kassa dokumentatsioonis](product.md).


Saate Commerce'i kasutamisel kuvada kassaseadmes tootesoovitusi. Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat. 

## <a name="open-layout-designer"></a>Paigutusekujundaja avamine

1. Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.
2. Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada. Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse **F2CP16:9M** järgi.
3. Otsige loendist ja valige soovitud kirje. Valige näiteks **Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M**.
4. Klõpsake valikut **Paigutusekujundaja**.
5. Järgige paigutusekujundaja avamiseks viipasid. Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.
6. Sisselogimisel avaneb alltoodule sarnane leht. Paigutus erineb olenevalt teie poele tehtud kohandustest.


    [![Paigutusekujundaja.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Valige kuvatav valik

Saadaval on kaks konfigureerimisvalikut. Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid. Võimalused on järgmised.

- Soovitused on alati nähtaval.
- Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.

### <a name="make-recommendations-always-visible"></a>Soovituste alati nähtavaks tegemine


1. Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge, kui vasakul asuv kliendipaneel.


    [![Kanderidade üksikasjade ala kõrgust on vähendatud.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele. Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.

    [![Paigutusele on lisatud soovituste juhtelement.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
4. Avage Commerce'is **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafikud**.
5. Valige loendist suvand **1090, registrid**.
6. Klõpsake valikut **Käivita kohe**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lisage soovituste vahekaart kuva paremas servas olevasse nupuruudustikku

1. Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.

2. Klõpsake **Kohandada**.

    [![Kohandamine – vahekaardi juhtimise dialoogiboks.](./media/pic-5.png)](./media/pic-5.png)

3. Klõpsake valikut **Uus vahekaart**.
4. Leidke vastlisatud uus vahekaart. Võib-olla peate selleks allapoole kerima.
5. Valige ripploendist **Sisu** suvand **Soovitatud tooted**.

    [![Soovitatud toodete valimine sisu väljast.](./media/pic-6.png)](./media/pic-6.png)

6. Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.
7. Valige väljal **Pilt** vahekaardil kuvatav pilt.
8. Klõpsake valikut **OK**. Uus vahekaart kuvatakse nupuruudustikus.
9. Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
10. Avage Commerce'is **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafikud**.
11. Valige loendist suvand **1090, registrid**.
12. Klõpsake valikut **Käivita kohe**.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]