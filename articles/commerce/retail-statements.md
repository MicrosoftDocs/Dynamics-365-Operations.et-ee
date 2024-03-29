---
title: Jaemüügi väljavõtted
description: See artikkel kirjeldab, kuidas väljavõtteid luuakse ja sisestatakse.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878453"
---
# <a name="retail-statements"></a>Jaemüügi väljavõtted

[!include [banner](includes/banner.md)]

Rakenduses Dynamics 365 Commerce kasutatakse väljavõtte sisestamise protsessi pilvekassas ja Modern POS-is toimuvate kannete arvestamiseks. Väljavõtte sisestamise protsess kasutab jaotusgraafikut, et tõmmata kassa kannete komplekt peakontori klienti. Lehtedel **Kaubanduse parameetrid** ja **Kauplused** määratletud parameetreid kasutatakse üksikutesse väljavõtetesse tõmmatavate kannete valimiseks.

Järgmine joonis illustreerib väljavõtte sisestamise protsessi. Selles protsessis edastatakse kassas salvestatud kanded kliendile Kaubanduse ajasti abil. Pärast seda, kui klient on kanded kätte saanud, saate luua, arvutada ja sisestada kaupluse kannete väljavõtte.

[![Väljavõtte sisestamise protsess.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Väljavõtete loomine ja sisestamine

Saate luua väljavõtte käsitsi või päeva jooksul perioodiliselt käivituma seadistatud pakktöötlust kasutades. Mõlemal juhul kasutatakse väljavõtete loomiseks ja sisestamiseks järgmisi toiminguid.

### <a name="create-the-statement"></a>Väljavõtte loomine

Selles etapis identifitseeritakse kauplus, millele väljavõte käsitsi luuakse. Pakktöötluse konfigureerimisel saate luua automaatselt väljavõtteid kõigi kaupluste kohta enda määratud ajakava alusel.

### <a name="calculate-the-statement"></a>Väljavõtte arvutamine

Selles etapis valitakse kanderead lehtedel **Kaubanduse parameetrid** ja **Kauplused** igale kauplusele määratletud kriteeriumide alusel. Neil lehtedel saate määratleda kriteeriumid ja määrata, kuidas kandeid arvutatakse. Väljavõttesse kaasatud kannete loendi vaatamiseks enne väljavõtte arvutamist kasutage lehte **Kanded**.

Väljavõtte arvutamisel kasutatakse loendatud summana registrite päevakassasid. Loetud summa saab sisestada ka käsitsi. Väljavõttel kuvatakse kõikide maksemeetodite kannete müügisumma ja tegeliku loendatud summa vahe. Väljavõte sisestatakse ainult juhul, kui erinevus on väiksem kui kaupluse puhul määratletud maksimaalne sisestuse erinevus.

> [!NOTE]
> Väljavõtte arvutamise protsess kasutab globaalset numbriseeriat.

Väljavõtte arvutamisel hõlmab arvutus järgmisi ülesandeid.

- Märkige valitud kuupäevavahemiku kohta kanded, mida eelmise väljavõtte arvutusse ei kaasatud.
- Arvutage valitud kannete puhul makstud kogusummad. Tulemused kuvatakse väljavõtte ridadel, olenevalt väljavõtte meetodist.

    - Kui väljavõtte meetod on **Kokku**, luuakse valitud kannetes iga makseviisi jaoks üks rida.
    - Kui väljavõtte meetod on **Personal**, luuakse iga makseviisi jaoks üks rida kannetes, mille sooritas valitud personali liige.
    - Kui väljavõtte meetod on **Kassaterminal**, luuakse iga makseviisi jaoks üks rida kannetes, mis sooritati valitud registris.
    - Kui väljavõtte meetod on **Vahetus**, luuakse iga makseviisi jaoks üks rida kannetes, mis sooritati vahetuse jooksul.

Kui lehel **Kauplused** on märgitud ruut **Tükelda väljavõtte meetodi alusel**, luuakse eraldi väljavõte, võttes aluseks väljal **Väljavõtte meetod** valitud väärtuse.

Kui teie kaupluse töötunnid ületavad kesköö, saate konfigureerida väljavõtte sisestamist nii, et see põhineb kalendripäeva lõpu asemel tööpäeva lõpu seisul.

Sisestage lehe **Kauplused** kiirkaardi **Väljavõte/sulgemine** väljal **Tööpäeva lõpp** aeg, millal viimane kanne tuleb salvestada, et see kaasataks tööpäeva väljavõttesse. Märkige ruut **Sisesta tööpäevana** kannete sisestamiseks sama tööpäeva jooksul. Väljavõtte sisestamisel saab sama tööpäeva jooksul salvestatud kanded kaasata samasse müügitellimusse, isegi kui mõni kanne toimub enne keskööd ja mõni pärast keskööd.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Näide: väljavõtte sisestamine tööpäeva kohta, mis hõlmab kahte kalendripäeva

Kauplus on avatud 8.00 kuni 03.00 ja kaupluse konfiguratsioonis on ruut **Sisesta tööpäevana** märgitud. 31. mail salvestab kauplus kandeid ajavahemikus 8.00 kuni kesköö. Kauplus salvestab ka kandeid 1. juunil ajavahemikus 00.01 kuni 03.00.

Kui kauplus sisestab väljavõtte tööpäeva sulgemise seisuga, hõlmab loodav müügitellimus kõiki kandeid, mis salvestati töötundidel 08.00 kuni 03.00, kuigi kanded toimusid kahel päeval, 31. mail ja 1. juunil.

Kui sama kaupluse puhul on märkeruut **Sisesta tööpäevana** tühi, luuakse eraldi müügitellimused, kui kauplus sisestab oma tööpäeva lõpu väljavõtte. Üks müügitellimus sisaldab kandeid, mis registreeriti 31. mail töötundidel 8.00 kuni kesköö ja teine müügitellimus sisaldab kandeid, mis registreeriti 1. juunil ajavahemikus 00.01. kuni 03.00.

> [!NOTE]
> Enne väljavõtete loomist tuleb sulgeda väljavõtte perioodi vahetused.

### <a name="post-the-statement"></a>Väljavõtte sisestamine

Väljavõtte sisestamisel luuakse väljavõtte müügitellimused ja arved.

- Sularahamüük koondatakse ühele müügitellimusele ja selle eest esitatakse arve kauplusele määratud vaikekliendile.
- Müük, mille puhul klient lisati kandele kassas, loob eraldi müügitellimused ja arved, üks iga kordumatu kliendi jaoks.

Makse töölehed luuakse väljavõtte maksetele automaatselt ja kassa kaupluse varud uuendatakse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]