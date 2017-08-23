--- 
title: Pangateenuste ja akreditiivide sisestusreeglite seadistamine
description: "See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4cf5d982fa58df93529f3506beef46f660265530
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Pangateenuste ja akreditiivide sisestusreeglite seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist. 

Ülesandes kasutatakse demoettevõtte USMF andmeid.






## <a name="general-ledger-parameter"></a>Pearaamatu parameeter
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.
2. Laiendage jaotist Pangadokument.
3. Valige suvand Impordi akreditiivi lubamine.
4. Valige suvand Ekspordi akreditiivi lubamine.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.

## <a name="create-bank-facility"></a>Panga süsteemiteenuse loomine
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Panga süsteemiteenused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Süsteemiteenuste tüüp panga süsteemiteenuste grupi nimi.
4. Sisestage väljale Kirjeldus panga süsteemiteenuste grupi kirjeldus.
5. Klõpsake nuppu Salvesta.
6. Klõpsake vahekaarti Süsteemiteenuste tüübid.
7. Klõpsake valikut Uus.
8. Sisestage ainuidentifikaator väljale Süsteemiteenuse tüüp.
9. Sisestage väljale Kirjeldus soovitud väärtus.
10. Klõpsake väljal Süsteemiteenuste grupp otsingu avamiseks ripploendi nuppu.
11. Otsige loendist ja valige soovitud kirje.
12. Klõpsake loendis valitud real olevat linki.
13. Valige väljal Süsteemiteenuste olemus panga süsteemiteenuste olemus.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.

## <a name="bank-posting-profile"></a>Panga sisestusreegel
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Pangadokumentide sisestusreegel.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Konto/grupi nimi otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Valige tasakaalustuse põhikonto.
    * Seda kontot kasutatakse likviidsuse planeerimise arvutamisel.  
7. Valige väljal Tasude konto kulukannete konto.
8. Valige väljal Kasumikonto marginaalkannete konto.
    * Seda kontot debiteeritakse, kui avamarginaal sisestatakse ja krediteeritakse makse sisestamisel.  
9. Klõpsake nuppu Salvesta.


