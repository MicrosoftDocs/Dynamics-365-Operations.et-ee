---
title: Lisada soovitusi kontrolli tehingu lehele POS seade
description: "Selles teemas kirjeldatakse soovitused juhtelement lisada kande ekraani Müügikoht (POS) seadme ekraani paigutuse kujundaja abil Microsoft Dynamics 365 toimingute küsimuses."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Lisada soovitusi kontrolli tehingu lehele POS seade

Selles teemas kirjeldatakse soovitused juhtelement lisada kande ekraani Müügikoht (POS) seadme ekraani paigutuse kujundaja abil Microsoft Dynamics 365 toimingute küsimuses.

Korraga kuvatakse toote soovitused POS seadmes Microsoft Dynamics 365 kasutamisel toiminguteks. *Soovitused* kaup teie klient võib olla huvitatud oma ostuajalugu, oma lemmikute loendi üksuste ja teiste klientide internetist ostetud kaupade ja Telliskivi-ja mördi kauplustes. Toote soovitused kuvamiseks peate juhtelemendi lisamine tehingu ekraan ekraani paigutuse kujundaja abil.

## <a name="open-layout-designer"></a>Avatud paigutus disainer
1.  Mine **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS**&gt;**ekraani paigutusega**.
2.  Kiire filtri abil leida ekraani, mida soovite juhtelemendi lisada. Näiteks filtreerida ning **ekraani paigutuse ID** välja väärtuse "F2CP16:9M".
3.  Otsige loendist ja valige soovitud kirje. Näiteks valige "nimi: F2CP16:9M paigutuse ID: F2CP16:9M".
4.  Klõpsake **paigutuse disainer**.
5.  Järgige viipasid käivitada paigutus disainer. Kui küsitakse mandaati, sisestage sama mandaati, mis olid kasutuses, kui paigutus disainer alustas **ekraani paigutusega** lehel.
6.  Kui te logite sisse, kuvatakse leht sarnaneb allpool. Paigutus on erinevad, sõltuvalt teie poe tehtud kohandused.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) valida kuvamissuvandi
-----------------------

Seal on kaks koosseisud võimalusi. Valige suvand, mis vastab kõige paremini teie poodi ja järgige juhiseid kontrolli lõpetamiseks. On kaks võimalust:
-   Soovitused on alati nähtav.
-   A **soovitused** vahekaardil kuvatakse ekraani paremas servas.

#### <a name="to-make-recommendations-always-visible"></a>Soovitused alati nähtavaks

1.  Vähendada kõrgus kande ridade üksikasjad ala, nii et see on sama kõrge kui klient paneel vasakul pool. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Vasakult menüüst lohistada soovitused kontrolli tehingu rida üksikasjad ja vahele center Tehingu ekraani allservas nuppu ruudustikus. Juhtelemendi suurust muuta, et see sobituks elamispinnal. [](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klõpsake selle **X** salvestamiseks ja väljumiseks paigutus disainer.
4.  Dynamics 365 toiminguteks, minge **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**Distribution plaanid**.
5.  Valige loendist, **1090 registreerib**.
6.  Klõpsake **Käivita kohe**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Soovitused vahekaardi lisamiseks nuppu Koordinaatvõrgu ekraani paremal

1.  Paremklõpsake tühjal viimase vahekaardi kohta asub lehe paremas servas nuppu all.
2.  Klõpsake **kohandamine**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klõpsake **uue vahekaardi**.
4.  Otsige uue vahekaardi, lisatud. Peate allapoole kerida.
5.  Aastal ning **sisu** rippmenüü, Vali **soovitatud tooted**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Linnas on **Label** välja, tippige vahekaardile soovitusi. Näiteks tippige "Soovitatavad tooted".
7.  Aastal ning **pilt** pildi kuvada vahekaardi number.
8.  Click **OK**. Vahekaardil kuvatakse nupp.
9.  Klõpsake selle **X** salvestamiseks ja väljumiseks paigutus disainer.
10. Dynamics 365 toiminguteks, minge **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**Distribution plaanid**.
11. Valige loendist, **1090 registreerib**.
12. Klõpsake **Käivita kohe**.


<a name="see-also"></a>Vt ka
--------

[Isikupärastatud ülevaade soovitused](personalized-product-recommendations.md)


