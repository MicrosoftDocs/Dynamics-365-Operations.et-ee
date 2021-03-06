---
title: Tegevuste seose loomine – Järgnev tegevus
description: Lean manufacturingi tootmisvoo tegevuste voog talletatakse tegevusseoste kaudu.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46dda12d4ad2b23ee86d240e6cdd8a1d46f1838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829230"
---
# <a name="create-activity-relation---successor"></a>Tegevuste seose loomine – Järgnev tegevus

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]