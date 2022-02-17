---
title: Küsimustike levitamine ajastamise abil
description: Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4885c11f0cb508edb8ebf3aef14748e819113264
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067398"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Küsimustike levitamine ajastamise abil


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

## <a name="create-a-questionnaire-schedule"></a>Küsimustiku graafiku loomine

1. **Avage QuestionnaireDistributeQuestionnaire'i** > **·** > **ajakavad**.

2. Klõpsake valikut **Uus**.

3. Tippige **väljale** Planeerimine väärtus.

4. Sisestage väärtus väljale **Kirjeldus**.
    * Määrake ajakavaks **Anonüümne**, kui vastused tuleks salvestada vastusega seotud nimedeta.  
    * Anonüümsete tulemuste lubamine tuleb esmalt inimressursside parameetrites seadistada.  

5. Valige väljal **Liik** plaanimistüüp.  Selles näites kasutame **rahulolu** tüüpi.

6. Otsige loendist ja valige soovitud kirje.

7. Klõpsake loendis valitud real olevat linki.

8. Väljale **Kuupäev** sisestage kuupäev.

9. Laiendage jaotist **E-post töötaja iseteeninduse** jaoks.

10. Sisestage väärtus väljale **Teema**.

    * Näide: küsimustik on saadaval  

11. Tippige väljale **Tekst** meilisõnumi keha. Pange tähele, et süsteemis saab kasutada väärtuste asendamiseks muutujat.

    * Näide: Lugupeetud %P%! Töötajate tervise küsitluse täitmiseks palun logige sisse töötaja iseteenindusse.  Contoso  

12. Klõpsake nuppu **Salvesta**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Kasutage seadistuse üksikasju vastamiseks küsimustik(e) valimiseks ja päringuid vastajate valimiseks.

1. Klõpsake nuppu **Häälestuse üksikasjad**.

2. Valige loendist päring, mille abil süsteemist küsimustikule vastajaid leida.

    * Näide: töötajad  

3. Kindlate inimeste valimiseks või päringu kohandamiseks kindlatele kriteeriumidele sobivate inimeste leidmiseks klõpsake nuppu **Kuva või muutke päringut**.

    * Pange tähele, et kõik vastajad peavad olema süsteemi kasutajad.  

4. Märkige loendisse rida isiku jaoks.

5. Sisestage või valige väärtus väljal **Kriteeriumid**.

    * Valige Julia Funderburk  

6. Valige loendist Julia Funderburk

7. Klõpsake valikut **OK**.

8. Klõpsake **vahekaarti Küsimustikud**.

9. Laiendage puus küsimustiku tüübi **Rahulolu-uuringu** sõlme.

10. Märkige puul valik Töötajate tervise hindamine.

11. Klõpsake valikut **OK**.

12. Klõpsake nuppu **Plaanitud vastuseseanss**.

    * Pange tähele, et **iga valitud/küsitud kasutaja jaoks on loodud plaanitud vastuseseansid**.  

13. Sulgege leht.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Küsimustiku graafiku käivitamine küsimustiku vastajatele kättesaadavaks muutmiseks.

1. Klõpsake suvandit **Funktsioonid**.

2. Klõpsake käsku **Käivita**.

3. Klõpsake valikut **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Meili saatmine vastajate teavitamiseks saadaolevast küsimustikust.

1. Klõpsake suvandit **Funktsioonid**.

2. Klõpsake nuppu **Saada meilisõnum**.

3. Klõpsake **Tühista**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Kasutage Valikut Planeeritud vastamisseansid, et jälgida, kes peab küsimustiku täitma.

1. Klõpsake nuppu **Plaanitud vastuseseanss**.

    * Kustutage kõik ülejäänud planeeritud vastamisseansid, kui olete valmis planeeritud seansi lõpetamiseks.  

2. Klõpsake **Kustuta**.

3. Klõpsake nuppu **Jah**.

4. Sulgege leht.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Lõpetage graafik, kui kõik vastajad on küsimustiku täitnud ja/või kõik järelejäänud plaanitud vastuseseansid on kustutatud.

1. Klõpsake suvandit **Funktsioonid**.
2. Klõpsake nuppu **Lõpp**.
3. Klõpsake valikut **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
