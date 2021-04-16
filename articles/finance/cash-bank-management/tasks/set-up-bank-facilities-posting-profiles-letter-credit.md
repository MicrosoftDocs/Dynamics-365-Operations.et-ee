---
title: Pangateenuste ja akreditiivide sisestusreeglite seadistamine
description: See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 945504cd73b743fb3711997274c537e51e5c6dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834640"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Pangateenuste ja akreditiivide sisestusreeglite seadistamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]