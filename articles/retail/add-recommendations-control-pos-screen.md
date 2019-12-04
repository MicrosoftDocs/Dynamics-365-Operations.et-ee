---
title: Soovituste juhtelemendi lisamine kassaseadmete kandekuvale
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili ekraanipaigutuse kujundajat.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811212"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a>Soovituste juhtelemendi lisamine kassaseadmete kandekuvale

[!include [banner](includes/banner.md)]


See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 Retaili ekraanipaigutuse kujundajat. Lisateavet tootesoovituste kohta lugege teemast [Tootesoovitused kassa dokumentatsioonis](product.md).


Saate Microsoft Dynamics 365 Retaili kasutamisel kuvada kassaseadmes tootesoovitusi. Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat. 

## <a name="open-layout-designer"></a>Paigutusekujundaja avamine

1. Minge jaotisse **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.
2. Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada. Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse **F2CP16:9M** järgi.
3. Otsige loendist ja valige soovitud kirje. Valige näiteks **Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M**.
4. Klõpsake valikut **Paigutusekujundaja**.
5. Järgige paigutusekujundaja avamiseks viipasid. Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.
6. Sisselogimisel avaneb alltoodule sarnane leht. Paigutus erineb olenevalt teie poele tehtud kohandustest.


    [![Paigutusekujundaja](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Valige kuvatav valik

Saadaval on kaks konfigureerimisvalikut. Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid. Võimalused on järgmised.

- Soovitused on alati nähtaval.
- Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.

### <a name="make-recommendations-always-visible"></a>Soovituste alati nähtavaks tegemine


1. Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge, kui vasakul asuv kliendipaneel.


    [![Kanderidade üksikasjade ala kõrgust on vähendatud](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele. Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.

    [![Paigutusele on lisatud soovituste juhtelement](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
4. Minge Dynamics 365 for Retailis jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.
5. Valige loendist suvand **1090, registrid**.
6. Klõpsake valikut **Käivita kohe**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Lisage soovituste vahekaart kuva paremas servas olevasse nupuruudustikku

1. Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.

2. Klõpsake **Kohandada**.

    [![Kohandamine – vahekaardi juhtimise dialoogiboks](./media/pic-5.png)](./media/pic-5.png)

3. Klõpsake valikut **Uus vahekaart**.
4. Leidke vastlisatud uus vahekaart. Võib-olla peate selleks allapoole kerima.
5. Valige ripploendist **Sisu** suvand **Soovitatud tooted**.

    [![Soovitatud toodete valimine sisu väljast](./media/pic-6.png)](./media/pic-6.png)

6. Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.
7. Valige väljal **Pilt** vahekaardil kuvatav pilt.
8. Klõpsake valikut **OK**. Uus vahekaart kuvatakse nupuruudustikus.
9. Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
10. Minge Dynamics 365 for Retailis jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.
11. Valige loendist suvand **1090, registrid**.
12. Klõpsake valikut **Käivita kohe**.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovitused kassas](product.md)

[Tootesoovituste ülevaade](../commerce/product-recommendations.md)
