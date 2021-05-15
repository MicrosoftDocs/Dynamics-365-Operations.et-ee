---
title: Maksu ei arvutatud või maksusumma on null
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui maksusumma on 0 (null) või maksu ei arvutata.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947626"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Maksu ei arvutatud või maksusumma on null

[!include [banner](../includes/banner.md)]

Kandel võib olla rea summa, mis ei ole 0 (null), kuid maksu pole arvutatud või on arvutatud maksusumma 0. Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Kontrollige, kas kanne on maksukoodid õigesti valinud

Kui kanne ei vali õigeid maksukoode või kui see ei vali ühtegi maksukoodi, siis makse ei arvestata. Järgige neid samme, et kontrollida, kas kanne on maksukoodid õigesti valinud. 

1. Kandereal **Rea detailid** kiirkaardil **Seaded** vahekaardi jaotises **Käibemaks** kontrollige, kas on valitud õiged maksugrupid väljadel **Kauba käibemaksugrupp** ja **Käibemaksugrupp**. Kui õigeid maksugruppe ei ole valitud, valige need.

    [![Kauba käibemaksugrupp ja käibemaksugrupi väljad](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksu grupid**.
3. Valige sobiv käibemaksugrupp ja tehke seejärel kiirkaardil **Seaded** maksukoodi märkus väljal **Käibemaksukood**.

    [![Käibemaksugruppide leht](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Kauba käibemaksugrupid**.
5. Valige sobiv kauba käibemaksugrupp ja seejärel kontrollige kiirkaardil **Seaded**, et välja **Käibemaksukood** maksukood vastab käibemaksugrupi maksukoodile.

    [![Kauba käibemaksugruppide leht](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Kui maksukoodid ei kattu, värskendage käibemaksukoodi ühele grupist.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Kontrollige, kas valitud maksukoodid ei ole maksuvabad ja kas neil on õige maksumäära väärtus

Kui maksukoodid on maksuvabad või kui maksumäär on 0 (null), on maksu arvutamise tulemus 0. Järgige neid samme, et määrata, kas valitud maksukoodid on maksuvabad, ja kontrollimaks, et neile rakendatakse õiget maksumäära.

1. Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksu grupid**.
2. Valige sobiv käibemaksugrupp ja seejärel kontrollige kiirkaardil **Seaded**, et **Maksuvabastus** märkeruut on tühi. Kui ruut on märgitud, tühjendage see.

    [![Maksuvaba märkeruut käibemaksugruppide lehel](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.
4. Valige sobiv käibemaksukood ja seejärel kontrollige, et maksumäära väärtus väljal **Väärtus** ei oleks 0 (null). Kui väärtus on 0, uuendage välja nii, et selle väärtuseks oleks seadistatud õige maksumäär.

    [![Välja väärtus Käibemaksukoodi väärtuse lehel](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Määrake, kas null on õige maksusumma

Mõnes stsenaariumis on maksusumma 0 (null) õige. Järgige neid samme, et määratleda, kas 0 on teie kandele õige maksusumma.

1. Avage **Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**.
2. Kontrollige vahekaardi **Käibemaks** väljal **Arvutusmeetod**, et **Kogusumma** on valitud.

    [![Kalkulatsiooni meetodi väli pearaamatu parameetrite lehel](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.
4. Valige sobiv käibemaksukood, valige **Kalkulatsioon** \> **Marginaali alus** ja kontrollige, et marginaali aluseks on seatud **Arve saldo netosumma** või **Arve kogusumma koos teiste käibemaksusummadega**. Lisateavet vt [Arve kogusumma koos teiste käibemaksusummadega](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Kui õiged väärtused on seadistatud 2. ja 4. sammus, määratlege, kas kande kogusumma on 0 (null). Kui kogusumma on 0, on eeldatav maksusumma 0. Kuna maksu arvutamine põhineb arve saldo kogusummal ja see summa ei ole rida realt, eraldatakse maksusumma 0 igale reale pärast maksu arvutamist.

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine

Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
