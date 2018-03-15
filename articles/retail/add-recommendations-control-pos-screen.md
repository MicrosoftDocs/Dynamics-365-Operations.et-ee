---
title: Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: b99d1d30fc320bca5c49921b7c4ccdd7e977f67c
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele

[!include[banner](includes/banner.md)]

> [!NOTE]
> Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame. Lisateavet vt teemast [Eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features). 

See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.

Saate Microsoft Dynamics 365 for Retaili kasutamisel kuvada kassaaparaadis tootesoovitusi. *Soovitused* on kaubad, millest teie klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda. Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat.

## <a name="open-layout-designer"></a>Paigutusekujundaja avamine
1.  Minge jaotisse **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.
2.  Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada. Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse „F2CP16:9M” järgi.
3.  Otsige loendist ja valige soovitud kirje. Valige näiteks Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M”.
4.  Klõpsake valikut **Paigutusekujundaja**.
5.  Järgige paigutusekujundaja avamiseks viipasid. Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.
6.  Sisselogimisel avaneb alltoodule sarnane leht. Paigutus erineb olenevalt teie poele tehtud kohandustest.

[![kuvapaigutuse-pilt-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Kuvamisvaliku tegemine
-----------------------

Saadaval on kaks konfigureerimisvalikut. Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid. Võimalused on järgmised.
-   Soovitused on alati nähtaval.
-   Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.

#### <a name="to-make-recommendations-always-visible"></a>Soovituste alati nähtavaks tegemine

1.  Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge kui vasakul asuv kliendipaneel.[](./media/pic-2.png)[![kuvapaigutuse-pilt-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele. Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.[](./media/pic-3.png)[![kuvapaigutuse-pilt-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
4.  Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.
5.  Valige loendist suvand **1090, registrid**.
6.  Klõpsake valikut **Käivita kohe**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Soovituste vahekaardi lisamine kuva paremas servas olevasse nupuruudustikku

1.  Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.
2.  Klõpsake valikut **Kohanda**.[![pilt-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klõpsake valikut **Uus vahekaart**.
4.  Leidke vastlisatud uus vahekaart. Võib-olla peate selleks allapoole kerima.
5.  Valige ripploendist **Sisu** suvand **Soovitatud tooted**. [![pilt-6](./media/pic-6.png)](./media/pic-6.png)
6.  Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.
7.  Valige väljal **Pilt** vahekaardil kuvatav pilt.
8.  Klõpsake **OK**. Uus vahekaart kuvatakse nupuruudustikus.
9.  Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.
10. Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.
11. Valige loendist suvand **1090, registrid**.
12. Klõpsake valikut **Käivita kohe**.


<a name="see-also"></a>Vt ka
--------

[Isikupärastatud tootesoovituste ülevaade](personalized-product-recommendations.md)




