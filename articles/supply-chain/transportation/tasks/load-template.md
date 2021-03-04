---
title: Koorma mallid
description: Teemas kirjeldatakse koormamallide häälestamist ja koormamalli seostamist uue koormaga.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646380"
---
# <a name="load-templates"></a>Koorma mallid

Uue koorma loomisel saate määrata koormamalli. Koorma mallis on teave seadmete ja selliste mõõtmete kohta nagu koorma kõrgus, laius, sügavus ja maht.

Teemas kirjeldatakse koormamallide häälestamist ja koormamalli seostamist uue koormaga.

## <a name="set-up-a-load-template"></a>Koormamalli häälestamine

1. Valige **Transpordihaldus \> Häälestus \> Koorma koostamine \> Koormamall**.
1. Uue malli lisamiseks valige toimingupaanil nupp **Uus** või valige nupp **Redigeerimi**, et redigeerida olemasolevat malli.
1. Määrake uue või olemasoleva malli real järgmised väljad.

    - **Koormamalli ID** – sisestage koormamalli jaoks kordumatu identifikaator (ID).
    - **Seadmed** – valige seadmed, mida tuleks kasutada koorma saatmiseks.
    - **Koorma kõrgus**, **koorma laius** ja **Koorma sügavus** – sisestage koorma mõõtmed.
    - **Koorma max lubatud maht** ja **Koorma max lubatud kaal** – sisestage koorma suurim lubatud maht ja kaal.
    - **Maksimaalne lubatud brutokaal** – sisestage koorma suurim lubatud brutokaal. Koorma brutokaal hõlmab nii omakaalu kui ka koormakaalu.
    - **Koorma maksimaalne lubatud veokoguste arv** – sisestage maksimaalne arv veokoguseid, mida koorem võib sisaldada.
    - **Koorma laadimine põramdale virna** – valige see märkeruut, et kasutada koorma põrandale laadimist. Põranda laadimise stsenaariumi puhul virnastatakse kastid põrandast laeni ja seinast seinani, et konteineri mahtu parimal moel ära kasutada.

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="associate-a-load-template-with-a-new-load"></a>Koormamalli seostamine uue koormaga

1. **Avage Transpordihaldus \> Plaanimine \> Koorma plaanimise töölaud.**
1. Valige lehe ülemises osas üks järgmistest vahekaartidest, sõltuvalt sellest, millist tüüpi lähtedokumendi puhul koormust luuakse: **Saadetised**, **Müügiread**, **Üleviimistellimuse read** või **Ostutellimuse read**. 
1. Valige kindel dokument, mille jaoks koormat planeerida.
1. Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**.
1. Valige dialoogiboksi **Koormamall** väljal **Koormamalli ID** rakendatav mall.
1. Malli rakendamiseks valige **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]