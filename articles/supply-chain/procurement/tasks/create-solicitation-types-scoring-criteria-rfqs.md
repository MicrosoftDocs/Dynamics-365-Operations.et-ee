---
title: Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine
description: See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262209"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine

[!include [banner](../../includes/banner.md)]

See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada. Samuti näitav see, kuidas kasutada kutse tüüpi pakkumiskutsel, mis siis vaike-hindamismeetodi määrab. Neid ülesandeid täidab üldjuhul ostujuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Enne alustamist peab teil olema hindamismeetod kättesaadav.


## <a name="create-a-solicitation-type"></a>Kutsetüübi loomine
1. Valige Hanked > Seadistus > Pakkumiskutse > Kutse tüüp.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljalt Hindamismeetod hindamismeetod, mida soovite selle kutse tüübi puhul kasutada.
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.

## <a name="use-the-solicitation-type"></a>Kutse tüübi kasutamine
1. Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.
2. Klõpsake valikut Uus.
3. Valige väljalt Kutse tüüp äsja loodud kutse tüüp. 
    *   
4. Klõpsake nuppu OK.
5. Klõpsake valikut Hindamiskriteeriumid.
    * Kuvatud hindamiskriteeriumid on kutse tüübiga seotud hindamismeetodi omad. Saate sellele lehele kriteeriume lisada või kustutada. Võimalik on ka uute kriteeriumide lisamine, kopeerides need muudest hindamismeetoditest.  
6. Klõpsake valikut Kopeeri kriteerium.
7. Valige või sisestage väärtus väljal Hindamismeetod.
8. Klõpsake nuppu OK.
9. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]