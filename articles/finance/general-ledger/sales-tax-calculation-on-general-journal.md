---
title: Arvutatud käibemaks üldise töölehe ridade kohta
description: See artikkel selgitab, kuidas eri tüüpi kontode (hankija, klient, pearaamat ja projekt) puhul pearaamatu ridadel käibemakse arvutatakse.
author: EricWangChen
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: a73e145dd26e930c860e9ea31d7dab4f1593c2a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845283"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Arvutatud käibemaks üldise töölehe ridade kohta
[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas eri tüüpi kontode (hankija, klient, pearaamat ja projekt) puhul pearaamatu ridadel käibemakse arvutatakse.

Protsessi saab jagada kolme etappi:

- Määratlege käibemaksu suund.

- Määratlege käibemaksu summa, mis talletatakse ajutise käibemaksu tabelis.

- Määratleb käibemaksu summa ja konto kandel.

## <a name="determine-the-sales-tax-direction"></a>Määratlege käibemaksu suund.

Käibemaksu suuna määratlemise viis sõltub konto tüübist kandes. Käibemaksu suund määratakse konto tüübi ja käibemaksukoodi kombinatsiooniga. Järgmistes jaotistes on võimalused üksikasjalikumalt. 

### <a name="account-type-is-project"></a>Kontotüüp on Projekt

Kui kandel on töölehe rida, kus konto tüüp on **Projekt**, rakendatakse kõigil kande tööleheridadel sama maksu suunda. Järgmine illustratsioon näitab seda vormingut. Järgmised punktid näitavad projekti kontode võimalikke maksu suundi.

• Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.

• Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.

• Kui käibemaksukood on intracom km, siis käibemaksu suund on tasumisele kuuluv käibemaks.

• Kui käibemaksukood on pöördmaksustamine, siis käibemaksu suund on tasumisele kuuluv käibemaks.

Vastasel juhul on käibemaksu suund saadaolev käibemaks.

Järgmine diagramm illustreerib reeglit graafiliselt.

![Maksu suuna võimalused projekti kontodele.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Kontotüüp on Tarnija

Kui kandel on töölehe rida, kus konto tüüp on **Tarnija**, rakendavad kõik kande töölehe read sama maksu suuna. Järgmised punktid näitavad tarnija kontode võimalikke maksustamise suundi. 

• Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.

• Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.

• Kui käibemaksukood on intracom km, siis käibemaksu suund on tasumisele kuuluv käibemaks.

• Kui käibemaksukood on pöördmaksustamine, siis käibemaksu suund on tasumisele kuuluv käibemaks.

Vastasel juhul on käibemaksu suund saadaolev käibemaks.

Järgmine diagramm illustreerib reeglit graafiliselt.

![Maksu suuna võimalused tarnija kontodele.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Kontotüüp on Klient

Kui kandel on töölehe rida, mille kontotüüp on **Klient**, kehtivad kõik kande tööleheread sama maksusuunaga. 

Kui käibemaksukood on maksust vabastatud, on käibemaksu suund maksuvaba müük. Muul juhul on käibemaksu suund tasumisele kuuluv käibemaks.

### <a name="account-type-is-ledger"></a>Konto tüüp on Pearaamat

Järgmisel joonisel on näha reegel, mis rakendub siis, kui kandel on ainult töölehe read, kus konto tüüp on **Pearaamat**. Järgmised punktid näitavad pearaamatu kontode võimalikke maksustamise suundi.

• Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.

• Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.

Vastasel juhul, kui töölehe summa on deebet (positiivne), on käibemaksu suund saadaolev käibemaks. Kui töölehe summa on kreedit (negatiivne), on käibemaksu suund tasumisele kuuluv käibemaks.

Järgmine diagramm illustreerib reeglit graafiliselt.

![Maksu suuna võimalused pearaamatu kontodele.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Käibemaksu suuna muutmine

Käibemaksu suunda saate muuta siis, kui kanne sisaldab ainult ridu, mille konto tüüp on **Pearaamat**.

Avage **Pearaamat \> Kontode tabel \> Kontod \> Põhikontod**, ja valige **juriidilise isiku muutmiste** kiirkaart

## <a name="determine-the-sales-tax-amount"></a>Käibemaksu summa määramine

Selles jaotises kirjeldatakse käibemaksu summa märgi arvutamist.

![Käibemaksu kannete leht.](media/sales-tax-amount-sign.jpg)

Järgmine tabel näitab üldist reeglit käibemaksu direktiivi piiritlemiseks ja määravad käibemaksu summad ajutise käibemaksu tabelis.

| Töölehe rea summa | Käibemaksu suund  | Käibemaksu summa märk |
|---------------------|----------------------|-----------------------|
| Positiivne            | Saadaolev käibemaks | Positiivne              |
| Positiivne            | Tasumisele kuuluv käibemaks    | Negatiivne              |
| Negatiivne            | Saadaolev käibemaks | Negatiivne              |
| Negatiivne            | Tasumisele kuuluv käibemaks    | Positiivne              |

On olemas erireegel kannete jaoks, millel on ainult read **Projekt** või **Pearaamat**, kui real **Pearaamat** on valitud käibemaksugrupp või kauba käibemaksugrupp. Seda reeglit juhib üldiste funktsioon **Lubage sõltumatu käibemaksu arvutamise funktsioon pearaamatus**. Kui see funktsioon on välja lülitatud, kasutab rea **Pearaamatu** maksusumma rea **Projekt** deebeti/kreediti suunda. Kui see funktsioon on sisse lülitatud, kasutab rea **Pearaamat** maksusmma omaenda deebeti/kreediti suunda. Järgmised tabelid näitavad iga stsenaariumi reeglit. 

**Reegel sisse lülitatud funktsiooni korral**

| Projekti töölehe rea summa | Käibemaksu suund  | Käibemaksu summa märk |
|--------------------------------|----------------------|-----------------------|
| Positiivne                       | Saadaolev käibemaks | Positiivne              |
| Negatiivne                       | Saadaolev käibemaks | Negatiivne              |

**Reegel välja lülitatud funktsiooni korral**

| Pearaamatu töölehe rea summa  | Käibemaksu suund  | Käibemaksu summa märk |
|--------------------------------|----------------------|-----------------------|
| Positiivne                       | Saadaolev käibemaks | Positiivne              |
| Negatiivne                       | Saadaolev käibemaks | Negatiivne              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Määratleb kande käibemaksu summa ja konto

Kui sisestate käibemaksu, tuuakse põhikonto pearaamatusse sisestatava grupi profiilist. Kui käibemaks on saadaolev, kasutab süsteem profiilis määratletud saadaoleva käibemaksu kontot. Kui käibemaks on tasumisele kuuluv, kasutab süsteem profiilis määratletud tasumisele kuuluva käibemaksu kontot.

Järgmine tabel näitab üldist reeglit.

| Käibemaksu suund  | Käibemaksu summa märk | Käibemaksukonto      | Kandesumma |
|----------------------|-----------------------|------------------------|-------------------|
| Saadaolev käibemaks | Positiivne              | Saadaoleva käibemaksu konto | Positiivne (deebet)  |
| Saadaolev käibemaks | Negatiivne              | Saadaoleva käibemaksu konto | Negatiivne (kreedit)  |
| Tasumisele kuuluv käibemaks    | Positiivne              | Tasumisele kuuluva käibemaksu konto    | Negatiivne (kreedit)  |
| Tasumisele kuuluv käibemaks    | Negatiivne              | Tasumisele kuuluva käibemaksu konto    | Positiivne (deebet)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
