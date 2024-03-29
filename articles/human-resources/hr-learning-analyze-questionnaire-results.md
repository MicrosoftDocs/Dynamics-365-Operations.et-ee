---
title: Küsimustiku tulemuste analüüsimine
description: Küsimustiku statistikat saab kasutada keskmiste, summade ja protsentide arvutamiseks demograafiliste andmete põhjal.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692915"
---
# <a name="analyzing-questionnaire-results"></a>Küsimustiku tulemuste analüüsimine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Küsimustiku statistikat saab kasutada keskmiste, summade ja protsentide arvutamiseks demograafiliste andmete põhjal. Selle protseduuri alustamiseks avage **Küsimustik** > **Tulemuste kuvamine ja analüüsimine** > **Küsimustiku statistika**. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-questionnaire-statistics-record"></a>Küsimustiku statistika kirje loomine
1. Avage **Küsimustiku statistika**.
2. Klõpsake valikut **Uus**.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale **Statistika**.
5. Sisestage väärtus väljale **Kirjeldus**.
6. Klõpsake väljal **Küsimustik** otsingu avamiseks ripploendi nuppu.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake vahekaarti **Üldine**.
    * Valige, kas soovite kaasata anonüümseid tulemusi või tulemusi töötajatelt, kontaktidelt ja kandidaatidelt.  
9. Valige või tühjendage märkeruut **Töötaja**.
    * Kui vaatate staaži või vanuse tulemusi, määrake vahemikud, mida sooviksite kasutada tulemuste grupeerimiseks.  
    * Vanusevahemiku puhul 5 sisestamine grupeerib tulemused viieaastaste vanusevahemike põhjal.  
10. Sisestage number väljale **Vanus**.
    * Valige, kas soovite käitada arvutamist kogu küsimustiku, iga tulemustegrupi, iga küsimuse või iga küsimuse rea puhul.  
    * Valige, kuidas soovite tulemused grupeerida.  
    * Näiteks kui arvutate keskmised punktid küsimuse kohta, võite soovida näha küsimusi tulemusegrupi järgi grupeerituna.  
    * Valige andmed, mis arvutamisel aluseks võtta.  
    * Näiteks kui soovite vaadata töötajate hulgas saadud küsimustiku keskmist protsenti ja töötajate hulgas saadud punktide keskmist arvu.  
11. Klõpsake vahekaarti **Vahemik**.
    * Kasutage tulemikomplekti piiramiseks ainult neid vahemikke, mis vahemiku kriteeriumidele vastavad.  
12. Klõpsake vahekaarti **Grupeerimisalus**.
    * Kasutage tulemuste kuvamise viisi määramiseks grupeerimisi.  
    * Näiteks grupeerige tulemused esmalt soo, seejärel vanuse järgi.  
13. Otsige loendist ja valige soovitud kirje.
    * Teisaldage grupeerimised **valitud** poolele ja pange need soovitud järjekorda.  

## <a name="execute-the-statistics-calculation"></a>Statistika arvutamine
1. Klõpsake nuppu **Käivita**.
    * Valige, millist arvutusfunktsiooni soovite tulemuste puhul kasutada.  
    * Näiteks arvutage küsimustiku keskmised protsendid valitud grupeerimiste puhul või valitud grupeerimiste tulemustegrupi punktid kokku.  
2. Märkige või tühjendage ruut **Kustuta varasemad otsingud**.
3. Klõpsake valikut **OK**.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Küsimustiku statistika käituse tulemuste kuvamine.
1. Klõpsake vahekaarti **Tulemus**.
2. Klõpsake vahekaarti **Tulemus**.
3. Sulgege leht.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
