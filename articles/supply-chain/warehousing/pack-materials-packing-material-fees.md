---
title: Pakkematerjalid ja tasud
description: "Pakkematerjalitasud makstakse jäätmekäitlusfirmale kindlate perioodide kaupa. Iga materjali eest, millest pakkimisühik koosneb, tuleb maksta summa kaaluühiku kohta. Pakkematerjalitasud arvutatakse ja esitatakse, kuid ühtegi pearaamatukannet ei sisestata, sest need tasud ei ole riigile makstavad maksud."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b131cdfa2f0e3b6a8f116464323d49eaa4584634
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="packing-materials-and-fees"></a>Pakkematerjalid ja tasud

[!INCLUDE [banner](../includes/banner.md)]

Pakkematerjalitasud makstakse jäätmekäitlusfirmale kindlate perioodide kaupa. Iga materjali eest, millest pakkimisühik koosneb, tuleb maksta summa kaaluühiku kohta. Pakkematerjalitasud arvutatakse ja esitatakse, kuid ühtegi pearaamatukannet ei sisestata, sest need tasud ei ole riigile makstavad maksud.

Pakkematerjalide kaalud ja tasud arvutatakse müügi- ja ostutellimuste ridade kohta.

Saate määratleda kaubale, kaupade pakkimisgrupile või kõikidele kaupadele vähemalt ühe pakkimisühiku. Pakkimisühik koosneb pakkematerjalidest, nende kaaludest ja pakkimisühikus sisalduvate kaupade arvust. Igale määratletud pakkematerjali tüübile määratakse pakkematerjali kood. Pakkematerjali koodi alusel saate määrata hinna määratletud perioodiks. Pakkematerjali tasu arvutatakse selle teabe alusel.

| **Märkus.**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Juhul, kui teie ettevõte ei maksa pakkematerjalitasu, saate seda funktsiooni kasutada pakkematerjalide kaalu statistika arvutamiseks. |

## <a name="setup-requirements-for-packing-material-fees"></a>Pakkematerjali tasude nõuete seadistamine
Enne pakkematerjalide kaalu ja/või pakkematerjali tasude arvutamist tuleb luua järgmised põhiandmed.

-   Pakkimisgrupid – saate luua kaupadele määratavad pakkimisgrupid.
-   Pakkematerjali koodid – saate luua pakkematerjali koodi igale määratletud pakkematerjali tüübile.
-   Pakkimisühikud – saate määrata pakkimisühiku kas kauba, pakkimisgrupi või kõikide kaupade jaoks. Iga pakkimisühiku puhul saate määratleda kaasatavad pakkematerjalid, kaalud ja sisestada väljale Pakkimisühiku tegur laoühiku teisendusteguri.
-   Pakkematerjali tasud – määrake pakkematerjali tasud pakkematerjali koodi kohta. Määratlege iga materjalitüübi puhul kehtivusperiood, materjali hind, valuuta ja ühik.

## <a name="packing-units-on-sales-order-lines"></a>Pakkimisühikud müügitellimuse ridadel
Müügitellimuse rea loomisel kontrollib süsteem, kas kaubale on määratud pakkimisühikud. Kui pakkimisühikud on määratud, uuendab süsteem müügitellimuse rida automaatselt koos määratud pakkimisühikuga ja pakkimisühiku kogusega. Pakkimisühikute kogus põhineb tellitud kogusel, mis jagatakse kaupade arvuga valitud pakkimisühikus. Kui pakkimisühikut ei ole määratud, saate pakkimisühiku ja pakkimisühiku koguse müügitellimuse reale käsitsi sisestada. Pakkimisühikut ja pakkimisühiku kogust saab ka müügitellimuse rea sisestamisel muuta. See võib olla vajalik, kui müügitellimuse rida tarnitakse või arveldatakse vaid osaliselt. Müügitellimuse eest arve esitamisel luuakse pakkematerjali kanded. Pakkematerjali kanded sisaldavad müügirea pakkematerjali kaalusid. Saate kandeid ka pärast nende eest arve esitamist muuta ja luua siis uusi kandeid.

## <a name="packing-units-on-purchase-order-lines"></a>Pakkimisühikud ostutellimuse ridadel
Süsteem ei loo ostutellimuse rea pakkematerjali kandeid. Arveldatud ostutellimuse ridade kanded luuakse käsitsi lehel **Pakkematerjali kanded**.

## <a name="set-up-customer-packaging-material-fee-license-numbers"></a>Kliendi pakkematerjali tasude litsentsinumbri seadistamine
Kui kliendid maksavad pakkematerjali tasud, määrake klientide pakkematerjali tasu litsentsinumber lehel **Kliendid**. Kui kliendile on määratud litsentsinumber, arvutatakse pakkematerjali tasud müügitellimuste arveldamisel automaatselt. Pärast arve esitamist tühjendatakse märkeruut **Arvuta tasu** lehel **Pakkematerjali kanded**, kuna teil pole vaja aruannet arvutada ja printida. Saate valida pakkematerjali kaalu printimise arvele ja teavitada kliente, et nemad maksavad tasud. 

Kui teie ettevõte maksab pakkematerjali tasusid, siis ärge kliendi litsentsinumbreid määrake. Pärast arveldamist märgitakse ruut **Arvuta tasu** lehel **Pakkematerjali kanded**. See näitab, et tasud arvutatakse aruande loomisel. Saate printida arvele kaalud ja näidata, et teie ettevõte maksab tasud.

## <a name="print-packaging-material-weights-on-invoices"></a>Pakkematerjali kaalu printimine arvetele
Saate printida arvele ka pakkematerjali kaalu ja näidata, kes maksab arvel näidatud pakkematerjali tasud. Kaalud summeeritakse pakkimiskoodi järgi.






