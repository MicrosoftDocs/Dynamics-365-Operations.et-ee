---
title: Tegevuste seose loomine – Järgnev tegevus
description: Lean manufacturingi tootmisvoo tegevuste voog talletatakse tegevusseoste kaudu.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5e5844939e1eb40e31530c434c096c5b3be7abe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "325453"
---
# <a name="create-activity-relation-successor"></a>Tegevuse seose loomine: järgnev tegevus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lean manufacturingi tootmisvoo tegevuste voog talletatakse tegevusseoste kaudu. See salvestus näitab, kuidas luua tegevusseoste kogumit.

Eeltingimused:

- Tootmisvoog ja mustand mustandirežiimis. 

- Kaks tootmisvoos üksteisele järgnevat tegevust on loodud, kuid pole seotud.


## <a name="find-the-production-flow-version"></a>Tootmisvoo versiooni leidmine 
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Märkige loendis valitud rida.
5. Valige loendist mustandversioon.
    * Tegevuse seosed saab lisada nii tootmisvoo mustand- kui ka aktiivsetele versioonidele.  

## <a name="open-the-activity-overview"></a>Tegevuse ülevaate avamine
1. Klõpsake suvandit Tegevused.
    * Pange tähele, et vormil kuvatakse kõik tootmisvoo tegevused, mis on eraldatud nende tootmisvoogude versioonile, millega töötate.  

## <a name="add-a-successor"></a>Järeltulija lisamine
1. Klõpsake suvandit Järeltulija lisamine.
2. Klõpsake väljal Tegevus otsingu avamiseks ripploendi nuppu.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Märkige ruut Piirang.
6. Sisestage number väljale Piirangu väärtus.
    * Piirangu aeg on aeg, mis plaanitakse eelkäija plaanitud lõpu (tähtaja kuupäev ja kellaaeg) ning järeltulija planeeritud alguse vahele.  
7. Sisestage väärtus väljale Ühikud.
8. Sisestage number väljale Tsükliaja määr.
    * Kui mõlemad tegevused toimivad samas taktis, siis peab tsükli aja suhte väärtus olema 1. Kui eelnev tegevus toimib järgnevast kaks korda kiiremini, siis peab suhte väärtus olema 2.   Tsükli aja suhteid kasutatakse tootmisvoo tegevuste individuaalsete tsükli aegade arvutamiseks.  
9. Klõpsake nuppu OK.
10. Sulgege leht.
11. Klõpsake vahekaarti GridPanel.
12. Sulgege leht.
13. Värskendage lehte.

