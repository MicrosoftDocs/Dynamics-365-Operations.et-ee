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
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82f688a3d9366e629eedefd876dd5669bd7ed04
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691634"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Küsimustike levitamine ajastamise abil


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

## <a name="create-a-questionnaire-schedule"></a>Küsimustiku graafiku loomine

1. Minge plaanidele **QuestionnaireDistributeQuestionnaire** > **·** > **·**.

2. Klõpsake valikut **Uus**.

3. **Tippige väärtus** väljale Planeerimine.

4. Sisestage väärtus väljale **Kirjeldus**.
    * Määrake graafik anonüümseks **,** kui vastused tuleks salvestada ilma vastusega seostatud nimedeta.  
    * Anonüümsete tulemuste lubamine tuleb esmalt inimressursside parameetrites seadistada.  

5. **Väljal Tüüp** valige planeerimistüüp.  Selles näites kasutatakse rahulolu **tüüpi**.

6. Otsige loendist ja valige soovitud kirje.

7. Klõpsake loendis valitud real olevat linki.

8. Väljale **Kuupäev** sisestage kuupäev.

9. Laiendage töötaja **iseteeninduse e-kirja jaotist**.

10. Sisestage väärtus väljale **Teema**.

    * Näide: küsimustik on saadaval  

11. **Tippige tekstiväljale** oma meilisõnumi keha. Pange tähele, et süsteemis saab kasutada väärtuste asendamiseks muutujat.

    * Näide: Lugupeetud %P%! Töötajate tervise küsitluse täitmiseks palun logige sisse töötaja iseteenindusse.  Contoso  

12. Klõpsake nuppu **Salvesta**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Kasutage seadistuse üksikasju vastamiseks küsimustik(e) valimiseks ja päringuid vastajate valimiseks.

1. Klõpsake seadistuse **üksikasju**.

2. Valige loendist päring, mille abil süsteemist küsimustikule vastajaid leida.

    * Näide: töötajad  

3. Kindlate **inimeste valimiseks või päringu kohandamiseks** kindlate kriteeriumitega inimeste leidmiseks klõpsake nuppu Vaata või muuda päringut.

    * Pange tähele, et kõik vastajad peavad olema süsteemi kasutajad.  

4. Märkige loendis rida Isiku jaoks.

5. Sisestage või valige väärtus väljal **Kriteeriumid**.

    * Valige Julia Funderburk  

6. Valige loendist Julia Funderburk

7. Klõpsake valikut **OK**.

8. Klõpsake vahekaarti **Küsimustikud**.

9. Laiendage puus küsimustikutüübi rahulolu-uuringu **sõlme**.

10. Märkige puul valik Töötajate tervise hindamine.

11. Klõpsake valikut **OK**.

12. Klõpsake planeeritud **vastamisseanssi**.

    * Pange tähele, **et igale valitud** /päringuga kasutajale on loodud plaanitud vastamisseansid.  

13. Sulgege leht.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Küsimustiku graafiku käivitamine küsimustiku vastajatele kättesaadavaks muutmiseks.

1. Klõpsake suvandit **Funktsioonid**.

2. Klõpsake käsku **Käivita**.

3. Klõpsake valikut **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Meili saatmine vastajate teavitamiseks saadaolevast küsimustikust.

1. Klõpsake suvandit **Funktsioonid**.

2. Klõpsake käsku **Saada meilisõnum**.

3. Klõpsake **Tühista**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Kasutage Valikut Planeeritud vastamisseansid, et jälgida, kes peab küsimustiku täitma.

1. Klõpsake planeeritud **vastamisseanssi**.

    * Kustutage kõik ülejäänud planeeritud vastamisseansid, kui olete valmis planeeritud seansi lõpetamiseks.  

2. Klõpsake **Kustuta**.

3. Klõpsake nuppu **Jah**.

4. Sulgege leht.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Lõpetage graafik, kui kõik vastajad on küsimustiku täitnud ja/või kõik järelejäänud plaanitud vastuseseansid on kustutatud.

1. Klõpsake suvandit **Funktsioonid**.
2. Klõpsake **nuppu Lõpeta**.
3. Klõpsake valikut **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
