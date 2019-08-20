---
title: Veose automaatse vastavusseviimise seadistamine
description: See protseduur näitab, kuidas seadistada andmeid veose automaatseks vastavusseviimiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 057d1b3a1b5294c75f02f4ed443ae6f525ac6b83
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837610"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Veose automaatse vastavusseviimise seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada andmeid veose automaatseks vastavusseviimiseks. Sellega tegeleb tavaliselt laohaldur. Saate seda protseduuri kasutada demoandmete ettevõttes USMF.


## <a name="set-up-the-freight-bill-type"></a>Veoarve tüübi seadistamine
1. Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Veoarve tüüp.
    * Veoarve tüüp määratleb, kuidas veoarveid ja vedaja arveid tuleks vastendada.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Veoarve tüüp.
4. Tippige väljale Mootori koost Microsoft.Dynamics.Ax.Tms.dll.
    * See on standardne transpordihalduse vastendusmootori koodi teek.  
5. Tippige väljale Mootori klass Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.
    * See on standardne transpordihalduse vastendusmootori klass.  
6. Klõpsake valikut Uus.
7. Valige väljalt Kirjeldus väärtus, mis peaks veoarvel ja vedaja arvel ühtima.  
8. Valige Jah väljalt Sobitus on nõutav.
    * Kui määrate selle välja väärtuseks Jah, siis tähendab see, et väljal Kirjeldus valitud väärtus peab olema vastav nii veoarvel kui ka vedaja arvel. Kui määrate väärtuseks Ei, võib ühel neist see väli tühi olla.  
9. Klõpsake nuppu Salvesta.

## <a name="set-up-the-freight-bill-type-assignment"></a>Veoarve tüübi määramise seadistamine
1. Sulgege leht.
2. Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Veoarve tüübi määramised.
    * Veoarve tüübi määrangut kasutatakse määramiseks, millist veoarve tüüpi konkreetse vedaja puhul kasutatakse.   
3. Klõpsake valikut Uus.
4. Valige või sisestage väärtus väljal Režiim.
5. Valige või sisestage väärtus väljal Kättetoimetaja.
6. Valige väljalt Veoarve tüüp varem loodud veoarve tüüp.
7. Sulgege leht.

## <a name="set-up-the-audit-master"></a>Auditi koondi seadistamine
1. Avage Transpordihaldus > Seadistus > Veose vastavusseviimine > Auditi koond.
    * Auditi koond määratleb automaatne veose vastavusseviimise lubatud hälbe. See määrab kui palju veoarve ja vedaja arve rahasummad võivad erineda, et vastavusseviimine siiski toimuda saaks. See määratleb ka lahknevuste käsitlemise viisi.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Auditi koondi ID.
4. Valige väljalt Kättetoimetaja sama kättetoimetaja, kelle varem valisite.
5. Valige väljalt Veoarve tüüp varem loodud veoarve tüüp.
6. Laiendage jaotist Hälve.
7. Sisestage number väljale Minimaalne lubatud hälbe tase.
8. Sisestage number väljale Maksimaalne lubatud hälbe tase.
9. Laiendage jaotist Tulemus.
10. Valige või sisestage väärtus väljal Ülemakse põhjuse kood.
    * Kui summad on veoarvel ja vedaja arvel erinevad, määratlevad üle- ja alamakse põhjuse koodid kontod, millel vahe tuleks registreerida, kuni vahe on lubatud hälbe piirides.  
11. Valige või sisestage väärtus väljal Alamakse põhjuse kood.
12. Sulgege leht.

