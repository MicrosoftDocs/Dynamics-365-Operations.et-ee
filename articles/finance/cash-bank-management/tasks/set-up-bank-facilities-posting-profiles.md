---
title: Pangateenuste ja garantiikirjade sisestusreeglite seadistamine
description: Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 427159048ffbb17749e813d67a900622900a7f21
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177365"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Pangateenuste ja garantiikirjade sisestusreeglite seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.



See ülesanne kasutab demoettevõtte USMF andmeid. 




## <a name="general-ledger-parameter"></a>Pearaamatu parameeter
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.
2. Laiendage jaotist Pangadokument.
3. Valige suvand Garantiikirja lubamine.
4. Klõpsake väljal Kande tööleht otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake vahekaarti Numbriseeriad.
    * Numbriseeria määratlemine garantiikirja numbri ja garantiikirja kandeviidete jaoks  
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.

## <a name="create-bank-facility"></a>Panga süsteemiteenuse loomine
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Panga süsteemiteenused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Süsteemiteenuste grupp garantiikirja kande jaoks panga süsteemiteenuste grupi nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.
6. Klõpsake vahekaarti Süsteemiteenuste tüübid.
7. Klõpsake valikut Uus.
8. Sisestage väljale Süsteemiteenuste tüüp panga süsteemiteenuse leppega seotud panga süsteemiteenuste tüübi nimi.
9. Sisestage väärtus väljale Kirjeldus.
10. Klõpsake väljal Süsteemiteenuste grupp otsingu avamiseks ripploendi nuppu.
11. Otsige loendist ja valige soovitud kirje.
12. Klõpsake loendis valitud real olevat linki.
13. Valige suvand väljal Süsteemiteenuse olemus.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.

## <a name="bank-posting-profile"></a>Panga sisestusreegel
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Pangadokumentide sisestusreegel.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Konto/grupi nimi otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Valige väljal Tasakaalustuskonto tasakaalustuseks põhikonto.
7. Valige väljal Tasude konto kulukannete konto.
8. Valige väljal Kasumikonto marginaalkande jaoks konto.
9. Valige väljal Likvideerimiskonto garantiikirja kande likvideerimiskonto. 
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.

