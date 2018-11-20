---
title: Protsessimalli loomine Attractis
description: Selles teemas antakse teavet selle kohta, kuidas Attractis protsessimalli luua.
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a>Protsessimalli loomine Attractis

[!include [banner](includes/banner.md)]

*Värbamisprotsessi mall* sisaldab kõiki tegevusi, mis peaksid olema tööle värbamise protsessi osad. Selles teemas kirjeldatakse protsessimalli elemente rakenduses Microsoft Dynamics 365 for Talent: Attract. Lisaks selgitatakse, kuidas malli luua.

> [!NOTE]
> Malli loomine on osa tervikliku värbamise lisamoodulist rakendusele Attract.

## <a name="template-management"></a>Mallihaldus

Organisatsioonid saavad otsustada, kas Attractis saavad protsessimalle luua kõik töörühma liikmed või ainult administraatorid. Mallihalduse konfigureerimiseks avage **Halduskeskus** \> **Mallihaldus**. Selleks, et töörühma liikmed saaksid oma malle luua, lülitage sisse mallihaldus. Kui te ei lülita mallihaldust sisse, saavad malle luua ainult administraatorid.

## <a name="default-template"></a>Vaikemall

Vaikemalli saab määrata ainult adminisitraator. Vaikemalli kasutatakse siis kui töö loomisel on mall valimata. Vaikemalli määramiseks avage **Halduskeskus** \> **Mallihaldus**. Valige malli kaardil, mis peaks olema vaikemall, kolmikpunkti nupp (**...**) ja seejärel valige **Sea vaikeseadeks**.

## <a name="create-a-process-template"></a>Protsessimalli loomine

Protsessimalle saavad luua administraatorid, värbajad ja personalijuhid. Protsessimall koosneb *etappidest* ja *tegevustest*. Etapid grupeerivad ühe või mitu tegevust. Vaikimisi on igal protsessimallil potentsiaalse töövõtja, avalduse ja pakkumise tegevused. Neid tegevusi sisaldavad etapid saab ümber nimetada. Saate lisada rohkem etappe, valides **+ Uus etapp**. Saate etappidele tegevusi lisada, pukseerides need sobivasse etappi või tehes neile tegevuste loendis topeltklõpsu.

> [!NOTE]
> Etapi nimed on kandidaatidele **Avalduse oleku** lehel näha. Pidage seda etappidele nimede valimisel meeles.

Tegevuste kohta lisateabe saamiseks vt [Värbamisprotsessi tegevused Attractis](./activities-attract.md).

Värbamisprotsessi malli loomiseks tehke järgmist.

1. Avage **Mallid**.
2. Valige **Uus**.
3. Sisestage **Mallinime** väljale malli nimi ja seejärel valige **Loo**.
4. Valige **Kinnitusprotsessi valimise** loendist **Vaikimisi**, et tööle kinnitust nõuda.
5. Valige potentsiaalsete töövõtjate lubamiseks või keelamiseks.
6. Valikuline: etappide lisamine või eemaldamine.

    - Etapi lisamiseks valige **+ Uus etapp**.
    - Etapi eemaldamiseks hoidke kursorit etapi kohal ja valige seejärel ilmunud prügikastinupule.

        > [!NOTE]
        > Potentsiaalse töövõtja, Rakenduse ja Pakkumise etappe ei saa eemaldada, kuid need saab ümber nimetada.

7. Valikuline: tegevuste lisamine või eemaldamine.

    - Tegevuse lisamiseks lohistage see tegevuste loendist otse sobivasse etappi. Teise võimalusena topeltklõpsake tegevusel ja valige etapp, kuhu see lisada.
    - Tegevuse eemaldamiseks laiendage seda ja seejärel valige prügikasti nupp tegevuse päises.

8. Valige **Salvesta**.

