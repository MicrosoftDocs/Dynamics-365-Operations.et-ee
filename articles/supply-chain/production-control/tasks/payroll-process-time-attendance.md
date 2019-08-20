---
title: Tööajaarvestuse palgaarvestuse protsessi lubamine
description: Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843525"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Tööajaarvestuse palgaarvestuse protsessi lubamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Seostatud tasumääraga tasutüübi loomine
1. Tööajaarvestus > Seadistus > Palk > Tasutüübid
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tasutüüp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.
6. Klõpsake valikut Määrad.
    * Tasutüüpide määrad seatakse konkreetseteks ajaperioodideks ja töötajatele saab luua eri tasumäärasid. Tasumäärade loomine tööajaarvestuse järgi ei ole alati vajalik. See teave võib juba olemas olla palgaarvestussüsteemis, kus palku luuakse.  
7. Klõpsake valikut Uus.
8. Märkige loendis valitud rida.
9. Sisestage arv väljale Määr.
10. Klõpsake nuppu Salvesta.

## <a name="create-a-pay-agreement"></a>Tasuleppe loomine
1. Sulgege leht.
2. Sulgege leht.
3. Avage Tasulepped.
    * Tööajaarvestus > Seadistus > Tasulepped  
4. Klõpsake valikut Uus.
5. Sisestage väärtus väljale Tasulepe.
6. Sisestage väljale Kirjeldus soovitud väärtus.
7. Klõpsake nuppu Salvesta.
8. Klõpsake valikut Lepingu read.
9. Klõpsake valikut Uus.
10. Märkige loendis valitud rida.
11. Sisestage või valige väärtus väljal Reeglite tüüp.
12. Sisestage või valige väärtus väljal Tasutüüp.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Kellaaja registreerimisega töötaja tasuleppe seadistamine
1. Sulgege leht.
2. Sulgege leht.
3. Avage jaotis Ajalise registreerimise töötajad.
    * Tööajaarvestus > Seadistus > Ajalise registreerimise töötajad  
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake vahekaarti Tööhõive.
6. Laiendage jaotist Ajaline registreerimine.
7. Klõpsake nuppu Redigeeri.
8. Sisestage või valige väärtus väljal Tasulepe.

