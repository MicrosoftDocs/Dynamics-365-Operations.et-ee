---
title: Maks sisestatakse kandes valele pearaamatukontole
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui maks sisestatakse kandes valele pearaamatukontole.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6834b460d3a78e47edb2edb7a72651e8454bf0ac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343810"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Maks sisestatakse kandes valele pearaamatukontole

[!include [banner](../includes/banner.md)]

Sisestamise ajal võib juhtuda, et maks sisestatakse kandes valele pearaamatukontole. Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid. Selle teema näidetes kasutatakse äridokumendina müügitellimust.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Leia valesti sisestatud maksukande maksukood

1. Leheküljel **Kviitungi kanne** valige kanne, mida soovite kasutada ja seejärel valige **Sisestatud käibemaks**.

    [![Sisestatud käibemaksu nupp lehel kviitungi kanded.](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Kontrollige väärtust väljal **Käibemaksukood**. Selles näites on **km 19**.

    [![Käibemaksukoodi väli sisestatud käibemaksu lehel.](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Kontrollige pearaamatu sisestamise rühma maksukoodi

1. Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.
2. Otsige ja valige maksukood ning vaadake seejärel üle väärtus väljal **Pearaamatu sisestusgrupp**. Selles näites on **km**.

    [![Pearaamatu sisestamisgrupi väli käibemaksukoodide lehel.](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Väärtus väljal **Pearaamatu sisestusrühm** on link. Grupi konfiguratsiooni üksikasjade vaatamiseks valige link. Teise võimalusena valige ja hoidke all (või paremklõpsake) väljal ja valige käsk **Kuva üksikasjad**.

    [![Kuva käsu üksikasjad.](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Väljal **Tasumisele kuuluv käibemaks** kontrollige, et kontonumber on kandetüübi alusel õige. Kui ei ole, valige õige konto, mida sisestada. Selles näites tuleks müügitellimuse käibemaks sisestada käibemaksu käibemaksu tasumisele kuuluvale kontole 222200.

    [![Tasumisele kuuluva käibemaksu väli lehel Pearaamatu sisestamisgrupid.](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Järgmine tabel annab teavet iga välja kohta **Pearaamatu sisestamisgruppide** lehel.

    | Field                  | Kirjeldus |
    |------------------------|-------------|
    | Tasumisele kuuluv käibemaks      | Maksuhaldurile makstava tasumisele kuuluva käibemaksu põhikonto. |
    | Saadaolev käibemaks   | Maksuhaldurilt saadaolevate maksutagastuste põhikonto. |
    | Kasutusmaksu kulu        | Peamine konto, mida kasutatakse mahaarvatavate kasutusmaksude kirjendamiseks, mida hankijad ei nõua või aruandeks maksuhaldurile osana Euroopa Liidu (EL) kaupade ja teenuste maksu pöördmaksustamisest (GST) / ühtlustatud käibemaksust (HST). Suvand **Kasuta maksu** peab olema valitud kandes kasutatavale käibemaksukoodile jaotises käibemaksugrupp. See väli ei ole kohaldatav, kui lehel **Pearaamatu parameetrid** on valitud suvand **Rakenda käibemaksuga maksustamise reeglid**. |
    | Kasutusmaksu kohustus        | Põhikonto, mida kasutatakse maksuametile makstavate sissetulevate kasutusmaksude sisestamiseks. |
    | Tasakaalustuskonto     | Põhikonto, mida kasutatakse pearaamatu kontode netosaldo kirjendamiseks, mis on täpsustatud väljadel **Makstav kasutusmaks** ja **Saadaolev käibemaks**. |
    | Hankija skonto   | Põhikonto, mida kasutatakse selle pearaamatu sisestamisgrupiga seotud käibemaksukoodide varase makse soodustuse sisestamiseks. |
    | Kliendijuhtumi allahindlus | Põhikonto, mida kasutatakse selle pearaamatu sisestamisgrupiga seotud käibemaksukoodide varase makse soodustuse sisestamiseks. |

    Lisateavet leiate teemast [Käibemaksu jaoks pearaamatu sisestusgruppide seadistamine](tasks/set-up-ledger-posting-groups-sales-tax.md)

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Vigade parandamine koodis kontrollimaks pearaamatu dimensioone

Koodis määrab sisestuskonto pearaamatu dimensioon. Pearaamatu dimensioon salvestab andmebaasi konto kirje ID.

1. Müügitellimuse puhul lisage katkestuspunkt meetoditele **Tax::saveAndPost()** ja **Tax::post()**. Pööra tähelepanu parameetri **\_pearaamati dimensioon** väärtusele.

    [![Müügitellimuse koodi näidis, millel on katkestuspunkt.](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Ostutellimuse puhul lisage katkestuspunkt meetoditele **TaxPost::saveAndPost()** ja **TaxPost::postToTaxTrans()**. Pööra tähelepanu parameetri **\_pearaamati dimensioon** väärtusele.

    [![Ostutellimuse koodi näidis, millel on katkestuspunkt.](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Käivitage järgmine SQL-päring, et leida andmebaasis konto kuvamisväärtus, mis põhineb pearaamatu dimensiooni salvestatud kirje ID-l.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Kirje ID kuvatav väärtus.](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Uurida väljakutse pinu, et leida kus **_pearaamatu dimensiooni** väärtus on määratud. Tavaliselt on väärtus pärit **TmpTaxWorkTrans**. Sel juhul peaksite lisama katkestuspunkti **TmpTaxWorkTrans::insert()** ja **TmpTaxWorkTrans::update()**, et leida kus väärtus määratud on.

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine

Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
