---
title: Tööajaarvestuse palgaarvestuse protsessi lubamine
description: Selles protseduuris näitlikustatakse, kuidas aktiveerida palgaarvestuse protsessi tööajaarvestuse põhjal.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3b196e25699c43dbac06e950aae0ad8a9457a8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566547"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Tööajaarvestuse palgaarvestuse protsessi lubamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]