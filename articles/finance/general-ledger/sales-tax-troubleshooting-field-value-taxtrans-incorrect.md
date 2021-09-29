---
title: TaxTransi välja vale väärtus
description: Selles teemas antakse teavet TaxTransi valede väljaväärtuste tõrkeotsingu kohta.
author: EricWangChen
ms.date: 04/27/2021
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
ms.openlocfilehash: 00424d98d5ff99123edf42ee19919d149e7a6abc
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488283"
---
# <a name="incorrect-field-value-in-taxtrans"></a>TaxTransi välja vale väärtus

[!include [banner](../includes/banner.md)]

Kui **TaxTrans** välja väärtus on vale, kasutage probleemi lahendamiseks selle teema teavet.

## <a name="overview-of-values"></a>Väärtuste ülevaade
Järgmine loend näitab, kuidas **TaxTrans**, **TaxUncommitted** ja **TmpTaxWorkTrans** on sarnased andmekomplektid, kuid töös erinevad.

  - **TaxTrans** on andmebaasi kinnistatud lõplik sisestatud maksukanne.
  - **TaxUncommitted** on andmebaasis kinnistatud vahe arvutatud maksu tulemus (kui see on olemas), mida kasutatakse hiljem sisestamisel.
  - **TmpTaxWorkTrans** on ajutine arvutatud maksu tulemus mälu tabelis (tabeli tüüp = InMemory).

Kui leiate vale **TaxTrans** veeru algpõhjuse, olete leidnud ka vale **TaxUncommitted** või **TmpTaxWorkTrans** veeru algpõhjuse. Seda seetõttu, et kolm veergu on üksteisest kopeeritud.

Tavaliselt luuakse maksuarvestuse ajal **TmpTaxWorkTrans** ja seejärel (kui on olemas) **TaxUncommitted**. Maksu sisestamisel luuakse **TaxTrans**.


## <a name="add-breakpoints"></a>Lisa katkestuspunktid
Katkestuspuntide lisamiseks tehke järgmised toimingud: 

1. Lisage laiendid ja katkestuspunktid *insert()* ja *update()* nagu alltoodud laiendites.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Võite katkestuspunktid lisada ka otse, kui **TaxUncommitted** ei ole lisatud.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Taasesitamine ja vigade eemaldamine

Pärast katkestuspunktide seadistamist on vigade eemaldamise ajal nähtavad kõik andmete püsivuse muutused. Et leida **TaxTrans**, **TaxUncommitted** või **TmpTaxWorkTrans** vale veeru algpõhjus, vaadake üle ja märkige järgmised üksused:

- Viimane katkestuspunkt, kus veerg on õige.
- Esimene katkestuspunkt, kus veerg on vale.
- Mis toimub nende kahe punkti vahel.

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine
Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, pöörduge abi saamiseks Microsoft Support'i poole.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

