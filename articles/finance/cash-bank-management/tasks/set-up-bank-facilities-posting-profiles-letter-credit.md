---
title: Pangateenuste ja akreditiivide sisestusreeglite seadistamine
description: See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779458"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Pangateenuste ja akreditiivide sisestusreeglite seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist. 

Ülesandes kasutatakse demoettevõtte USMF andmeid.


## <a name="general-ledger-parameter"></a>Pearaamatu parameeter
1. Avage sularaha **ja panga > > parameetrite seadistus**.
2. Laiendage jaotist **Pank**.
3. Valige suvand **Luba impordi akreditiivi** suvand.
4. Valige suvand **Luba ekspordi akreditiivi** suvand.
5. Klõpsake nuppu **Salvesta**.
6. Sulgege leht.

## <a name="create-bank-facility"></a>Panga süsteemiteenuse loomine
1. Avage sularaha **- ja pangahalduse > installiprogrammi > panga vahendid**.
2. Klõpsake valikut **Uus**.
3. Väljale Süsteemiteenuse **grupp** sisestage panga süsteemiteenuse grupi nimi.
4. Sisestage **väljale** Kirjeldus panga süsteemiteenuse grupi kirjeldus.
5. Klõpsake nuppu **Salvesta**.
6. Klõpsake vahekaardil Süsteemiteenuse **tüübid**.
7. Klõpsake valikut **Uus**.
8. Sisestage **väljale** Süsteemiteenuse tüüp kordumatu kood.
9. Sisestage väärtus väljale **Kirjeldus**.
10. **Otsingu avamiseks** klõpsake väljal Süsteemiteenuse grupp ripploendit.
11. Otsige loendist ja valige soovitud kirje.
12. Klõpsake loendis valitud real olevat linki.
13. **Väljal Süsteemiteenuse** olemus valige panga süsteemiteenuse olemus.
14. Klõpsake nuppu **Salvesta**.
15. Sulgege leht.

## <a name="bank-posting-profile"></a>Panga sisestusreegel
1. Avage sularaha **- ja pangahalduse > seadistus > pangadokumentide sisestusreeglid**.
2. Klõpsake valikut **Uus**.
3. **Otsingu avamiseks** klõpsake väljal Konto/grupi number ripploendit.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Valige tasakaalustuse põhikonto.
    * Seda kontot kasutatakse likviidsuse planeerimise arvutamisel.  
7. **Valige kulukannete** konto väljal Kulude konto.
8. **Valige marginaalikannete** konto väljal Marginaali konto.
    * Seda kontot debiteeritakse, kui avamarginaal sisestatakse ja krediteeritakse makse sisestamisel.  
9. Klõpsake nuppu **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
