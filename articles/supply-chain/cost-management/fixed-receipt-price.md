---
title: Fikseeritud jaehind
description: See artikkel selgitab, kuidas saab fikseeritud vastuvõtuhindu Microsoftis konfigureerida ja kasutada Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907576"
---
# <a name="fixed-receipt-price"></a>Fikseeritud jaehind

[!include [banner](../includes/banner.md)]

**Fikseeritud vastuvõtuhind** on *valik, mille saate valida kauba mudeligrupile, kui kasutate muud laomudelit kui Standardne kulu* või *Teisaldatud kaalutud keskmine*. Selle valiku varasemas Microsoft Dynamics AX versioonis nimetati selle suvandi nimi **Standardne kulu**. See nimetati ümber fikseeritud **vastuvõtuhinnaks**, kui Dynamics AX 2012 juurutati uus standardkulu laomudel. See artikkel selgitab, kuidas saab fikseeritud vastuvõtuhindu konfigureerida ja kasutada Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Fikseeritud jaehinnad

Kui valite **kauba mudeligrupi** **lehel** märkeruudu Fikseeritud vastuvõtuhind, kasutab süsteem sissetuleku hinda lao sissetuleku standardkuluna. Kui toote jaoks konfigureeritud ostuhind ja vaikimisi omahind erinevad **, sisestatakse erinevus fikseeritud jaehinna** **kasumile või fikseeritud jaehinna kahjumi** **kontole** ja tasakaalustatakse fikseeritud jaehinna vastaskontole, mille määrate lehel Lao sisestusreeglid.**·**

Kuna **fikseeritud vastuvõtuhinna** valikut kasutatakse koos erinevate laomudelitega (nt esimesena sisse, esimesena välja (FIFO); viimasena sisse, esimesena välja (LIFO) ja kaalutud keskmine), loob *lao sulgemis- ja korrigeerimisprotsess* siiski tasakaalustusi ja korrektsioone vastavalt **kauba mudeligrupi** lehel valitud laopõhimõttele. Korrektuure korrigeeritakse siiski ainult lao väljaminek.

Näiteks olete konfigureerinud toote kauba mudeligrupiga, kus laomudeli väli on seadistatud FIFO-ks ja valitud on suvand **Fikseeritud** *vastuvõtuhind*.**·** Kui saate lao ostutellimuse kaudu, seatakse laoväärtuseks kauba vaikimisi omahind toote sissetuleku ajal. Ostutellimuse arveldamisel sisestab süsteem väljastatud toote vaikekuluhinna laokontole, kui arve hind on erinev. See sisestab erinevuse fikseeritud jaehinna kasumi- või kahjumikontole. Hiljem, kui müüte või tarbite toodet, kasutab süsteem kauba jooksvat keskmist müügitellimuse arve sisestamise ajal (v.a juhul, kui kasutate märkimist).

Lao sulgemise ja *korrigeerimise protsessi käivitamisel* loob süsteem tasakaalustamise esimese väljaminek esimese sissetulekuga. Sissetulekul kasutatud vastuvõtuhinna ja väljaminekul kasutatud jooksva keskmise vahe sisestatakse uude kandesse.

## <a name="enable-fixed-receipt-prices"></a>Luba fikseeritud jaehinnad

Kauba fikseeritud jaehindade lubamiseks järgige neid samme.

1. Avage **Varude haldus \> Seadistus \> Varud \> Kauba mudeligrupid**.
2. Looge uus kauba mudeligrupp või valige olemasolev mudeligrupp.
3. Kuluarvestuse **meetodi &kulu tuvastamise kiirkaardil** märkige ruut **Fikseeritud vastuvõtuhind**.

    > [!NOTE]
    > Te ei saa valida märkeruutu **Fikseeritud vastuvõtuhind,** kui laomudeli **väli** on seatud *valikule Standardne kulu või* Teisaldatud *keskmine*.

4. Sulgege leht.

Pärast suvandi Fikseeritud **vastuvõtuhind lubamist** peate varude sisestusreeglid järgmiste sammude abil uuendama.

1. Avage **Varude haldus \> Seadistus \> Sisestus \> Sisestus**.
1. **Valige vahekaardi Ostutellimus** veerus Vali suvand **Fikseeritud** jaehinna **kasum**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadistage uus rida nii, et see rakenduks kauba mudeligrupile, mille jaoks olete lubanud fikseeritud sissetulekute hinnakujunduse, ja määratlege põhikonto, mida kasutatakse ostutellimuste fikseeritud vastuvõtuhinna kasumi kirjendamiseks. Konfigureerige muud sätted vastavalt vajadusele.
1. Valige veerus **Vali** fikseeritud jaehinna **kahjum**. Lisage uus rida, mida rakendatakse kauba mudeligrupile, mille jaoks olete lubanud sissetuleku fikseeritud hinnakujunduse, ja määrake põhikonto, mida kasutatakse ostutellimuste fikseeritud vastuvõtuhinna kahjumi kirjendamiseks. Konfigureerige muud sätted vastavalt vajadusele.
1. Valige veerus **Vali fikseeritud** jaehinna **vastaskonto**. Lisage uus rida, mida rakendatakse kauba mudeligrupile, mille jaoks olete lubanud sissetuleku fikseeritud hinnakujunduse, ja määrake põhikonto, mida kasutatakse ostutellimuste fikseeritud jaehinna vastaskonto kirjendamiseks. Konfigureerige muud sätted vastavalt vajadusele.
1. Valige vahekaardi **Varud** veerus Vali **suvand** Fikseeritud **jaehinna kasum**. Lisage uus rida, mida rakendatakse kauba mudeligrupile, mille jaoks olete lubanud sissetuleku fikseeritud hinnakujunduse, ja määrake põhikonto, mida kasutatakse lao fikseeritud vastuvõtuhinna kasumi kirjendamiseks. Konfigureerige muud sätted vastavalt vajadusele.
1. Valige veerus **Vali** fikseeritud jaehinna **kahjum**. Lisage uus rida, mida rakendatakse kauba mudeligrupile, mille jaoks olete lubanud sissetuleku fikseeritud hinnakujunduse, ja määrake põhikonto, mida kasutatakse lao fikseeritud vastuvõtuhinna kahjumi kirjendamiseks. Konfigureerige muud sätted vastavalt vajadusele.

> [!NOTE]
> Tavaliselt on soovitatav, et väljadel **Fikseeritud jaehinna** **kasum ja** Fikseeritud jaehinna kahjum kasutaks sama põhikontot nii ostutellimuste kui ka laovarude puhul.

> [!IMPORTANT]
> Kui muudate välja **Hind väärtust** **·** **kiirkaardil** Väljastatud tooted kulude haldamine, ei hinda süsteem automaatselt vaba kaubavarusid. Käsitsi lahendusena avage sulgemis- **ja korrigeerimisleht** ja **valige tegevuspaanil \> korrigeerimise** vaba kaubavaru. Seejärel valige vabad kaubad ja korrigeerige need praegusele hinnale. Üks standardse kulu laomudeli kasutamise selge eelis on see, et süsteem hinnab vaba kaubavaru automaatselt ümber.
