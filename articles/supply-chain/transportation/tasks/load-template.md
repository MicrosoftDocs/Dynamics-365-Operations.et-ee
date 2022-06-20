---
title: Koorma mallid
description: See artikkel kirjeldab, kuidas seadistada koormamalle ja kuidas siduda koormamalli uue koormaga.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844176"
---
# <a name="load-templates"></a>Koorma mallid

[!include [banner](../../includes/banner.md)]

Uue koorma loomisel saate määrata koormamalli. Koorma mallis on teave seadmete ja selliste mõõtmete kohta nagu koorma kõrgus, laius, sügavus ja maht.

See artikkel kirjeldab, kuidas seadistada koormamalle ja kuidas siduda koormamalli uue koormaga.

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