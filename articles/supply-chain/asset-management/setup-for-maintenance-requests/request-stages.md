---
title: Hooldustaotluse elutsükli olekud
description: See teema kirjeldab, kuidas seadistada hooldustaotluse elutsükli olekuid varahalduses.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ece0fc1121211706350d804fec59e72ef08282fcba4e65f557a510834738b11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743670"
---
# <a name="maintenance-request-lifecycle-states"></a>Hooldusnõuete töötsükli olek

[!include [banner](../../includes/banner.md)]

 


Hooldustaotluse elutsükli olekud määratlevad etapid, mida taotlus võib läbida. Näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**. Kui hooldustaotlus teisendatakse töökäsuks, tuleks hooldustaotluse elutsükli olekut värskendada olekusse **Lõpetatud** või **Suletud**, et see ei oleks enam aktiivne. Loendileht **Kõik hooldustaotlused** näitab kõiki hooldustaotlusi, olenemata nende elutsükli olekust.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Hooldustaotluse elutsükli olekute sätestamine

1. Valige **Varahaldus**\>**Häälestus**\>**Hooldustaotlused**\>**Elutsükli olekud**.
2. Valige uue hooldustaotluse elutsükli oleku loomiseks **Uus**.
3. Sisestage väljale **Elutsükli olek** elutsükli olek ID.
4. Väljale **Nimi** sisestage nimi.

    Kiirkaardi **Üksikasjad** väljal **Elutsükli mudelid** kuvatakse hooldustaotluste elutsükli mudelite arvu, mida selles elutsükli olekus kasutatakse.

5. Kiirkaardil **Üldine** sätestage suvandi **Aktiivne** väärtuseks **Jah**, kui hooldustaotlus peaks selle elutsükli oleku jooksul aktiivne olema.
6. Sätestage suvandi **Määra tegelik lõpp** väärtuseks **Jah**, kui tegelik lõppkuupäev ja kellaaeg tuleks automaatselt sisestada hooldustaotlusele, mis on selles töötsükli olekus.
7. Sätestage suvandi **Loo töökäsk** väärtuseks **Jah**, kui töökäsku saab luua hooldustaotlusest, mis on selles elutsükli olekus.
8. Seadke suvandi **Kustuta** väärtuseks **Jah**, kui hooldustaotlust saab kustutada, kui see on selles elutsükli olekus.
9. Kiirkaardil **Värskenda** on valikud **Sissetulev** ja **Väljaminev** jaotises **Vara** asjakohased, kui kasutate depooparandust. Seadke sobiv suvand väärtusele **Jah**, kui hooldusnõudes valitud varade töötsükli olek tuleks automaatselt muuta väärtusele **Sissetulev** või **Väljaminev**, kui selle hooldusnõude töötsükli olek on seatud väärtusele **Sissetulev** või **Väljaminev**.

Järgnev illustratsioonil kuvatakse lehe **Hooldustaotluse elutsükli olekud** näide.

![Hooldusnõuete töötsükli olekute leht.](media/02-setup-for-requests.png)

> [!NOTE]
> Hooldustaotluse elutsükli olekud, elutsükli oleku rühmad ja tüübid on seotud ja neid kasutatakse samal viisil nagu töökäsu elutsükli olekud, elutsükli oleku rühmad ja tüübid. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Hooldustaotluse elutsükli mudelite sätestamine

Pärast seda, kui olete loonud oma hooldustaotluste jaoks nõutavad elutsükli olekud, saab neid jagada elutsükli oleku rühmadeks või elutsükli mudeliteks. Hooldustaotluse elutsükli mudeleid kasutatakse voo loomiseks, mida saab kasutada eri tüüpi hooldustaotluste puhul. Vähemalt üks standardne hooldustaotluse elutsükli mudel tuleks luua.

1. Valige **Varahaldus**\>**Häälestus**\>**Hooldustaotlused**\>**Elutsükli mudelid**.
2. Uue hooldustaotluse elutsükli mudeli loomiseks valige **Uus**.
3. Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.
4. Väljale **Nimi** sisestage nimi.

    Kiirkaardil **Üksikasjad** kuvab **Elutsükli olekud** selles elutsükli mudelis valitud elutsükli olekute arvu. Väljal **Hooldustaotluse tüübid** kuvatakse selles elutsükli mudelis kasutavate hooldustaotluse tüüpide arvu.

5. Kiirkaardil **Elutsükli olekud** valige need elutsükli olekud, mis tuleks elutsükli mudelisse kaasata.

    - Elutsükli oleku lisamiseks lifecycle mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige paremnool ![paremnool.](media/03-setup-for-requests.png) et teisaldada see valitud jaotisesse **Elutsükli valitud olekud**.
    - Et lisada kõik saadaolevad elutsükli olekud elutsükli mudelisse valige **Vali kõik saadaolevad olekud** nupp ![Vali kõik saadaolevad olekud.](media/04-setup-for-requests.png). Kõik elutsükli olekud teisaldatakse jaotisesse **Valitud elutsükli olekud**.
    - Elutsükli oleku lisamiseks elutsükli mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige paremnool ![paremnool.](media/05-setup-for-requests.png) et teisaldada see valitud jaotisesse **Elutsükli järelejäänud olekud**.

6. Kiirkaardil **Üldine** väljad jaotises **Värskendused** on asjakohased, kui kasutate depooparandust.

    - Väljal **Vastuvõetud vara elutsükli olek** valige vara elutsükli olek hooldustaotlusel valitud varadele, mida peaks automaatselt värskendama, kui need on vastuvõetud depooparanduseks.
    - Väljal **Kohale toimetatud elutsükli olekud** valige vara elutsükli olek hooldustaotlusel valitud varadele, mida peaks automaatselt värskendama, kui need tagastatakse pärast parandust.

Järgnev illustratsioon näitab lehe **Hooldustaotluse elutsükli mudelid** näidet.

![Hooldusnõuete töötsükli mudelite leht.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]