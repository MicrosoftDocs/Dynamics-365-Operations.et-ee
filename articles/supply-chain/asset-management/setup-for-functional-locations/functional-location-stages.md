---
title: Töö asukoha töötsükli olekud
description: See artikkel kirjeldab, kuidas seadistada funktsionaalse asukoha olekuid ja töötsükli mudeleid Varahalduses.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae56c2b734339343b134be95abe0ce40b70c8a0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934728"
---
# <a name="functional-location-lifecycle-states"></a>Töö asukoha töötsükli olekud

[!include [banner](../../includes/banner.md)]

 

See artikkel kirjeldab, kuidas seadistada varahalduses funktsionaalse asukoha töötsükli olekuid ja töötsükli mudeleid. Funktsionaalse asukoha elutsükli olekud määratlevad, et funktsionaalne asukoht võib läbida näiteks olekud loodud, aktiivne ja lõpetatud. Kõiki funktsionaalseid asukohti, olenemata nende elutsükli olekust, saate vaadata loendilehel **Kõik funktsionaalsed asukohad**. Funktsionaalse asukoha olekut saate muuta valides selle loendilehel **Kõik funktsionaalsed asukohad** ja valides **Värskenda funktsionaalse asukoha olek**.

## <a name="set-up-functional-location-lifecycle-states"></a>Seadke funktsionaalse asukoha elutsükli olekud

1. Valige **Varahaldus** > **Sätted** > **Funktsionaalsed asukohad** > **Elutsükli olekud**.
2. Uue funktsionaalse asukoha oleku loomiseks valige **Uus**.
3. Sisestage oleku ID väljale **Elutsükli olek** ja funktsionaalse asukoha oleku nimi väljale **Nimi**. Väljal **Elutsükli mudelid** saate vaadata funktsionaalse asukoha olekut kasutavate funktsionaalse asukoha oleku elutsükli mudelite arvu.
4. Kiirkaardil **Üldine** valige „Jah“ tumblernupul **Aktiivne**, kui funktsionaalne asukoht peaks selles olekus aktiivne olema.
5. Valige „Jah“ tumblernupul **Loo varad**, kui varade loomine peaks olema automaatselt võimalik sama nimega nagu funktsionaalne asukoht ja installige see funktsionaalse asukoha selle olekuga.  
>[!NOTE]
>See tumblernupp on seotud väljaga **Vara tüüp** kiirkaardil **Üldine** vormil **Funktsionaalse asukoha tüübid** (**Varahaldus** > **Sätestamine** > **Funktsionaalsed asukohad** > **Funktsionaalse asukoha tüübid**).

6. Valige „Jah“ tumblernupul **Nimeta asukoht ümber**, kui selles olekus on võimalik muuta funktsionaalse asukoha nime.
7. Valige „Jah“ tumblernupul **Uued alamasukohad**, kui selles olekus on võimalik lisada uusi alamasukohti funktsionaalsele asukohale.
8. Valige „Jah“ tumblernupul **Installi varad**, kui selles olekus on võimalik installida varasid funktsionaalsele asukohale.
9. Valige „Jah“ tumblernupul **Kustuta funktsionaalne asukoht**, kui selles olekus on võimalik kustutada funktsionaalne asukoht.
10. Valige vara olek väljal **Elutsükli olek**, kui soovite, et vara elutsükli olekut kõigi funktsionaalse asukoha varade kohta värskendataks selles olekus automaatselt. Näide: kui sulete funktsionaalse asukoha ja määrate funktsionaalse asukoha elutsükli oleku väärtuseks „Lõpetatud“, võite soovida automaatselt muuta selle funktsionaalse asukoha installitud varade elutsükli olekuks „Pole kasutuses“.


>[!NOTE]
>Funktsionaalsed asukoha elutsükli olekud, elutsükli mudelid ja tüübid on seotud ja neid kasutatakse samamoodi nagu töötellimuse elutsükli olekud, töökäsu elutsükli mudelid ja töötellimuse tüübid. 

## <a name="set-up-functional-location-lifecycle-models"></a>Funktsionaalse asukoha elutsükli mudelite sätestamine

Kui olete loonud oma funktsionaalsete asukohtade jaoks vajalikud elutsükli olekud, saab neid rühmadesse jagada. Seda tehakse selleks, et luua elutsükli mudeli voog, mida võib kasutada erinevat tüüpi funktsionaalsete asukohtade puhul. Luua tuleks vähemalt üks standardne funktsionaalne asukoha elutsükli mudel.

1. Valige **Varahaldus** > **Sätestamine** > **Funktsionaalsed asukohad** > **Elutsükli mudelid**.
2. Valige uue elutsükli mudeli loomiseks **Uus**.
3. Sisestage elutsükli mudeli ID väljale **Elutsükli mudel** ja elutsükli mudeli nimi väljale **Nimi**. Väljadel **Funktsionaalsed asukoha tüübid** ja **Elutsükli olekud** näete elutsükli mudelit kasutatavate funktsionaalsete asukoha tüüpide arvu ja elutsükli mudelis valitud olekute arvu.
4. Kiirkaardil **Elutsükli olekud** valige olekud, mis peaksid olema mudelisse kaasatud. Seda saab teha klõpsates olekul jaotises **Ülejäänud elutsükli olekud** ja klõpsake nuppu ![edasi nool.](media/02-setup-for-functional-locations.png) nupp.
5. Kui soovite valida mudeli jaoks kõik saadaolevad olekud, klõpsake nupul ![Vali kõik saadaolevad etapid.](media/03-setup-for-functional-locations.png) nupp. Kõik olekud viiakse üle jaotisesse **Valitud elutsükli olekud**.
6. Kui soovite valitud olekut mudelist eemaldada, valige soovitud olek jaotises **Valitud elutsükli olekud** ja seejärel valige nupp ![tagasi nool.](media/04-setup-for-functional-locations.png). nupp.
7. Valige **Elutsükli oleku värskendused**, et määratleda, millised elutsükli olekud saavad valitud olekut järgida.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
