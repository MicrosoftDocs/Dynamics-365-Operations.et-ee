---
title: Tootmises olevate materjalide vaikimisi reserveerimise põhimõtte alistamine
description: See artikkel kirjeldab, kuidas seadistada vaikimisi reserveerimispõhimõte igale kauba mudeligrupile, nii et igale kaubale, mis on tootmiskoosluse või partiitellimuse valemi osa, saab automaatselt rakendada erinevaid reserveerimispõhimõtteid.
author: johanhoffmann
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 87f10efd7eebdc034af3f7c9081d2674a6190b38
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334591"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Tootmises olevate materjalide vaikimisi reserveerimise põhimõtte alistamine

[!include [banner](../includes/banner.md)]

*Vaikimisi tootmise broneerimise alistamise* funktsioon võimaldab teil määrata vaikimisi reserveerimise põhimõtte igale kauba mudeligrupile. Seega saab igale tootmiskoosluse või partiitellimuse valemi osaks olevale kaubale rakendada erinevaid reserveerimise põhimõtteid. Saate valida, kas iga kauba mudeligrupp peaks alistama tellimusele määratud vaikimisi reserveerimise põhimõtte ning millist reserveerimise põhimõtet tuleks selle asemel kasutada (*käsitsi*, *hinnang*, *planeerimine*, *väljastamine* või *alustamine*).

Uue tootmistellimuse või partiitellimuse loomisel palutakse teil valida reserveerimise põhimõte, mis tuleks rakendada sellele tellimusele ja kõigile selle koosluse või valemiridade puhul. *Vaikimisi tootmise broneerimise alistamise* funktsiooni kasutamisel saavad osad või kõik koosluse või valemi read selle reserveerimise põhimõtte alistada ja selle asemel kasutada vastava kauba mudeligrupi jaoks seadistatud reserveerimise põhimõtet.

Näiteks kui teil on toormaterjale või koostisosi, mis nõuavad nende toodete jaoks loodud komplekteerimistööd, koosluse või valemiridu, vajavad füüsilist reserveerimist, kuna füüsiline reserveerimine on eeltingimuseks laotöö loomisele. Tavaliselt kui soovite, et reserveering toimuks automaatselt, valite ühe järgmistest reserveerimise põhimõtetest: *hindamine*, *planeerimine*, *vabastamine* või *alustamine*. Samas kui teil on materjale või koostisosi, mis ei vaja komplekteerimise tööd, sest need tarbitakse otse asukohast, valite tavaliselt *käsitsi* reserveerimise põhimõtte, mis ei tee mingeid füüsilisi reserveeringuid ega ei loo ühtegi komplekteerimise tööd.

## <a name="turn-the-override-default-production-reservation-feature-on-or-off"></a>Tootmise reserveerimise vaikefunktsiooni alistamise sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.25 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumis tootmise vaikereserveeringu funktsiooni.

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Tootmise reserveerimise poliitika määramine kauba mudeligrupile

1. Avage **Kuluhaldus \> Laoarvestuse poliitikate seadistus \> Üksuse mudeligrupid**.
1. Looge või valige kauba mudeligrupp.
1. Valige kiirkaardil **Laopoliitikad** märkeruut **Kauba tootmise reserveerimise alistamine**.
1. Valige väljal **Reserveering** valitud mudeligrupile kuuluvate kaupade reserveerimise põhimõte. (Need kaubad sisaldavad kaupu, mis on koosluse või valemireal.)

    - **Käsitsi** – mudeligrupi kaupu ei reserveerita tootmise jaoks automaatselt. Kuid neid saab vajadusel ka käsitsi reserveerida.
    - **Hinnang** – mudeligrupi kaubad reserveeritakse tootmistellimuse hindamise ajal füüsiliselt.
    - **Planeerimine** – mudeligrupi kaubad reserveeritakse tootmistellimuse planeerimise ajal füüsiliselt.
    - **Vabastamine** – mudeligrupi kaubad reserveeritakse tootmistellimuse vabastamisel füüsiliselt.
    - **Alustamine** – mudeligrupi kaubad reserveeritakse tootmistellimuse alustamise ajal füüsiliselt.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Näide: reserveerimise põhimõtete kasutamine hulgi-/pakkimisstsenaariumis

Suur hulk määrdematerjali toodetakse 1000-liitrises segajas. Pärast seda, kui materjalihulk on valmis, pumbatakse see mitmesse täitmisjaama, kus täidetakse erineva mõõduga pudeleid. Pärast täitmise lõpetamist pakitakse pudelid kastidesse. Seejärel pakitakse need kastid kaubaalustele.

Selles stsenaariumis luuakse partiitellimus 1000 liitmiseks materjalihulgaks. (See tellimus on hulgitellimus.) Kui see partiitellimus on lõpetatud, siis on see kinnitatud lõpetatuna materjali sisestamise asukohas, kus tellimus täidetakse. Seejärel luuakse iga pudeli suuruse täitmiseks ja pakkimiseks partii tellimus. (Need tellimused on pakkimistellimused.) Pakkimistellimustel on valem, mis koosneb hulgimaterjalist, tühjast pudelist, sildist ja teistest pakkematerjalidest. Kuna materjalihulk voolab otse segajast täitmisjaamadesse, ei ole koostisosa komplekteerimiseks laotöö vajalik ja materjalihulk tarbitakse tse sisestuskohast. Seetõttu seatakse reserveerimise põhimõtte väärtuseks *Käsitsi*. Muud materjalid viiakse etapiviisiliselt täitmisejaama komplekteerimise töö abil. Seega on nende ridade reserveerimise põhimõtteks määratud *vabastamine* näiteks nii, et reserveering toimub automaatselt, kui pakkimistellimus vabastatakse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]